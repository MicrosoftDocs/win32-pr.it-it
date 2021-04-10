---
description: "Altre informazioni su: funzioni dell'API cabinet"
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funzioni dell'API cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877554"
---
# <a name="cabinet-api-functions"></a>Funzioni dell'API cabinet

In questa sezione vengono descritte le funzioni dell'API CAB seguenti:

## <a name="fci-functions"></a>Funzioni FCI

La libreria FCI (file compression Interface) offre la possibilità di creare armadi (noti anche come "file CAB"). Inoltre, la libreria fornisce la compressione per ridurre le dimensioni dei dati dei file archiviati nei file CAB.



| Funzione                                   | Descrizione                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Aggiunge un file al file CAB attualmente in fase di contructed.<br/>                                           |
| [**FCICreate**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Crea un contesto dell'istanza del cluster di failover.<br/>                                                                          |
| [**FCIDestroy**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Elimina un contesto FCI aperto, liberando tutti i file di memoria e temporanei associati al contesto.<br/> |
| [**FCIFlushCabinet**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Completa il file CAB corrente.<br/>                                                                   |
| [**FCIFlushFolder**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Impone il completamento immediato della cartella corrente in costruzione.<br/>                        |



 

## <a name="fdi-functions"></a>Funzioni IDE

La libreria IDE (file Decompression Interface) offre la possibilità di estrarre i file dai file CAB.



| Funzione                                         | Descrizione                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**FDICopy**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Estrae i file dai file CAB.<br/>                                                          |
| [**FDICreate**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Crea un contesto IDE.<br/>                                                                |
| [**FDIDestroy**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Elimina un contesto IDE aperto.<br/>                                                           |
| [**FDIIsCabinet**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Determina se un file è un file CAB e, in caso contrario, restituisce informazioni descrittive.<br/> |
| [**FDITruncateCabinet**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Tronca un file CAB a partire dal numero di cartella specificato.<br/>                      |



 

## <a name="deprecated-functions"></a>Funzioni deprecate

-   [**DeleteExtractedFiles**](deleteextractedfiles.md)
-   [**DllGetVersion**](dllgetversion.md)
-   [**Estrarre**](extract.md)
-   [**GetDllVersion**](getdllversion.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'API cabinet](cabinet-api-reference.md)
</dt> <dt>

[Uso dell'API cabinet](using-the-cabinet-api.md)
</dt> </dl>

 

 




