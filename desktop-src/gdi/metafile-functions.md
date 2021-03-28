---
description: Le funzioni seguenti vengono usate con i metafile in formato avanzato.
ms.assetid: 93a17a8c-308b-4442-933e-fedc8b9a84b0
title: Funzioni metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd137095fe0659871291ec4e8670054cc2899d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528315"
---
# <a name="metafile-functions"></a>Funzioni metafile

Le funzioni seguenti vengono usate con i metafile in formato avanzato.



| Funzione                                                             | Descrizione                                                                                                            |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile)                         | Chiude un contesto di dispositivo Enhanced Metafile.                                                                            |
| [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea)                           | Copia il contenuto di un metafile con formato avanzato in un file specificato.                                                |
| [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)                       | Crea un contesto di dispositivo per un metafile in formato avanzato.                                                              |
| [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)                       | Elimina un metafile in formato avanzato o un handle del metafile in formato avanzato.                                             |
| [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)                           | Funzione di callback definita dall'applicazione utilizzata con la funzione EnumEnhMetaFile.                                       |
| [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile)                           | Enumera i record all'interno di un metafile con formato avanzato.                                                             |
| [**GdiComment**](/windows/desktop/api/Wingdi/nf-wingdi-gdicomment)                                     | Copia un commento da un buffer in un metafile del formato avanzato specificato.                                              |
| [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea)                             | Crea un handle che identifica il metafile in formato avanzato archiviato nel file specificato.                            |
| [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits)                     | Recupera il contenuto del metafile del formato avanzato specificato e lo copia in un buffer.                        |
| [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)       | Recupera una descrizione di testo facoltativa da un metafile in formato avanzato e copia la stringa nel buffer specificato. |
| [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader)                 | Recupera il record contenente l'intestazione per il metafile del formato avanzato specificato.                                 |
| [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) | Recupera le voci della tavolozza facoltative dal metafile avanzato specificato.                                               |
| [**GetMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilea)                                   | GetMetaFile non è più disponibile per l'uso a partire da Windows 2000. Usare invece [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea).  |
| [**GetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getwinmetafilebits)                     | Converte i record in formato avanzato da un metafile in record in formato Windows.                                      |
| [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile)                           | Visualizza l'immagine archiviata nel metafile del formato avanzato specificato.                                                 |
| [**PlayEnhMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafilerecord)               | Riproduce un record Enhanced-Metafile eseguendo le funzioni GDI (Graphics Device Interface) identificate dal record. |
| [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)                     | Crea un metafile in formato avanzato basato sulla memoria dai dati specificati.                                               |
| [**SetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setwinmetafilebits)                     | Converte un metafile dal formato Windows precedente al nuovo formato migliorato.                                          |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

Le funzioni seguenti sono obsolete. Sono forniti per la compatibilità con i file di formato di Windows.

-   [**CloseMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closemetafile)
-   [**CopyMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copymetafilea)
-   [**CreateMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createmetafilea)
-   [**DeleteMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deletemetafile)
-   [**EnumMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enummetafile)
-   [**EnumMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-mfenumproc)
-   [**GetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilebitsex)
-   [**PlayMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafile)
-   [**PlayMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafilerecord)
-   [**SetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-setmetafilebitsex)

 

 
