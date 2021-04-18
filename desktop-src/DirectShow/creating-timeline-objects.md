---
description: Creazione di oggetti Timeline
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Creazione di oggetti Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303782"
---
# <a name="creating-timeline-objects"></a>Creazione di oggetti Timeline

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Il codice di esempio presentato in questo articolo inizia con una sequenza temporale vuota, ma gli stessi passaggi si applicano se si carica un progetto esistente e si desidera aggiungervi oggetti.

Per creare qualsiasi tipo di oggetto nella sequenza temporale, chiamare il metodo [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) . Il codice seguente, ad esempio, consente di creare un nuovo gruppo:


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



Il secondo parametro è un membro dell'enumerazione [**di \_ \_ tipo principale della sequenza temporale**](timeline-major-type.md) . Specifica il tipo di oggetto sequenza temporale da creare, ad esempio un gruppo o una traccia.

Il metodo **CreateEmptyNode** crea l'oggetto e restituisce un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto. Incrementa inoltre il conteggio dei riferimenti sull'interfaccia **IAMTimelineObj** , pertanto è necessario rilasciare l'interfaccia al termine dell'utilizzo. Non chiamare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) . Usare invece sempre **CreateEmptyNode** per creare un oggetto sequenza temporale, perché Inizializza il nuovo oggetto per l'uso in una sequenza temporale.

L'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) è un'interfaccia generica. Fornisce metodi comuni a tutti i tipi di oggetto sequenza temporale. Ogni tipo di oggetto espone anche altre interfacce. Ad esempio, i gruppi espongono l'interfaccia [**IAMTimelineGroup**](iamtimelinegroup.md) , tra gli altri. È possibile ottenere i puntatori alle altre interfacce chiamando **QueryInterface**.

Dopo aver creato un oggetto, non fa ancora parte della sequenza temporale. Il metodo per aggiungere un oggetto alla sequenza temporale dipende dal tipo di oggetto. Nella sezione seguente viene descritto come aggiungere gruppi, composizioni e tracce alla sequenza temporale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 
