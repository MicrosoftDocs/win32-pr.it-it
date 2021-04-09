---
description: Creazione di una ridisposizione video personalizzata
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Creazione di una ridisposizione video personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124107"
---
# <a name="providing-a-custom-video-resizer"></a>Creazione di una ridisposizione video personalizzata

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

> [!Note]  
> Questa funzionalità richiede DirectX 9,0 o versione successiva.

 

Quando [DirectShow editing Services](directshow-editing-services.md) (des) ridimensiona una clip di origine video, il comportamento predefinito è *StretchBlt*, che è veloce ma non con anti-aliasing. È possibile modificare il comportamento di ridimensionamento implementando un oggetto Resizer personalizzato come filtro di trasformazione DirectShow. Il filtro deve esporre l'interfaccia [**IResize**](iresize.md) , che consente a des di specificare le dimensioni del video di input e di output. Per informazioni sulla scrittura di un filtro di trasformazione, vedere [scrittura di filtri di trasformazione](writing-transform-filters.md). La classe base **CTransformFilter** è consigliata come punto di partenza. Quando si implementa il filtro, tenere presente quanto segue:

-   Supportare l'interfaccia **IResize** sul filtro (non sui pin).
-   Il filtro deve accettare solo formati [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (Format \_ videoinfo). Rifiutare altri tipi di formato.
-   Il formato video di DES può essere qualsiasi tipo RGB non compresso, incluso RGB a 32 bit con Alpha (MEDIASUBTYPE \_ ARGB32). Il filtro può rifiutare in modo sicuro i formati con **biHeight** < 0.
-   Prima di connettere il pin di output del filtro, il motore di rendering chiama [**IResize::p UT \_ mediaType**](iresize-put-mediatype.md) per impostare il tipo di output. Può anche chiamare [**IResize::p \_ dimensioni UT**](iresize-put-size.md) per modificare le dimensioni di output. Può chiamare questi due metodi in qualsiasi ordine, un numero qualsiasi di volte, prima di connettere il pin di output.
-   Una volta che il motore di rendering si connette al pin di output, potrebbe chiamare nuovamente **put \_ size** . Il filtro Resizer deve riconnettere il pin di output con le nuove dimensioni.
-   All'interno del metodo [**CTransformFilter:: Transform**](ctransformfilter-transform.md) del filtro, estendere il video di input alla dimensione di output.
-   Il filtro non deve mai impostare il flag di discontinuità nell'esempio di output o alleghi un tipo di supporto all'esempio di output.
-   Per salvare lo stato del filtro in un file GraphEdit (con estensione GRF), implementare l'interfaccia **IPersistStream** . Questa operazione è facoltativa, ma utile per i test.

Per usare il filtro di ridimensionamento, è necessario che il filtro sia registrato come oggetto COM nel sistema dell'utente. Prima che l'applicazione esegua il rendering del progetto video, eseguire una query sul motore di rendering per l'interfaccia [**IRenderEngine2**](irenderengine2.md) e chiamare [**IRenderEngine2:: SETRESIZERGUID**](irenderengine2-setresizerguid.md) con il CLSID del filtro di ridimensionamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un progetto](rendering-a-project.md)
</dt> </dl>

 

 



