---
description: Supporto di AutoPlay
ms.assetid: e91334d9-9041-4cb8-a6d0-0e2371800064
title: Supporto di AutoPlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467a4f6289492177beab0469a181297b13accfce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758456"
---
# <a name="supporting-autoplay"></a>Supporto di AutoPlay

AutoPlay è una funzionalità della shell che avvia applicazioni associate a dispositivi specifici. A seconda delle impostazioni di AutoPlay correnti, questa funzionalità eseguirà una delle diverse azioni, ad esempio la presentazione di un elenco di applicazioni di gestione disponibili, la visualizzazione di una visualizzazione cartella standard dei file e così via.

In Windows Vista, la funzionalità AutoPlay è stata estesa in modo che un dispositivo WPD possa fornire un elenco di tipi di contenuto supportati. Analogamente, le applicazioni WPD possono registrare i tipi di contenuto supportati. Ad esempio, un'acquisizione guidata foto può essere registrata come gestore per qualsiasi dispositivo WPD che fornisce immagini e un'applicazione multimediale può registrarsi come gestore per qualsiasi dispositivo che archivia file audio o video.

Le applicazioni registrano le informazioni specifiche del gestore scrivendo le voci nella chiave **HKEY del \_ \_ software del computer locale \\ \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\** . Usando un gestore dell'applicazione WPD (denominato MyWpdApplication.exe) come esempio, l'applicazione può inserire i valori seguenti in una chiave **\\ \\ MyWpdApplicationHandler dei gestori** .



| Valore          | Tipo            | Data                                                 |
|----------------|-----------------|------------------------------------------------------|
| Azione         | REG \_ SZ         | Esplorare il contenuto nei dispositivi portatili.                  |
| CLSIDForCancel | REG \_ SZ         | {00000000-0000-0000-0000-000000000000}               |
| DefaultIcon    | REG \_ Espandi \_ SZ | % SystemDrive% \\ Multimedia \\ WPD \\MyWpdApplication.exe |
| InitCmdLine    | REG \_ SZ         | /AutoPlay                                            |
| ProgID         | REG \_ SZ         | MyWpdApplication.MyWpdApplicationAutoPlay            |
| Provider       | REG \_ SZ         | MyWpdApplication                                     |



 

Per ulteriori informazioni sulle chiavi del registro di sistema AutoPlay e sui valori disponibili nel **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ Handlers** Key, vedere la documentazione corrispondente su MSDN.

### <a name="the-wpd-autoplay-scheme"></a>Schema AutoPlay WPD

Lo schema WPD AutoPlay si integra con la funzionalità AutoPlay di Windows Vista. Supporta tre categorie AutoPlay, descritte nella tabella seguente.



| Category | Descrizione                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------|
| Source (Sorgente)   | Un dispositivo WPD può essere considerato come un'origine di contenuto, ovvero è possibile trasferire il contenuto dal dispositivo.        |
| Sink     | Un dispositivo WPD può essere considerato come una destinazione per il contenuto, ovvero è possibile trasferire il contenuto al dispositivo.    |
| Funzione | Un dispositivo WPD supporta una funzionalità programmabile o controllabile (ad esempio, può inviare e ricevere messaggi SMS). |



 

Le applicazioni si registrano per la categoria di origine, sink e/o funzione appropriata scrivendo le voci nella sezione AutoPlay del registro di sistema. Queste voci vengono visualizzate in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ EventHandlers \\ WPD** Key. Nella chiave WPD sono incluse la **funzione**, il **sink** e le chiavi di **origine** . In ognuna di queste chiavi è presente un GUID che corrisponde a una categoria funzionale o a un tipo di contenuto WPD.

La tabella seguente elenca i GUID disponibili sotto la chiave **Function** nel registro di sistema e identifica la categoria funzionale che corrisponde a ogni GUID.



| Categoria funzionale WPD                           | Chiave del registro di sistema (GUID)                    |
|---------------------------------------------------|----------------------------------------|
| \_categoria funzionale \_ WPD \_ All                    | {2D8A6512-A74C-448E-BA8A-F4AC07C49399} |
| \_ \_ acquisizione audio della categoria funzionale \_ WPD \_         | {3F2A1919-C7C2-4A00-855D-F57CF06DEBBB} |
| \_ \_ dispositivo categoria funzionale \_ WPD                 | {08EA466B-E3A4-4336-A1F3-A44D2B5C438C} |
| \_configurazione di \_ rete della categoria funzionale \_ WPD \_ | {48F4DB72-7C6A-4AB0-9E1A-470E3CDBF26A} |
| \_ \_ \_ informazioni sul rendering della categoria funzionale WPD \_ | {08600BA4-A7BA-4A01-AB0E-0065D0A356D3} |
| \_SMS della \_ categoria \_ funzionale WPD                    | {0044A0B1-C1E9-4AFD-B358-A62C6117C9CF} |
| \_ \_ \_ \_ acquisizione immagini ancora della categoria funzionale WPD \_  | {613CA327-AB93-4900-B4FA-895BB5874B79} |
| \_ \_ archiviazione categoria funzionale \_ WPD                | {23F05BBC-15DE-4C2A-A55B-A9AF5CE412EF} |
| \_ \_ acquisizione video della categoria funzionale \_ WPD \_         | {E23E5F6B-7243-43AA-8DF1-0EB3D968A918} |



 

Nella tabella seguente sono elencati i GUID disponibili sotto il **sink** e le chiavi di **origine** nel registro di sistema e viene identificato il tipo di contenuto corrispondente a ogni GUID.



| Tipo di contenuto WPD                          | Chiave del registro di sistema (GUID)                    |
|-------------------------------------------|----------------------------------------|
| \_tipo di contenuto WPD \_ \_ All                   | {80E170D2-1055-4A3E-B952-82CC4F8A8689} |
| \_ \_ appuntamento tipo di contenuto WPD \_           | {0FED060E-8793-4B1E-90C9-48AC389AC631} |
| \_audio del \_ tipo di contenuto WPD \_                 | {4AD2C85E-5E2D-45E5-8864-4F229E3C6CF0} |
| \_ \_ album audio del tipo di contenuto WPD \_ \_          | {AA18737E-5009-48FA-AE21-85F24383B4E6} |
| \_ \_ Calendario tipo di contenuto WPD \_              | {A1FD5967-6023-49A0-9DF1-F8060BE751B0} |
| \_certificato del \_ tipo di contenuto WPD \_           | {DC3876E8-A948-4060-9050-CBD77E8A3D87} |
| \_ \_ contatto tipo di contenuto WPD \_               | {EABA8313-4525-4707-9F0E-87C6808E9435} |
| \_gruppo di \_ contatti del tipo di contenuto WPD \_ \_        | {346B8932-4C36-40D8-9415-1828291F9DE9} |
| \_documento del \_ tipo di contenuto WPD \_              | {680ADF52-950A-4041-9B41-65E393648155} |
| \_indirizzo di \_ \_ posta elettronica del tipo di contenuto WPD                 | {8038044A-7E51-4F8F-883D-1D0623D14533} |
| \_cartella del \_ tipo di contenuto WPD \_                | {27E2E392-A111-48E0-AB0C-E17705A05F85} |
| \_ \_ oggetto funzionale del tipo di contenuto WPD \_ \_    | {99ED0160-17FF-4C44-9D98-1D7A6F941921} |
| \_ \_ file generico di tipo di contenuto WPD \_ \_         | {0085E0A6-8D34-45D7-BC5C-447E59C73D48} |
| \_ \_ messaggio generico di tipo di contenuto WPD \_ \_      | {E80EAAF8-B2DB-4133-B67E-1BEF4B4A6E5F} |
| \_immagine del \_ tipo di contenuto WPD \_                 | {EF2107D5-A52A-4243-A26B-62D4176D7603} |
| \_album di \_ Immagini del tipo di contenuto WPD \_ \_          | {75793148-15F5-4A30-A813-54ED8A37E226} |
| \_cast del \_ supporto del tipo di contenuto WPD \_ \_           | {5E88B3CC-3E65-4E62-BFFF-229495253AB0} |
| \_Memo del \_ tipo di contenuto WPD \_                  | {9CD20ECF-3B50-414F-A641-E473FFE45751} |
| \_album di \_ contenuto \_ misto \_ tipo \_ di contenuto WPD | {00F0C3AC-A593-49AC-9219-24ABCA5A2563} |
| \_associazione di \_ rete del tipo di contenuto WPD \_ \_  | {031DA7EE-18C8-4205-847E-89A11261D0F3} |
| \_playlist del \_ tipo di contenuto WPD \_              | {1A33F7E4-AF13-48F5-994E-77369DFE04A3} |
| \_ \_ programma tipo di contenuto WPD \_               | {D269F96A-247C-4BFF-98FB-97F3C49220E6} |
| \_sezione del \_ tipo di contenuto WPD \_               | {821089F5-1D91-4DC9-BE3C-BBB1B35B18CE} |
| \_ \_ attività tipo di contenuto WPD \_                  | {63252F2C-887F-4CB6-B1AC-D29855DCEF6C} |
| \_televisione del \_ tipo di contenuto WPD \_            | {60A169CF-F2AE-4E21-9375-9677F11C1C6E} |
| tipo di contenuto WPD non \_ \_ \_ specificato           | {28D8D31E-249C-454E-AABC-34883168E634} |
| \_video del \_ tipo di contenuto WPD \_                 | {9261B03C-3D78-4519-85E3-02C5E1F50BB9} |
| \_ \_ album video del tipo di contenuto WPD \_ \_          | {012B0DB7-D4C1-45D6-B081-94B87779614F} |
| \_ \_ profilo wireless del tipo di contenuto WPD \_ \_     | {0BAC070A-9F5F-4DA4-A8F6-3DE44D68FD6C} |



 

Se un'applicazione supporta una determinata funzione, origine o categoria di sink, inserisce una stringa che specifica il nome della chiave del gestore sotto il GUID che ha identificato la categoria funzionale o Content-Type supportata. Usando MyWpdApplication come esempio, l'applicazione crea una voce sotto... Chiavi **/EventHandlers/WPD/Function**, **/sink** o **/source** . Questa voce avrebbe il formato "MyWpdApplicationHandler" ed essere di tipo REG \_ SZ. Inoltre, questa voce viene visualizzata sotto il GUID per le categorie funzionali o i tipi di contenuto supportati dall'applicazione.

 

 



