---
description: Uso di origini multimediali con la sessione multimediale
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Uso di origini multimediali con la sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968890"
---
# <a name="using-media-sources-with-the-media-session"></a>Uso di origini multimediali con la sessione multimediale

Se si usa la sessione multimediale per controllare la riproduzione, il set di metodi che è necessario chiamare su un'origine multimediale è limitato. Questa sezione descrive come usare l'origine dei supporti insieme alla sessione multimediale.

Ecco i passaggi di base che verranno eseguiti dall'applicazione:

1.  Creare l'origine multimediale. Per creare un'origine multimediale, usare il resolver di origine. Per ulteriori informazioni, vedere [resolver di origine](source-resolver.md). Il resolver di origine restituisce un puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine. Se è stata scritta un'origine multimediale personalizzata, è possibile specificare invece un metodo di creazione personalizzato.

2.  Configurare la presentazione. Per configurare la presentazione dell'origine, chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). È possibile modificare questa copia, ma le modifiche non diventano attive fino a quando non viene avviata la riproduzione. Non modificare il descrittore della presentazione durante la riproduzione. Per ulteriori informazioni, vedere [descrittori di presentazione](presentation-descriptors.md).

3.  Creare una topologia che contenga l'origine del supporto. Per ulteriori informazioni, vedere [topologie](topologies.md).

4.  Usare la sessione multimediale per controllare la riproduzione. La sessione multimediale chiama i metodi sull'origine multimediale. Al momento l'applicazione non deve chiamare alcun metodo sull'origine multimediale.

5.  Prima di rilasciare l'origine del supporto, chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) per arrestare l'origine.

    > [!Note]  
    > Se si utilizza l'origine sequencer, l'origine del sequencer gestisce la chiusura delle origini del segmento. Per ulteriori informazioni, vedere [sequencer source](sequencer-source.md).

     

Se si usa la sessione multimediale, gli unici metodi che è necessario chiamare sull'origine del supporto sono [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**getcaratteristiche**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)e [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). In particolare:

-   Non chiamare [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)o [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); questi metodi devono essere chiamati solo dalla sessione multimediale.

-   Non chiamare alcun metodo [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) .

-   Non recuperare gli eventi direttamente dall'origine supporto o da uno dei flussi. Per il corretto funzionamento della pipeline, la sessione multimediale deve ricevere questi eventi. La sessione multimediale trasmette tutti gli eventi necessari per l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> </dl>

 

 



