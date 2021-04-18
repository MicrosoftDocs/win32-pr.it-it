---
description: Registrazione del gestore della finestra delle proprietà
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: Registrazione del gestore della finestra delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a59a03ebd13f5a541674012da7b07045e0a510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314440"
---
# <a name="registering-your-property-sheet-handler"></a>Registrazione del gestore della finestra delle proprietà

Affinché il gestore della finestra delle proprietà venga riconosciuto dallo spazio dei nomi WPD, è necessario registrarlo correttamente nel registro di sistema di Windows. Le voci di registrazione per un gestore della finestra delle proprietà di WPD sono simili a quelle della shell, ma sono registrate come tipi di file speciali. I gestori della finestra delle proprietà di WPD vengono registrati in base al tipo di contenuto che rappresentano. Di seguito è riportato un esempio di albero di registrazione per un gestore menu di scelta rapida WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



Nell'esempio precedente viene registrato un gestore personalizzato con lo spazio dei nomi WPD. Quando un utente fa clic con il pulsante destro del mouse su un file di immagine in un dispositivo tramite la shell di Windows e seleziona **Proprietà**, richiama questo gestore della finestra delle proprietà. Lo spazio dei nomi WPD USA \_ il \_ tipo di contenuto WPD per determinare quali gestori della finestra delle proprietà caricare. Se il tipo di contenuto non fornisce una classificazione utile, lo spazio dei nomi caricherà i gestori della finestra delle proprietà sotto la chiave **del registro di sistema WPDPropSheet. Generic** . Nella tabella seguente sono elencate tutte le classi di file disponibili per un gestore di menu di scelta rapida e i tipi di contenuto e le estensioni di file che rappresentano.



| Chiave del Registro di sistema                   | Tipo di contenuto WPD                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPDContextMenu. Device**      | La registrazione in questa chiave Abilita il gestore del menu di scelta rapida a livello di dispositivo. (Fare clic con il pulsante destro del mouse su un dispositivo).                   |
| **WPDContextMenu. storage**     | La registrazione in questa chiave Abilita il gestore del menu di scelta rapida a livello di archiviazione. Fare clic con il pulsante destro del mouse su una risorsa di archiviazione.                 |
| **WPDContextMenu. Folder**      | \_cartella del \_ tipo di contenuto WPD \_                                                                                                     |
| **WPDContextMenu. image**       | \_immagine del \_ tipo di contenuto WPD \_                                                                                                      |
| **WPDContextMenu. audio**       | \_audio del \_ tipo di contenuto WPD \_                                                                                                      |
| **WPDContextMenu. video**       | \_video del \_ tipo di contenuto WPD \_                                                                                                      |
| **WPDContextMenu. playlist**    | \_playlist del \_ tipo di contenuto WPD \_                                                                                                   |
| **WPDContextMenu.Document**    | \_documento del \_ tipo di contenuto WPD \_                                                                                                   |
| **WPDContextMenu. Contact**     | \_ \_ contatto tipo di contenuto WPD \_                                                                                                    |
| **WPDContextMenu.Email**       | \_indirizzo di \_ \_ posta elettronica del tipo di contenuto WPD                                                                                                      |
| **WPDContextMenu. appuntamento** | \_ \_ appuntamento tipo di contenuto WPD \_                                                                                                |
| **WPDContextMenu. Task**        | \_ \_ attività tipo di contenuto WPD \_                                                                                                       |
| **WPDContextMenu. memo**        | \_Memo del \_ tipo di contenuto WPD \_                                                                                                       |
| **WPDContextMenu.ImageAlbum**  | \_album di \_ Immagini del tipo di contenuto WPD \_ \_                                                                                               |
| **WPDContextMenu.AudioAlbum**  | \_ \_ album audio del tipo di contenuto WPD \_ \_                                                                                               |
| **WPDContextMenu.VideoAlbum**  | \_ \_ album video del tipo di contenuto WPD \_ \_                                                                                               |
| **WPDContextMenu.MixedAlbum**  | \_album di \_ contenuto \_ misto \_ tipo \_ di contenuto WPD                                                                                      |
| **WPDContextMenu. Generic**     | tipo di contenuto WPD non \_ \_ \_ specificato<br/> \_ \_ file generico di tipo di contenuto WPD \_ \_<br/> \_ \_ programma tipo di contenuto WPD \_<br/> |



 

 

 




