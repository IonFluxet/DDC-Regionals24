# DDC-Regionals24
Writeup DDC-regionals


## Drilske Dæknavne - Email
Jeg har brugt Autopsy til denne opgave

- Importer filen til Autopsy.

Det skulle gerne se noglelunde sådan her ud:

![image](https://github.com/IonFluxet/DDC-Regionals24/assets/93826052/27adcf24-3940-4a0f-8ee1-82becd6c5668)

- Hvis vi kigger under "Web accounts" kan vi se emailen

![image](https://github.com/IonFluxet/DDC-Regionals24/assets/93826052/2e6ba9b1-6b8c-44ea-b1d1-8d3193677ccd)

#### Flag: DDC{michellinmartin04@gmail.com}


## Drilske Dæknavne - Leverance-IDer

Jeg har brugt Autopsy og SQLite Studio til denne opgave
- Åben dit eksisterende Autopsy case fra Drilske Dæknavne - Email

- Vi skal lede efter Whatsapp database

- Gå ind på Whatsapp's wa.db

![image](https://github.com/IonFluxet/DDC-Regionals24/assets/93826052/7db0a404-79eb-497e-bb15-48f5f3d7afcf)

Nu har jeg allerede kigget i wa.db og ved at der ikke er noget vigigt i den database, jeg fandt dog ud af at msgstore.db var ret interrasant

- Eksporter msgstore.db til dit skrivebord eller hvor du fortrækker

![image](https://github.com/IonFluxet/DDC-Regionals24/assets/93826052/b527b73b-18af-4fcb-a2db-0e15ce666182)

![image](https://github.com/IonFluxet/DDC-Regionals24/assets/93826052/19a3152f-2804-40e6-8e5b-e5b76c106703)

- Åben en form for SQL editor, jeg bruger SQLite studio
- Importer msgstore.db in i SQLite studio

![image](https://github.com/IonFluxet/DDC-Regionals24/assets/93826052/d41f3446-5726-4207-b726-eac7d6141dc5)

Jeg syntes det er nemmere at kigge alle tables igennem ved at eksportere databasen som en html
- Eksporter msgstore og vælg at eksporter den som en html fil

![image](https://github.com/IonFluxet/DDC-Regionals24/assets/93826052/47e06b88-70c2-4492-ab1f-15a8a54c53e3)

- Find den table der hedder: message
- I message kan du se text_data hvor du kan se beskederne mellem de to personer jeg ikke kan huske navne på

![image](https://github.com/IonFluxet/DDC-Regionals24/assets/93826052/5d536c28-8b27-4bad-927b-f74cafc5105f)

- I den ene besked står der leveringskoderne til de 5 poser vasketøj

![image](https://github.com/IonFluxet/DDC-Regionals24/assets/93826052/35b73888-94a3-4fa5-857a-da8ba6762c36)

- Vi kan se 5 koder, LKJ73, HDH79, VCS13, LÆD72, SJV4W.
- Når vi sætter dem sammen får vi:
#### Flag: DDC{LKJ73-HDH79-VCS13-LÆD72-SJV4W}
