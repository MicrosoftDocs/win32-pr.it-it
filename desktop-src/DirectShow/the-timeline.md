---
description: Sequenza temporale
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f298c2649a280bf5fd622d5fb5a2aef820d1f340d45f7e2beb83fe9edd6a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050001"
---
# <a name="the-timeline"></a>Sequenza temporale

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

La sequenza temporale espone [**l'interfaccia IAMTimeline.**](iamtimeline.md) Questa interfaccia contiene metodi per l'impostazione delle proprietà nella sequenza temporale. per l'aggiunta di gruppi alla sequenza temporale; e per la creazione di oggetti sequenza temporale, ad esempio gruppi, tracce e origini. Per creare una nuova sequenza temporale, chiamare la funzione **CoCreateInstance** standard come indicato di seguito:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



La nuova sequenza temporale è vuota. A questo punto è possibile caricare un file di progetto esistente (vedere Caricamento e anteprima di un [Project)](loading-and-previewing-a-project.md)o creare la sequenza temporale creando e inserendo nuovi oggetti (vedere Costruzione di una sequenza [temporale).](constructing-a-timeline.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dei componenti della sequenza temporale](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



