---
description: Registrazione del gestore del menu di scelta rapida
ms.assetid: 0023004b-b6b3-486a-8b8c-8e63c5731206
title: Registrazione del gestore del menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafd2798683b4bc291653bca34996f143fc36842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314441"
---
# <a name="registering-your-context-menu-handler"></a>Registrazione del gestore del menu di scelta rapida

Affinché il gestore del menu di scelta rapida venga riconosciuto dallo spazio dei nomi WPD, è necessario registrarlo correttamente nel registro di sistema di Windows. Le voci di registrazione per un gestore di menu di scelta rapida WPD sono simili a quelle della shell, ma sono registrate come tipi di file speciali. I gestori dei menu di scelta rapida WPD vengono registrati in base al tipo di contenuto che rappresentano. Di seguito è riportato un esempio di albero di registrazione per un gestore menu di scelta rapida WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDContextMenu.Image
      \-- shellex
           \-- ContextMenuHandlers
                \-- ShImageViewer (Default)  REG_SZ {E847DA7C-1D6A-45F6-B725-CB260C236066}

```



Nell'esempio precedente viene registrato il Visualizzatore di immagini della shell con lo spazio dei nomi WPD. Quando un utente fa clic con il pulsante destro del mouse o fa doppio clic sul contenuto di un dispositivo tramite la shell di Windows Vista, richiama questo gestore del menu di scelta rapida. Lo spazio dei nomi WPD usa il \_ \_ tipo di contenuto WPD per determinare quali gestori di menu di scelta rapida caricare. Se il tipo di contenuto WPD \_ \_ è uguale al tipo di contenuto WPD non \_ \_ \_ specificato, il tipo di contenuto WPD è un \_ \_ \_ \_ file generico o \_ \_ un tipo di contenuto WPD \_ , lo spazio dei nomi WPD tenterà di trovare la migliore corrispondenza in base all'estensione del file selezionato. Se né l'estensione di file né il tipo di contenuto forniscono una classificazione utile, lo spazio dei nomi WPD caricherà i gestori del menu di scelta rapida sotto la chiave del registro di sistema **WPDContextMenu. Generic** . Nella tabella seguente sono elencate tutte le classi di file disponibili per un gestore di menu di scelta rapida e i tipi di contenuto e le estensioni di file che rappresentano:



| Chiave del Registro di sistema                           | Tipo di contenuto WPD                                                                                               | Estensione nome del file                                                                                           |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **WPDContextMenu. Device**              | La registrazione in questa chiave Abilita il gestore del menu di scelta rapida a livello di dispositivo. (Fare clic con il pulsante destro del mouse su un dispositivo).   | (N/D)                                                                                                    |
| **WPDContextMenu. storage**             | La registrazione in questa chiave Abilita il gestore del menu di scelta rapida a livello di archiviazione. Fare clic con il pulsante destro del mouse su una risorsa di archiviazione. | (N/D)                                                                                                    |
| **WPDContextMenu. Folder**              | \_cartella del \_ tipo di contenuto WPD \_                                                                                     | (N/D)                                                                                                    |
| **WPDContextMenu. image**               | \_immagine del \_ tipo di contenuto WPD \_                                                                                      | bmp <br/> gif <br/> png <br/> jpg <br/> jpe <br/> jpeg <br/>   |
| **WPDContextMenu. audio**               | \_audio del \_ tipo di contenuto WPD \_                                                                                      | .aiff <br/> mp3 <br/> .wav <br/> wma <br/>                                     |
| **WPDContextMenu. video**               | \_video del \_ tipo di contenuto WPD \_                                                                                      | .asf<br/> .avi <br/> DVR-MS <br/> . MPEG <br/> mpg <br/> wmv <br/> |
| **WPDContextMenu. playlist**<br/> | \_playlist del \_ tipo di contenuto WPD \_                                                                                   | . WPL <br/> .m3u <br/> . MPL <br/> .asx <br/> . pls <br/>                     |
| **WPDContextMenu.Document**            | \_documento del \_ tipo di contenuto WPD \_                                                                                   | doc <br/> .txt <br/> .rtf <br/> xls <br/> ppt <br/>                     |
| **WPDContextMenu. Contact**<br/>  | \_ \_ contatto tipo di contenuto WPD \_                                                                                    | nessuno                                                                                                     |
| **WPDContextMenu.Email**               | \_indirizzo di \_ \_ posta elettronica del tipo di contenuto WPD                                                                                      | nessuno                                                                                                     |
| **WPDContextMenu. appuntamento**         | \_ \_ appuntamento tipo di contenuto WPD \_                                                                                | nessuno                                                                                                     |
| **WPDContextMenu. Task**                | \_ \_ attività tipo di contenuto WPD \_                                                                                       | nessuno                                                                                                     |
| **WPDContextMenu. memo**                | \_Memo del \_ tipo di contenuto WPD \_                                                                                       | nessuno                                                                                                     |
| **WPDContextMenu.ImageAlbum**          | \_album di \_ Immagini del tipo di contenuto WPD \_ \_                                                                               | nessuno                                                                                                     |
| **WPDContextMenu.AudioAlbum**          | \_ \_ album audio del tipo di contenuto WPD \_ \_                                                                               | nessuno                                                                                                     |
| **WPDContextMenu.VideoAlbum**          | \_ \_ album video del tipo di contenuto WPD \_ \_                                                                               | nessuno                                                                                                     |
| **WPDContextMenu.MixedAlbum**          | \_album di \_ contenuto \_ misto \_ tipo \_ di contenuto WPD                                                                      | nessuno                                                                                                     |
| **WPDContextMenu. Generic**             | tipo di contenuto WPD non \_ \_ \_ specificato                                                                                | Tutte le altre estensioni di file                                                                                |



 

 

 




