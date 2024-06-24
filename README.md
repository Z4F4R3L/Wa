<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.tailwindcss.com"></script>
    <title>Whatsapp Chat</title>
  </head>
  <body>
    <div
      class="max-w-xl w-full mx-auto text-center min-h-screen flex flex-col items-center justify-center"
    >
      <h1 class="text-2xl font-bold sm:text-3xl">Go To Whatsapp</h1>
      <form
        action="#"
        class="mx-auto mb-0 mt-8 max-w-md space-y-4"
        onsubmit="sendMessageToWhatsapp()"
      >
        <input
          type="text"
          class="w-300 rounded-lg border border-green-200 p-4 pe-12 text-sm shadow-sm"
          placeholder="Nomor yang dituju"
          value="6285182752645"
          id="nomor"
        />
        <br>
        <input
          type="text"
          class="w-300 rounded-lg border border-green-100 p-4 pe-12 text-sm shadow-sm"
          placeholder="ketik pesan anda..."
          id="pesan"
        />
        <br>
        <button
          type="submit"
          class="inline-block rounded-lg bg-green-500 px-5 py-3 text-sm font-medium text-white rounded-w"
        >
          Kirim Pesan
        </button>
      </form>
    </div>
    <script>
      function sendMessageToWhatsapp() {
        const urlToWhatsapp = `https://wa.me/${nomor.value}?text=${pesan.value}`;

        window.open(urlToWhatsapp, "_blank");
      }
    </script>
  </body>
</html>
