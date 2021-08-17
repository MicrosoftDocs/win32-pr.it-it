---
description: Uso di origini multimediali con la sessione multimediale
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Uso di origini multimediali con la sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ffec1b854829b5b8a0317d10adf121463e539dde471bc5b3063b1479037ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688725"
---
# <a name="using-media-sources-with-the-media-session"></a>Uso di origini multimediali con la sessione multimediale

Se si usa la sessione multimediale per controllare la riproduzione, il set di metodi da chiamare su un'origine multimediale è limitato. Questa sezione descrive come usare l'origine multimediale in combinazione con la sessione multimediale.

Ecco i passaggi di base che verranno eseguono dall'applicazione:

1.  Creare l'origine multimediale. Per creare un'origine multimediale, usare il sistema di risoluzione di origine. Per altre informazioni, vedere [Resolver di origine](source-resolver.md). Il sistema di risoluzione di origine restituisce un puntatore [**all'interfaccia IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine. Se è stata scritta un'origine multimediale personalizzata, è invece possibile fornire un metodo di creazione personalizzato.

2.  Configurare la presentazione. Per configurare la presentazione dell'origine, chiamare [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). È possibile modificare questa copia, ma le modifiche non diventano attive fino all'avvio della riproduzione. Non modificare il descrittore di presentazione durante la riproduzione. Per altre informazioni, vedere [Descrittori di presentazione](presentation-descriptors.md).

3.  Creare una topologia contenente l'origine multimediale. Per altre informazioni, vedere [Topologie .](topologies.md)

4.  Usare la sessione multimediale per controllare la riproduzione. La sessione multimediale chiama i metodi sull'origine multimediale. L'applicazione non deve chiamare metodi sull'origine multimediale in questo momento.

5.  Prima di rilasciare l'origine multimediale, chiamare [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) per arrestare l'origine.

    > [!Note]  
    > Se si usa l'origine sequencer, l'origine sequencer gestisce l'arresto delle origini dei segmenti. Per altre informazioni, vedere [Origine sequencer](sequencer-source.md).

     

Se si usa la sessione multimediale, gli unici metodi che è necessario chiamare sull'origine multimediale sono [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)e [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). In particolare:

-   Non chiamare [**Start,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)o [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); Questi metodi devono essere chiamati solo dalla sessione multimediale.

-   Non chiamare alcun [**metodo IMFMediaStream.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

-   Non recuperare gli eventi direttamente dall'origine multimediale o da uno dei flussi. La sessione multimediale deve ricevere questi eventi per il corretto funzionamento della pipeline. La sessione multimediale inoltra gli eventi necessari per l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> </dl>

 

 



