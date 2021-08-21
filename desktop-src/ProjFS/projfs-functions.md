---
title: Funzioni ProjFS
description: Le funzioni seguenti vengono dichiarate in projectedfslib.h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 47e4371a7d00ca6564223f7415a69ee0308bf8757041b49f5df9f214e6c978b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792608"
---
# <a name="projfs-functions"></a>Funzioni ProjFS

Le funzioni seguenti vengono dichiarate in projectedfslib.h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**PrjAllocateAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | Alloca un buffer che soddisfa i requisiti di allineamento della memoria del dispositivo di archiviazione dell'istanza di virtualizzazione. |
| [**PrjClearNegativePathCache**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | Elimina la cache dei percorsi negativi dell'istanza di virtualizzazione, se è attiva. |
| [**PrjCompleteCommand**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | Indica che il provider ha completato l'elaborazione di un callback da cui in precedenza aveva restituito HRESULT_FROM_WIN32(ERROR_IO_PENDING). |
| [**PrjDeleteFile**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | Consente a un provider di eliminare un elemento memorizzato nella cache nel file system. |
| [**PrjDoesNameContainWildCards**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | Determina se un nome contiene caratteri jolly. |
| [**PrjFileNameCompare**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | Confronta due nomi di file e restituisce un valore che indica il relativo ordine delle regole di confronto. |
| [**PrjFileNameMatch**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | Determina se un nome file corrisponde a un criterio di ricerca. |
| [**PrjFillDirEntryBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | Fornisce informazioni per un file o una directory a un'enumerazione. |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | Fornisce informazioni per un file o una directory a un'enumerazione e consente al chiamante di specificare informazioni estese. |
| [**PrjFreeAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | Libera un buffer allocato. |
| [**PrjGetOnDiskFileState**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | Ottiene lo stato del file su disco per un file o una directory. |
| [**PrjGetVirtualizationInstanceInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | Recupera informazioni sull'istanza di virtualizzazione. |
| [**PrjMarkDirectoryAsPlaceholder**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | Converte una directory esistente in un segnaposto di directory. |
| [**PrjStartVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | Configura un'istanza di Virtualizzazione ProjFS e la avvia, rendendola disponibile per l'I/O del servizio e richiamare i callback sul provider. |
| [**PrjStopVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | Arresta un'istanza di virtualizzazione ProjFS in esecuzione, rendendola non disponibile per l'I/O del servizio o per l'utilizzo di callback nel provider. |
| [**PrjUpdateFileIfNeeded**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | Consente a un provider di aggiornare un elemento memorizzato nella cache nel file system. |
| [**PrjWriteFileData**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | Invia il contenuto del file a ProjFS. |
| [**PrjWritePlaceholderInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | Invia i metadati di file o directory a ProjFS. |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | Invia i metadati di file o directory a ProjFS e consente al chiamante di specificare informazioni estese. |
