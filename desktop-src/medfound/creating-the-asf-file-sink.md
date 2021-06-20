---
description: Informazioni sulla creazione del sink di file ASF, che un'applicazione può usare per archiviare i dati multimediali di ASF in un file.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Creazione del sink del file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fcd9ea19f0200dfd330f421fd5dac2cd100b702
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409924"
---
# <a name="creating-the-asf-file-sink"></a>Creazione del sink del file ASF

Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati multimediali di ASF in un file. Per informazioni sul modello a oggetti di ASF Media Sinks e sull'utilizzo generale, vedere [AsF Media Sinks](asf-media-sinks.md).

Esistono due modi per creare un'istanza del sink di file ASF. È possibile chiamare [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) o [**MFCreateASFMediaSinkActivate.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)

Se si chiama [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), è necessario specificare un flusso di byte, per il file di output, in cui il sink scriverà il contenuto asf durante una sessione di codifica. Il flusso di byte specificato deve avere funzionalità ricercabili e scrivibili; in caso contrario, la chiamata **MFCreateASFMediaSink** ha esito negativo con il codice di errore E \_ FAIL. Questa chiamata crea un oggetto sink di file in-process e restituisce un puntatore [**all'interfaccia IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del sink di file.

Se si chiama [**MFCreateASFMediaSinkActivate,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)è necessario specificare l'URL del file di output in cui il sink di file scriverà i dati multimediali. In questo caso, il sink di file crea internamente il flusso di byte. La funzione restituisce un puntatore [**all'interfaccia IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del sink di file. Per

Prendere [**in considerazione MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) anziché [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)quando la topologia di codifica è progettata come segue:

-   La topologia di codifica è per il percorso del supporto protetto (PMP) e il sink di file viene usato out-of-process.
-   Il nodo di output della topologia viene creato usando il puntatore restituito all'oggetto activate del sink di file e l'applicazione tiene traccia dei flussi nel sink di file in base ai numeri di flusso.
    > [!Note]  
    > È possibile attivare il sink di file chiamando [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Non è tuttavia necessario attivare esplicitamente l'oggetto. La sessione multimediale tiene traccia dell'oggetto attivazione e attiva automaticamente il sink del file durante la sessione di codifica.

     

-   Le informazioni sul flusso vengono configurate nell'oggetto ContentInfo. Disucssed nella sottosezioni successiva.

Dopo aver creato il sink di file ASF, è necessario configurarlo prima di compilare la topologia. Il sink di file deve conoscere le informazioni seguenti per generare il file di output.

-   Informazioni di base sul flusso
-   Informazioni sulla modalità di codifica
-   Metadati

Il sink di file implementa [l'oggetto ContentInfo](asf-contentinfo-object.md) di ASF ed espone l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) in modo che un'applicazione possa usarla per impostare informazioni correlate ai flussi e alla codifica. A seconda della funzione chiamata per creare il sink di file, esistono due modi per ottenere un riferimento **all'interfaccia IMFASFContentInfo.**

-   Se si chiama la [**funzione MFCreateASFMediaSink,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) l'applicazione deve eseguire una query per l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) chiamando **IMFMediaSink::QueryInterface** sul sink di file restituito.
-   Se si sceglie di chiamare [**MFCreateASFMediaSinkActivate,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)questa funzione prevede che sia presente un oggetto ContentInfo completamente configurato prima della chiamata. A tale scopo, è necessario creare un oggetto ContentInfo vuoto chiamando [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) e quindi configurarlo con tutte le informazioni necessarie. Passare l'oggetto ContentInfo configurato a **MFCreateASFMediaSinkActivate** per ricevere un puntatore all'oggetto di attivazione sink. Non è possibile attivare il sink di file usando l'oggetto di attivazione restituito e quindi modificare le informazioni di flusso o codifica.

Per informazioni sulla configurazione di flussi di sink e proprietà specifiche, vedere gli argomenti seguenti:

-   [Aggiunta di informazioni di flusso al sink del file ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Impostazione delle proprietà nel sink file](setting-properties-in-the-file-sink.md)
-   [Aggiunta di metadati al sink di file](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sink multimediali asf](asf-media-sinks.md)
</dt> <dt>

[Componenti ASF del livello pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



