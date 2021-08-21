---
description: Registrazione del gestore del menu di scelta rapida
ms.assetid: 0023004b-b6b3-486a-8b8c-8e63c5731206
title: Registrazione del gestore del menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027e01d4b3bc58727579b77345d3f1b8eed668e5b858e49eb4859a40db9ad2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083545"
---
# <a name="registering-your-context-menu-handler"></a>Registrazione del gestore del menu di scelta rapida

Perché il gestore del menu di scelta rapida venga riconosciuto dallo spazio dei nomi WPD, è necessario registrarlo correttamente nel registro Windows dati. Le voci di registrazione per un gestore del menu di scelta rapida WPD sono simili a quelle per la shell, ma vengono registrate come tipi di file speciali. I gestori del menu di scelta rapida WPD vengono registrati in base al tipo di contenuto rappresentato. Di seguito è riportato un albero di registrazione di esempio per un gestore del menu di scelta rapida WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDContextMenu.Image
      \-- shellex
           \-- ContextMenuHandlers
                \-- ShImageViewer (Default)  REG_SZ {E847DA7C-1D6A-45F6-B725-CB260C236066}

```



L'esempio precedente registra il visualizzatore di immagini della shell con lo spazio dei nomi WPD. Quando un utente fa clic con il pulsante destro del mouse o fa doppio clic sul contenuto di un dispositivo tramite Windows Vista Shell, richiama questo gestore del menu di scelta rapida. Lo spazio dei nomi WPD usa WPD \_ CONTENT \_ TYPE per determinare i gestori del menu di scelta rapida da caricare. Se WPD CONTENT TYPE è uguale a \_ \_ WPD \_ CONTENT \_ TYPE \_ UNSPECIFIED, WPD CONTENT TYPE GENERIC FILE o \_ \_ \_ \_ WPD CONTENT TYPE PROGRAM, \_ \_ lo \_ spazio dei nomi WPD tenterà di trovare la corrispondenza migliore in base all'estensione del file selezionato. Se né l'estensione di file né il tipo di contenuto forniscono una classificazione utile, lo spazio dei nomi WPD carica i gestori del menu di scelta rapida nella chiave del Registro di sistema **WPDContextMenu.Generic.** Nella tabella seguente sono elencate tutte le classi di file disponibili per un gestore del menu di scelta rapida e i tipi di contenuto e le estensioni di file che rappresentano:



| Chiave del Registro di sistema                           | Tipo di contenuto WPD                                                                                               | Estensione nome del file                                                                                           |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **WPDContextMenu.Device**              | La registrazione in questa chiave abilita il gestore del menu di scelta rapida a livello di dispositivo. Fare clic con il pulsante destro del mouse su un dispositivo.   | (N/D)                                                                                                    |
| **WPDContextMenu. Archiviazione**             | La registrazione in questa chiave abilita il gestore del menu di scelta rapida a livello di archiviazione. Fare clic con il pulsante destro del mouse su un archivio. | (N/D)                                                                                                    |
| **WPDContextMenu.Folder**              | CARTELLA DEL TIPO \_ DI CONTENUTO WPD \_ \_                                                                                     | (N/D)                                                                                                    |
| **WPDContextMenu.Image**               | IMMAGINE DEL TIPO \_ DI CONTENUTO WPD \_ \_                                                                                      | bmp <br/> gif <br/> png <br/> jpg <br/> jpe <br/> jpeg <br/>   |
| **WPDContextMenu.Audio**               | AUDIO DEL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                      | .aiff <br/> mp3 <br/> .wav <br/> wma <br/>                                     |
| **WPDContextMenu.Video**               | VIDEO SUL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                      | .asf<br/> .avi <br/> .dvr-ms <br/> .mpeg <br/> mpg <br/> wmv <br/> |
| **WPDContextMenu.Playlist**<br/> | PLAYLIST DEL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                   | .wpl <br/> .m3u <br/> .mpl <br/> .asx <br/> file con estensione pls <br/>                     |
| **WPDContextMenu.Document**            | DOCUMENTO DEL TIPO \_ DI CONTENUTO WPD \_ \_                                                                                   | doc <br/> .txt <br/> .rtf <br/> xls <br/> ppt <br/>                     |
| **WPDContextMenu.Contact**<br/>  | CONTATTO DEL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                    | Nessuno                                                                                                     |
| **WPDContextMenu.Email**               | POSTA ELETTRONICA DEL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                      | Nessuno                                                                                                     |
| **WPDContextMenu.Appointment**         | APPUNTAMENTO CON TIPO DI CONTENUTO WPD \_ \_ \_                                                                                | Nessuno                                                                                                     |
| **WPDContextMenu.Task**                | ATTIVITÀ TIPO DI CONTENUTO WPD \_ \_ \_                                                                                       | Nessuno                                                                                                     |
| **WPDContextMenu.Memo**                | MEMO DEL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                       | Nessuno                                                                                                     |
| **WPDContextMenu.ImageAlbum**          | WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM                                                                               | Nessuno                                                                                                     |
| **WPDContextMenu.AudioAlbum**          | ALBUM AUDIO \_ CON TIPO DI \_ \_ CONTENUTO \_ WPD                                                                               | Nessuno                                                                                                     |
| **WPDContextMenu.VideoAlbum**          | ALBUM VIDEO \_ CON TIPO DI \_ \_ CONTENUTO \_ WPD                                                                               | Nessuno                                                                                                     |
| **WPDContextMenu.MixedAlbum**          | ALBUM DI \_ CONTENUTO \_ MISTO CON TIPO DI \_ \_ CONTENUTO \_ WPD                                                                      | Nessuno                                                                                                     |
| **WPDContextMenu.Generic**             | TIPO DI CONTENUTO WPD \_ \_ NON \_ SPECIFICATO                                                                                | Tutte le altre estensioni di file                                                                                |



 

 

 




