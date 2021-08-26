---
description: Creazione di oggetti sequenza temporale
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Creazione di oggetti sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c0a2a88b2cd931e6a9d12274f4a2503b4c97d52348b6ed2629c22bf204f302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054781"
---
# <a name="creating-timeline-objects"></a>Creazione di oggetti sequenza temporale

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Il codice di esempio presentato in questo articolo inizia con una sequenza temporale vuota, ma gli stessi passaggi si applicano se si carica un progetto esistente e si vogliono aggiungervi oggetti.

Per creare qualsiasi tipo di oggetto nella sequenza temporale, chiamare il [**metodo IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md) Ad esempio, il codice seguente crea un nuovo gruppo:


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



Il secondo parametro è un membro [**dell'enumerazione TIMELINE \_ MAJOR \_ TYPE.**](timeline-major-type.md) Specifica il tipo di oggetto sequenza temporale da creare, ad esempio un gruppo o una traccia.

Il **metodo CreateEmptyNode** crea l'oggetto e restituisce un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto. Incrementa anche il conteggio dei riferimenti **nell'interfaccia IAMTimelineObj,** quindi è necessario rilasciare l'interfaccia al termine dell'uso. Non chiamare la [**funzione CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Usare invece sempre **CreateEmptyNode** per creare un oggetto sequenza temporale, perché inizializza il nuovo oggetto da usare in una sequenza temporale.

[**L'interfaccia IAMTimelineObj**](iamtimelineobj.md) è un'interfaccia generica. Fornisce metodi comuni a tutti i tipi di oggetto sequenza temporale. Ogni tipo di oggetto espone anche altre interfacce. Ad esempio, i gruppi espongono [**l'interfaccia IAMTimelineGroup,**](iamtimelinegroup.md) tra gli altri. È possibile ottenere puntatori alle altre interfacce chiamando **QueryInterface.**

Dopo aver creato un oggetto, questo non fa ancora parte della sequenza temporale. Il metodo per aggiungere un oggetto alla sequenza temporale dipende dal tipo di oggetto. La sezione seguente descrive come aggiungere gruppi, composizione e tracce alla sequenza temporale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costruzione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 
