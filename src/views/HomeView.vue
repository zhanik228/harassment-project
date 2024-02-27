<script setup>  
</script>

<template>
  <main>
    <div class="max-w-screen-lg mx-auto p-2 sm:p-5">
        <div class="grid grid-cols-1 md:grid-cols-12 border">
            <div class="bg-gray-900 md:col-span-4 p-5 sm:p-10 text-white">
                <div class="logo">
                    <img class="mx-auto" src="../assets/logo108.png" alt="">
                </div>
                <h2 class="mt-4 text-xl mb-10 text-center">
                    Комитет Государственных Доходов Министерства финансов Республики Казахстан
                </h2>
                <p class="mt-4 text-sm leading-7 font-regular uppercase">
                    Обращение 
                </p>
                <h3 class="text-3xl sm:text-4xl leading-normal font-extrabold tracking-tight">
                    Связаться с <span class="text-indigo-600">Нами</span>
                </h3>
<!--               
                <div class="flex items-center mt-5">
                    <svg class="h-6 mr-2 text-indigo-600" fill="currentColor" version="1.1"
                        xmlns="http://www.w3.org/2000/svg" viewBox="0 0 489.536 489.536"
                        xmlns:xlink="http://www.w3.org/1999/xlink" enable-background="new 0 0 489.536 489.536">
                        <g>
                            <g>
                                <path
                                    d="m488.554,476l-99-280.2c-1-4.2-5.2-7.3-9.4-7.3h-45.6c12.9-31.1 19.6-54.9 19.6-70.8 0-64.6-50-117.7-112.5-117.7-61.5,0-112.5,52.1-112.5,117.7 0,17.6 8.2,43.1 19.9,70.8h-39.7c-4.2,0-8.3,3.1-9.4,7.3l-99,280.2c-3.2,10.3 6.3,13.5 9.4,13.5h468.8c4.2,0.5 12.5-4.2 9.4-13.5zm-246.9-455.3c51,1.06581e-14 91.7,43.7 91.7,96.9 0,56.5-79.2,182.3-91.7,203.1-31.3-53.1-91.7-161.5-91.7-203.1 0-53.1 40.6-96.9 91.7-96.9zm-216.7,448l91.7-259.4h41.7c29.9,64.1 83.3,151 83.3,151s81.4-145.7 83.8-151h47.4l91.7,259.4h-439.6z">
                                </path>
                                <rect width="136.5" x="177.054" y="379.1" height="20.8"></rect>
                                <path
                                    d="m289.554,108.2c0-26-21.9-47.9-47.9-47.9s-47.9,21.9-47.9,47.9 20.8,47.9 47.9,47.9c27.1,0 47.9-21.8 47.9-47.9zm-75-1c0-14.6 11.5-27.1 27.1-27.1s27.1,12.5 27.1,27.1-11.5,27.1-27.1,27.1c-14.6,2.84217e-14-27.1-12.5-27.1-27.1z">
                                </path>
                            </g>
                        </g>
                    </svg>
                    <span class="text-sm">House #14, Street #12, Darulaman Road, Kabul, Afghanistan.</span>
                </div> -->
                <div class="flex items-center mt-5">
                    <svg class="h-6 mr-2 text-indigo-600" fill="currentColor" version="1.1" id="Capa_1"
                        xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
                        viewBox="0 0 300.988 300.988" style="enable-background:new 0 0 300.988 300.988;"
                        xml:space="preserve">
                        <g>
                            <g>
                                <path d="M150.494,0.001C67.511,0.001,0,67.512,0,150.495s67.511,150.493,150.494,150.493s150.494-67.511,150.494-150.493
                    S233.476,0.001,150.494,0.001z M150.494,285.987C75.782,285.987,15,225.206,15,150.495S75.782,15.001,150.494,15.001
                    s135.494,60.782,135.494,135.493S225.205,285.987,150.494,285.987z">
                                </path>
                                <polygon
                                    points="142.994,142.995 83.148,142.995 83.148,157.995 157.994,157.995 157.994,43.883 142.994,43.883 		">
                                </polygon>
                            </g>
                        </g>
                    </svg>
                    <span class="text-sm">24/7</span>
                </div>
                <div class="flex items-center mt-5 gap-2">
                    <span class="font-bold">Telegram:</span> <a href="https://t.me/SalyqBot" class="text-sm text-indigo-600 font-semibold"> @SalyqBot</a>
                </div>
                <p class="mt-4 leading-7 text-gray-200">
                    Все данные защищены
                </p>
            </div>
            <form class="form md:col-span-8 p-3 sm:p-10" @submit.prevent="sendMessage">
              <input hidden type="text" name="to_name" value="zhanik">
                <div class="flex flex-col h-full  flex-wrap justify-between mb-6">
                    <div class="w-full px-3">
                        <h1 class="text-3xl font-bold">Анонимное Обращение </h1>
                        <p class="mb-10">Оставьте обращение, ваши данные не будут видны</p>
                    </div>
                    <div class="flex flex-col w-full px-3">
                        <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
                            for="message">
                            Ваше сообщение
                        </label>
                        <textarea 
                            id="message"
                            placeholder="Введите ваше обращение"
                            v-model="message"
                            rows="10"
                            :class="`appearance-none block w-full  text-gray-700 border ${!message && error ? 'border-red-500' : ''} rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white`"
                            name="message"
                            ></textarea>
                            <p v-if="!message && error" class="text-red-500 text-xs italic">Пожалуйста заполните это поле.</p>
                        <button
                            class=" self-end shadow bg-indigo-600 hover:bg-indigo-400 focus:shadow-outline focus:outline-none text-white font-bold py-2 px-6 rounded"
                            type="submit">
                            Отправить Обращение
                        </button>
                    </div>
                  
                </div>
                <p v-if="success" class="text-green-500 text-xs italic">Успешно отправлено.</p>
            </form>
          
        </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      message: '',
      error: false,
      success: false,
    }
  },
  methods: {
    async sendMessage() {
      const form = document.querySelector('.form')

      if (!this.message) {
        this.error = true
        console.log('error')
      }

      emailjs.init('rbFI_1ITj3IWrPgho');
      emailjs.sendForm("service_oji1kcr","template_9koj2nj", form);
      this.success = true;
      this.message = ''
    }
  }
}
</script>