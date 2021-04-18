---
title: Funzioni ProjFS
description: Le funzioni seguenti sono dichiarate in projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 40f3f2aec8e52d2caafdcf1554d0871e9bb185de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300847"
---
# <a name="projfs-functions"></a>Funzioni ProjFS

Le funzioni seguenti sono dichiarate in projectedfslib. h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**PrjAllocateAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | Alloca un buffer che soddisfa i requisiti di allineamento della memoria del dispositivo di archiviazione dell'istanza di virtualizzazione. |
| [**PrjClearNegativePathCache**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | Elimina la cache dei percorsi negativi dell'istanza di virtualizzazione, se è attiva. |
| [**PrjCompleteCommand**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | Indica che il provider ha completato l'elaborazione di un callback dal quale era stato restituito in precedenza HRESULT_FROM_WIN32 (ERROR_IO_PENDING). |
| [**PrjDeleteFile**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | Consente a un provider di eliminare un elemento memorizzato nella cache nella file system locale. |
| [**PrjDoesNameContainWildCards**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | Determina se un nome contiene caratteri jolly. |
| [**PrjFileNameCompare**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | Confronta due nomi di file e restituisce un valore che indica l'ordine delle regole di confronto relativo. |
| [**PrjFileNameMatch**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | Determina se un nome di file corrisponde a un criterio di ricerca. |
| [**PrjFillDirEntryBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | Fornisce informazioni per un file o una directory a un'enumerazione. |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | Fornisce informazioni per un file o una directory a un'enumerazione e consente al chiamante di specificare le informazioni estese. |
| [**PrjFreeAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | Libera un buffer allocato. |
| [**PrjGetOnDiskFileState**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | Ottiene lo stato del file su disco per un file o una directory. |
| [**PrjGetVirtualizationInstanceInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | Recupera le informazioni sull'istanza di virtualizzazione. |
| [**PrjMarkDirectoryAsPlaceholder**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | Converte una directory esistente in un segnaposto di directory. |
| [**PrjStartVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | Configura un'istanza di virtualizzazione ProjFS e la avvia, rendendola disponibile per l'I/O del servizio e richiama i callback sul provider. |
| [**PrjStopVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | Arresta un'istanza di virtualizzazione ProjFS in esecuzione, rendendola non disponibile per l'I/O del servizio o implicare callback sul provider. |
| [**PrjUpdateFileIfNeeded**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | Consente a un provider di aggiornare un elemento memorizzato nella cache del file system locale. |
| [**PrjWriteFileData**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | Invia il contenuto del file a ProjFS. |
| [**PrjWritePlaceholderInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | Invia i metadati di file o directory a ProjFS. |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | Invia i metadati di file o directory a ProjFS e consente al chiamante di specificare le informazioni estese. |
