---
description: Registrazione del gestore della finestra delle proprietà
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: Registrazione del gestore della finestra delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f1642c03a068a24b37cd5647bcdef63222ed2dbe5d78832daeea31e8abd67d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083535"
---
# <a name="registering-your-property-sheet-handler"></a>Registrazione del gestore della finestra delle proprietà

Perché il gestore della finestra delle proprietà venga riconosciuto dallo spazio dei nomi WPD, è necessario registrarlo correttamente nel registro Windows proprietà. Le voci di registrazione per un gestore della finestra delle proprietà WPD sono simili a quelle per la shell, ma vengono registrate come tipi di file speciali. I gestori della finestra delle proprietà WPD vengono registrati in base al tipo di contenuto rappresentato. Di seguito è riportato un albero di registrazione di esempio per un gestore del menu di scelta rapida WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



Nell'esempio precedente viene registrato un gestore personalizzato con lo spazio dei nomi WPD. Quando un utente fa clic con il pulsante destro del mouse su un file di immagine in un dispositivo tramite Windows Shell e seleziona Proprietà **,** richiama questo gestore della finestra delle proprietà. Lo spazio dei nomi WPD usa il tipo di contenuto WPD per determinare quali gestori \_ della finestra delle proprietà \_ caricare. Se il tipo di contenuto non fornisce una classificazione utile, lo spazio dei nomi carica i gestori della finestra delle proprietà nella chiave del Registro di sistema **WPDPropSheet.Generic.** Nella tabella seguente sono elencate tutte le classi di file disponibili per un gestore del menu di scelta rapida e i tipi di contenuto e le estensioni di file che rappresentano.



| Chiave del Registro di sistema                   | Tipo di contenuto WPD                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPDContextMenu.Device**      | La registrazione in questa chiave abilita il gestore del menu di scelta rapida a livello di dispositivo. Fare clic con il pulsante destro del mouse su un dispositivo.                   |
| **WPDContextMenu. Archiviazione**     | La registrazione in questa chiave abilita il gestore del menu di scelta rapida a livello di archiviazione. Fare clic con il pulsante destro del mouse su un archivio.                 |
| **WPDContextMenu.Folder**      | CARTELLA DEL TIPO \_ DI CONTENUTO WPD \_ \_                                                                                                     |
| **WPDContextMenu.Image**       | IMMAGINE DEL TIPO \_ DI CONTENUTO WPD \_ \_                                                                                                      |
| **WPDContextMenu.Audio**       | AUDIO DEL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                                      |
| **WPDContextMenu.Video**       | VIDEO SUL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                                      |
| **WPDContextMenu.Playlist**    | PLAYLIST DEL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                                   |
| **WPDContextMenu.Document**    | DOCUMENTO DEL TIPO \_ DI CONTENUTO WPD \_ \_                                                                                                   |
| **WPDContextMenu.Contact**     | CONTATTO DEL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                                    |
| **WPDContextMenu.Email**       | MESSAGGIO DI POSTA ELETTRONICA \_ DEL TIPO DI CONTENUTO WPD \_ \_                                                                                                      |
| **WPDContextMenu.Appointment** | APPUNTAMENTO CON TIPO DI CONTENUTO WPD \_ \_ \_                                                                                                |
| **WPDContextMenu.Task**        | ATTIVITÀ TIPO DI CONTENUTO WPD \_ \_ \_                                                                                                       |
| **WPDContextMenu.Memo**        | MEMO DEL TIPO DI CONTENUTO WPD \_ \_ \_                                                                                                       |
| **WPDContextMenu.ImageAlbum**  | WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM                                                                                               |
| **WPDContextMenu.AudioAlbum**  | ALBUM AUDIO \_ CON TIPO DI \_ \_ CONTENUTO \_ WPD                                                                                               |
| **WPDContextMenu.VideoAlbum**  | ALBUM VIDEO \_ CON TIPO DI \_ \_ CONTENUTO \_ WPD                                                                                               |
| **WPDContextMenu.MixedAlbum**  | ALBUM DI \_ CONTENUTO \_ MISTO CON TIPO DI \_ \_ CONTENUTO \_ WPD                                                                                      |
| **WPDContextMenu.Generic**     | TIPO DI CONTENUTO WPD \_ \_ NON \_ SPECIFICATO<br/> FILE GENERICO DEL \_ TIPO DI \_ CONTENUTO \_ WPD \_<br/> PROGRAMMA DI TIPO \_ DI CONTENUTO WPD \_ \_<br/> |



 

 

 




