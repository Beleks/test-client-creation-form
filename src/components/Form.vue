<template>
  <div class="forms">
    <div class="FIO">
      <div class="field">
        <div>
          <div class="title">
            Имя
            <div class="important">Обязательно</div>
          </div>
          <div class="input">
            <input type="text" />
          </div>
        </div>
        <div>
          <div class="title">
            Фамилия
            <div class="important">Обязательно</div>
          </div>
          <div class="input">
            <input type="text" />
          </div>
        </div>
        <div>
          <div class="title">
            Отчество
            <!-- <div class="important">Обязательно</div> -->
          </div>
          <div class="input">
            <input type="text" />
          </div>
        </div>
      </div>
    </div>
    <div class="dob">
      <div class="field">
        <div class="title">
          Дата рождения
          <div class="important">Обязательно</div>
        </div>
        <div class="birth">
          <div class="input small">
            <div>ДД</div>
            <input type="text" />
          </div>
          <div class="input small">
            <div>ММ</div>
            <input type="text" />
          </div>
          <div class="input big">
            <div>ГГГГ</div>
            <input type="text" />
          </div>
        </div>
      </div>
    </div>
    <div class="phone">
      <div class="field">
        <div class="title">
          Номер телефона
          <div class="important">Обязательно</div>
        </div>
        <div class="phone-input">
          <div>+7</div>
          <input type="text" />
        </div>
      </div>
    </div>
    <div class="gender">
      <div class="field">
        <div class="title">
          Пол
          <!-- <div class="important">Обязательно</div> -->
        </div>
        <div class="gender-chose">
          <div class="left">Жен</div>
          <div class="right">Муж</div>
        </div>
      </div>
    </div>
    <div class="group">
      <div class="field">
        <div class="title">
          Группа клиентов
          <div class="important">Обязательно</div>
        </div>
        <div class="group-chose">
          <div class="left">VIP</div>
          <div class="center">Проблемные</div>
          <div class="right">ОМС</div>
        </div>
      </div>
    </div>
    <div class="doctor">
      <div class="field">
        <div class="title">
          Лечущий врач
          <!-- <div class="important">Обязательно</div> -->
        </div>
        <select name="" id="">
          <option value="1">Иванов</option>
          <option value="2">Захаров</option>
          <option value="3">Чернышева</option>
        </select>
      </div>
    </div>
    <div class="sms">
      <div class="field">
        <input type="checkbox" name="sms" id="" />
        <label for="sms">Не отправлять СМС</label>
      </div>
    </div>
    <div class="place">
      <div class="field">
        <div>
          <div class="title">Страна</div>
          <div class="input">
            <input type="text" />
          </div>
        </div>
        <div>
          <div class="title">Область</div>
          <div class="input">
            <input type="text" />
          </div>
        </div>
        <div>
          <div class="title">
            Город
            <div class="important">Обязательно</div>
          </div>
          <div class="input">
            <input type="text" />
          </div>
        </div>
      </div>
    </div>
    <div class="index">
      <div class="field">
        <div class="title">Индекс</div>
        <div class="">
          <input type="text" />
        </div>
      </div>
    </div>
    <div class="house">
      <div class="field">
        <!-- <div class="title">
          Номер телефона
          <div class="important">Обязательно</div>
        </div> -->
        <div class="hose-input">
          <div>Улица</div>
          <input type="text" />
        </div>
        <div class="number-hose-input">
          <div>Дом</div>
          <input type="text" />
        </div>
      </div>
    </div>
    <div class="document-type">
      <div class="field">
        <div class="title">
          Тип документа
          <div class="important">Обязательно</div>
        </div>
        <div class="type">
          <div class="left" :class="{ active: documentType === 'Паспорт' }" @click="documentType = 'Паспорт'">
            Паспорт
          </div>
          <div
            class="center"
            :class="{ active: documentType === 'Свидетельство о рождении' }"
            @click="documentType = 'Свидетельство о рождении'"
          >
            Свидетельство о рождении
          </div>
          <div
            class="right"
            :class="{ active: documentType === 'Вод. удостоверение' }"
            @click="documentType = 'Вод. удостоверение'"
          >
            Вод. удостоверение
          </div>
        </div>
        <div class="pasport">
          <div class="series-input">
            <div>Серия</div>
            <input type="text" />
          </div>
          <div class="number-input">
            <div>Номер</div>
            <input type="text" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      documentType: "Паспорт",
    };
  },
  mounted() {},
};
</script>

<style lang="scss" scoped>
.forms {
  display: flex;
  flex-direction: column;
  // align-items: center;
}

// =========
.FIO {
  // display: flex;
  .field {
    display: flex;
    flex-wrap: wrap;
    // justify-content: center;
    > div {
      margin-top: 0.5em;
      margin-right: 0.5em;
    }
  }
}
.dob {
  // display: flex;
  // flex

  .birth {
    display: flex;
    > div {
      margin-right: 0.5em;
    }
    .small {
      text-align: center;
      input {
        max-width: 30px;
      }
    }
    .big {
      text-align: center;
      input {
        max-width: 60px;
      }
    }
    .input {
      input {
        text-align: center;
      }
    }
  }
}
.phone-input {
  display: flex;
  align-items: center;
  input {
    margin-left: 0.3em;
  }
}
.gender {
  .gender-chose {
    display: flex;
    > div {
      cursor: pointer;
      padding: 0.3em 0.5em;
      border: 1px solid black;
    }
    .right {
      border-radius: 0 5px 5px 0;
    }
    .left {
      border-right: none;
      border-radius: 5px 0 0 5px;
    }
  }
}
.group {
  .group-chose {
    display: flex;
    flex-direction: column;
    > div {
      max-width: 100px;
      text-align: center;
      cursor: pointer;
      padding: 0.3em 0.5em;
      margin: 0.3em 0;
      // background-color: gray;
      border: 1px solid black;
      border-radius: 5px;
    }
  }
}
.sms {
}
.place {
  .field {
    display: flex;
    flex-wrap: wrap;
    // justify-content: center;
    > div {
      margin-top: 0.5em;
      margin-right: 0.5em;
    }
  }
}
.house {
  .field {
    display: flex;
    flex-wrap: wrap;
    > div {
      margin-right: 1em;
      margin-top: 0.5em;
      display: flex;
      align-items: center;
      > div {
        font-size: 1.1rem;
        margin-right: 0.3em;
        min-width: 60px;
      }
    }
    .number-hose-input {
      > div {
        text-align: center;
      }
      input {
        max-width: 70px;
      }
    }
  }
}
.document-type {
  .field {
    .type {
      display: flex;

      > div {
        display: flex;
        align-items: center;
        font-size: 0.9rem;
        cursor: pointer;
        padding: 0.3em 0.5em;
        border: 1px solid black;
      }
      .right {
        border-radius: 0 5px 5px 0;
        border-left: none;
      }
      .left {
        border-right: none;
        border-radius: 5px 0 0 5px;
      }
      .active {
        color: white;
        background-color: rgba(66, 184, 131, 1);
      }
    }
    .pasport {
      margin-top: 1em;
      display: flex;
      > div {
        margin-right: 0.5em;
      }
    }
  }
}
// ==============
.field {
  margin: 1em 0.4em;
}
.title {
  font-size: 1.1rem;
  display: flex;
  align-items: center;
  margin-bottom: 0.3em;
}

.important {
  margin-left: 1em;
  border-radius: 5px;
  padding: 0.1em 0.3em;
  font-size: 0.8rem;
  background-color: rgb(255, 162, 171);
}
input {
  // height: 40px;
  padding: 0.5em;
  border: 1px solid black;
  // border: 1px solid rgb(255, 55, 55);

  border-radius: 5px;
  background-image: none;
  background-color: transparent;
  box-shadow: none;
  outline: none;
  z-index: 10;
  font-size: 1rem;
  // min-width: 280px;
}
select {
  font-size: 1rem;
  width: 200px;
}
</style>