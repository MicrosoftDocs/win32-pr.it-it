---
description: Fornire un ridimensionatore video personalizzato
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Fornire un ridimensionatore video personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a006f4620accc3917ae3072846f99f7537a1eadfaab21da36aab17f17d94e433
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747901"
---
# <a name="providing-a-custom-video-resizer"></a>Fornire un ridimensionatore video personalizzato

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

> [!Note]  
> Questa funzionalità richiede DirectX 9.0 o versione successiva.

 

Quando [DirectShow Editing Services](directshow-editing-services.md) (DES) ridimensiona un clip sorgente video, il comportamento predefinito è *StretchBlt*, che è veloce ma non antialiasing. È possibile modificare il comportamento di ridimensionamento implementando un ridimensionamento personalizzato come filtro DirectShow trasformazione. Il filtro deve esporre [**l'interfaccia IResize,**](iresize.md) che consente a DES di specificare le dimensioni del video di input e output. Per informazioni sulla scrittura di un filtro di trasformazione, vedere [Scrittura di filtri di trasformazione](writing-transform-filters.md). La classe di base **CTransformFilter** è consigliata come punto di partenza. Quando si implementa il filtro, tenere presente quanto segue:

-   Supportare **l'interfaccia IResize** nel filtro (non i pin).
-   Il filtro deve accettare solo [**formati VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (FORMAT \_ VideoInfo). Rifiutare altri tipi di formato.
-   Il formato video di DES può essere qualsiasi tipo RGB non compresso, incluso RGB a 32 bit con alfa (MEDIASUBTYPE \_ ARGB32). Il filtro può rifiutare in modo sicuro i formati **con biHeight** < 0.
-   Prima che il motore di rendering connetta il pin di output del filtro, chiama [**IResize::p ut \_ MediaType**](iresize-put-mediatype.md) per impostare il tipo di output. Può anche chiamare [**IResize::p ut \_ Size per**](iresize-put-size.md) regolare le dimensioni dell'output. Può chiamare questi due metodi in qualsiasi ordine, in qualsiasi numero di volte, prima di connettere il pin di output.
-   Dopo che il motore di rendering ha connesso il pin di output, potrebbe chiamare **di nuovo put \_ Size.** Il filtro di ridimensionamento deve riconnettere il segnaposto di output con le nuove dimensioni.
-   All'interno del metodo [**CTransformFilter::Transform del**](ctransformfilter-transform.md) filtro, estendere il video di input fino alle dimensioni di output.
-   Il filtro non deve mai impostare il flag di discontinuità nell'esempio di output o collegare un tipo di supporto all'esempio di output.
-   Per salvare lo stato del filtro in un file GraphEdit (con estensione grf), implementare **l'interfaccia IPersistStream.** È facoltativo, ma utile per i test.

Per usare il filtro di ridimensionamento, il filtro deve essere registrato come oggetto COM nel sistema dell'utente. Prima che l'applicazione eserviti il progetto video, eseguire una query sul motore di rendering per l'interfaccia [**IRenderEngine2**](irenderengine2.md) e chiamare [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) con il CLSID del filtro di ridimensionamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un Project](rendering-a-project.md)
</dt> </dl>

 

 



