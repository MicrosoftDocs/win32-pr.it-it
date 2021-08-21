---
description: "Altre informazioni su: Funzioni dell'API Cabinet"
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funzioni dell'API Cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b08234a47c84a604c78275632d88be2bcdeef68e47fd092bbf50e4d97dcf925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668355"
---
# <a name="cabinet-api-functions"></a>Funzioni dell'API Cabinet

In questa sezione vengono descritte le funzioni dell'API Cabinet seguenti:

## <a name="fci-functions"></a>Funzioni FCI

La libreria FCI (File Compression Interface) consente di creare file CAB (noti anche come "file CAB"). Inoltre, la libreria fornisce la compressione per ridurre le dimensioni dei dati dei file archiviati in archivi.



| Funzione                                   | Descrizione                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Aggiunge un file all'archivio attualmente in fase di esecuzione.<br/>                                           |
| [**FCICrea**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Crea un contesto FCI.<br/>                                                                          |
| [**FCIDestroy**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Elimina un contesto FCI aperto, liberando la memoria e i file temporanei associati al contesto.<br/> |
| [**FCIFlushCabinet**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Completa l'archivio corrente.<br/>                                                                   |
| [**FCIFlushFolder**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Forza il completamento immediato della cartella corrente in corso di costruzione.<br/>                        |



 

## <a name="fdi-functions"></a>Funzioni FDI

La libreria FDI (File Decompression Interface) consente di estrarre file da archivi.



| Funzione                                         | Descrizione                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**FDICopy**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Estrae i file dai file cab.<br/>                                                          |
| [**FDICrea**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Crea un contesto FDI.<br/>                                                                |
| [**FDIDestroy**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Elimina un contesto FDI aperto.<br/>                                                           |
| [**FDIIsCabinet**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Determina se un file è un file cab e, in caso contrario, restituisce informazioni descrittive.<br/> |
| [**FDITruncateCabinet**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Tronca un file CAB a partire dal numero di cartella specificato.<br/>                      |



 

## <a name="deprecated-functions"></a>Funzioni deprecate

-   [**DeleteExtractedFiles**](deleteextractedfiles.md)
-   [**DllGetVersion**](dllgetversion.md)
-   [**Estrazione**](extract.md)
-   [**GetDllVersion**](getdllversion.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API cabinet](cabinet-api-reference.md)
</dt> <dt>

[Uso dell'API Cabinet](using-the-cabinet-api.md)
</dt> </dl>

 

 




