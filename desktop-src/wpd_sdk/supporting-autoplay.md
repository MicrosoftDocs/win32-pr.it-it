---
description: Supporto di AutoPlay
ms.assetid: e91334d9-9041-4cb8-a6d0-0e2371800064
title: Supporto di AutoPlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83091191d8468b7ea3d34146e4a4c02e8cf5bf80cb3e49c72dc43bb092d10f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083395"
---
# <a name="supporting-autoplay"></a>Supporto di AutoPlay

AutoPlay è una funzionalità della shell che avvia applicazioni associate a dispositivi specifici. A seconda delle impostazioni correnti di AutoPlay, questa funzionalità eseguirà una delle diverse azioni, ad esempio la presentazione di un elenco di applicazioni di gestione disponibili, la visualizzazione di una visualizzazione di cartelle standard dei file e così via.

In Windows Vista la funzionalità AutoPlay è stata estesa in modo che un dispositivo WPD possa fornire un elenco dei tipi di contenuto supportati. Analogamente, le applicazioni WPD possono registrare i tipi di contenuto supportati. Ad esempio, una procedura guidata di acquisizione di foto può registrarsi come gestore per qualsiasi dispositivo WPD che fornisce immagini e un'applicazione multimediale può registrarsi come gestore per qualsiasi dispositivo che archivia file audio o video.

Le applicazioni registrano informazioni specifiche del gestore scrivendo voci nella chiave **HKEY \_ LOCAL MACHINE SOFTWARE di Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Explorer \\ \\ AutoplayHandlers \\ Handlers.** Usando un gestore dell'applicazione WPD (denominato MyWpdApplication.exe) come esempio, l'applicazione può inserire i valori seguenti sotto una chiave **\\ \\ Handlers MyWpdApplicationHandler.**



| Valore          | Tipo            | Dati                                                 |
|----------------|-----------------|------------------------------------------------------|
| Azione         | REG \_ SZ         | Esplorare il contenuto nei dispositivi portatili.                  |
| CLSIDForCancel | REG \_ SZ         | {00000000-0000-0000-0000-000000000000}               |
| DefaultIcon    | REG \_ EXPAND \_ SZ | %SystemDrive% \\ multimedia \\ wpd \\MyWpdApplication.exe |
| InitCmdLine    | REG \_ SZ         | /AutoPlay                                            |
| ProgID         | REG \_ SZ         | MyWpdApplication.MyWpdApplicationAutoPlay            |
| Provider       | REG \_ SZ         | MyWpdApplication                                     |



 

Per altre informazioni sulle chiavi e i valori del Registro di sistema AutoPlay disponibili nella chiave **HKEY \_ LOCAL MACHINE SOFTWARE microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Explorer \\ \\ AutoplayHandlers, \\** vedere la documentazione corrispondente in MSDN.

### <a name="the-wpd-autoplay-scheme"></a>Schema di riproduzione automatica WPD

Lo schema WPD AutoPlay si integra con la Windows Vista AutoPlay. A tale scopo, supporta tre categorie autoPlay, descritte nella tabella seguente.



| Category | Descrizione                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------|
| Source (Sorgente)   | Un dispositivo WPD può essere considerato come un'origine di contenuto, ovvero il contenuto può essere trasferito dal dispositivo.        |
| Sink     | Un dispositivo WPD può essere considerato come una destinazione per il contenuto, ovvero il contenuto può essere trasferito al dispositivo.    |
| Funzione | Un dispositivo WPD supporta una funzionalità programmabile o controllabile,ad esempio può inviare e ricevere messaggi SMS. |



 

Le applicazioni si registrano per l'origine, il sink e/o la categoria di funzioni appropriati scrivendo voci nella sezione AutoPlay del Registro di sistema. Queste voci vengono visualizzate sotto la **chiave HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Explorer \\ \\ AutoplayHandlers \\ EventHandlers \\ WPD.** Sotto la chiave WPD sono presenti **le chiavi Function**, **Sink** **e Source.** In ognuna di queste chiavi è disponibile un GUID che corrisponde a una categoria funzionale WPD o a un tipo di contenuto.

Nella tabella seguente sono elencati i GUID disponibili nella chiave **Function** del Registro di sistema e viene identificata la categoria funzionale corrispondente a ogni GUID.



| Categoria funzionale WPD                           | Chiave del Registro di sistema (GUID)                    |
|---------------------------------------------------|----------------------------------------|
| CATEGORIA FUNZIONALE WPD \_ \_ \_ ALL                    | {2D8A6512-A74C-448E-BA8A-F4AC07C49399} |
| ACQUISIZIONE AUDIO CATEGORIA FUNZIONALE WPD \_ \_ \_ \_         | {3F2A1919-C7C2-4A00-855D-F57CF06DEBBB} |
| DISPOSITIVO CATEGORIA \_ FUNZIONALE WPD \_ \_                 | {08EA466B-E3A4-4336-A1F3-A44D2B5C438C} |
| CONFIGURAZIONE DI RETE \_ DELLE \_ CATEGORIE FUNZIONALI \_ \_ WPD | {48F4DB72-7C6A-4AB0-9E1A-470E3CDBF26A} |
| INFORMAZIONI SUL \_ RENDERING DELLE \_ CATEGORIE FUNZIONALI \_ WPD \_ | {08600BA4-A7BA-4A01-AB0E-0065D0A356D3} |
| SMS DELLA CATEGORIA \_ FUNZIONALE \_ WPD \_                    | {0044A0B1-C1E9-4AFD-B358-A62C6117C9CF} |
| CATEGORIA FUNZIONALE WPD \_ \_ ACQUISIZIONE DI \_ \_ IMMAGINI \_  | {613CA327-AB93-4900-B4FA-895BB5874B79} |
| ARCHIVIAZIONE DELLE CATEGORIE FUNZIONALI WPD \_ \_ \_                | {23F05BBC-15DE-4C2A-A55B-A9AF5CE412EF} |
| ACQUISIZIONE VIDEO DELLA CATEGORIA FUNZIONALE WPD \_ \_ \_ \_         | {E23E5F6B-7243-43AA-8DF1-0EB3D968A918} |



 

Nella tabella seguente sono elencati i GUID presenti nel **Sink** e le chiavi **di** origine nel Registro di sistema e viene identificato il tipo di contenuto corrispondente a ogni GUID.



| Tipo di contenuto WPD                          | Chiave del Registro di sistema (GUID)                    |
|-------------------------------------------|----------------------------------------|
| TIPO DI CONTENUTO WPD \_ \_ \_ ALL                   | {80E170D2-1055-4A3E-B952-82CC4F8A8689} |
| APPUNTAMENTO CON TIPO DI CONTENUTO WPD \_ \_ \_           | {0FED060E-8793-4B1E-90C9-48AC389AC631} |
| AUDIO DEL TIPO DI CONTENUTO WPD \_ \_ \_                 | {4AD2C85E-5E2D-45E5-8864-4F229E3C6CF0} |
| ALBUM AUDIO \_ CON TIPO DI \_ \_ CONTENUTO \_ WPD          | {AA18737E-5009-48FA-AE21-85F24383B4E6} |
| CALENDARIO DEL TIPO DI CONTENUTO WPD \_ \_ \_              | {A1FD5967-6023-49A0-9DF1-F8060BE751B0} |
| CERTIFICATO DEL TIPO \_ DI CONTENUTO WPD \_ \_           | {DC3876E8-A948-4060-9050-PIÙ77E8A3D87} |
| CONTATTO DEL TIPO DI CONTENUTO WPD \_ \_ \_               | {EABA8313-4525-4707-9F0E-87C6808E9435} |
| GRUPPO DI CONTATTI \_ PER IL TIPO DI \_ \_ CONTENUTO \_ WPD        | {346B8932-4C36-40D8-9415-1828291F9DE9} |
| DOCUMENTO DEL TIPO \_ DI CONTENUTO WPD \_ \_              | {680ADF52-950A-4041-9B41-65E393648155} |
| INDIRIZZO DI POSTA ELETTRONICA \_ DEL TIPO DI \_ CONTENUTO WPD \_                 | {8038044A-7E51-4F8F-883D-1D0623D14533} |
| CARTELLA DEL TIPO \_ DI CONTENUTO WPD \_ \_                | {27E2E392-A111-48E0-AB0C-E17705A05F85} |
| OGGETTO FUNZIONALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_    | {99ED0160-17FF-4C44-9D98-1D7A6F941921} |
| FILE GENERICO DEL \_ TIPO \_ DI \_ CONTENUTO \_ WPD         | {0085E0A6-8D34-45D7-BC5C-447E59C73D48} |
| MESSAGGIO GENERICO DEL \_ TIPO \_ DI CONTENUTO \_ \_ WPD      | {E80EAAF8-B2DB-4133-B67E-1BEF4B4A6E5F} |
| IMMAGINE DEL TIPO DI \_ CONTENUTO WPD \_ \_                 | {EF2107D5-A52A-4243-A26B-62D4176D7603} |
| WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM          | {75793148-15F5-4A30-A813-54ED8A37E226} |
| CAST MULTIMEDIALE \_ DEL TIPO \_ DI \_ CONTENUTO \_ WPD           | {5E88B3CC-3E65-4E62-BFFF-229495253AB0} |
| MEMO DEL TIPO DI CONTENUTO WPD \_ \_ \_                  | {9CD20ECF-3B50-414F-A641-E473FFE45751} |
| ALBUM DI \_ CONTENUTO \_ MISTO CON TIPO DI \_ \_ CONTENUTO \_ WPD | {00F0C3AC-A593-49AC-9219-24ABCA5A2563} |
| ASSOCIAZIONE DI RETE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_  | {031DA7EE-18C8-4205-847E-89A11261D0F3} |
| PLAYLIST DEL TIPO DI CONTENUTO WPD \_ \_ \_              | {1A33F7E4-AF13-48F5-994E-77369DFE04A3} |
| PROGRAMMA DI TIPO \_ DI CONTENUTO WPD \_ \_               | {D269F96A-247C-4BFF-98FB-97F3C49220E6} |
| SEZIONE TIPO DI \_ CONTENUTO WPD \_ \_               | {821089F5-1D91-4DC9-BE3C-BBB1B35B18CE} |
| ATTIVITÀ TIPO DI CONTENUTO WPD \_ \_ \_                  | {63252F2C-887F-4CB6-B1AC-D29855DCEF6C} |
| TIPO DI CONTENUTO WPD \_ \_ \_ TV            | {60A169CF-F2AE-4E21-9375-9677F11C1C6E} |
| TIPO DI CONTENUTO WPD \_ \_ NON \_ SPECIFICATO           | {28D8D31E-249C-454E-AABC-34883168E634} |
| VIDEO SUL TIPO DI CONTENUTO WPD \_ \_ \_                 | {9261B03C-3D78-4519-85E3-02C5E1F50BB9} |
| ALBUM VIDEO \_ CON TIPO DI \_ \_ CONTENUTO \_ WPD          | {012B0DB7-D4C1-45D6-B081-94B87779614F} |
| PROFILO WIRELESS \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_     | {0BAC070A-9F5F-4DA4-A8F6-3DE44D68FD6C} |



 

Se un'applicazione supporta una determinata funzione, origine o categoria sink, inserisce una stringa che specifica il nome della chiave del gestore nel GUID che identifica la categoria funzionale o di tipo di contenuto supportata. Usando MyWpdApplication come esempio, l'applicazione creerebbe una voce in ... **Chiavi /EventHandlers/WPD/Function** o **/Sink** o **/Source.** Questa voce ha il formato "MyWpdApplicationHandler" e sarà di tipo REG \_ SZ. Inoltre, questa voce viene visualizzata sotto il GUID per le categorie funzionali o i tipi di contenuto supportati dall'applicazione.

 

 



