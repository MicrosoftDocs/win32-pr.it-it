---
description: Il sink di file ASF è un'implementazione di IMFMediaSink fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file. Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai sink di supporto ASF.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Creazione del sink di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c43625bcbc581b4967d4db99cef71a0fc779f070
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127943"
---
# <a name="creating-the-asf-file-sink"></a>Creazione del sink di file ASF

Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file. Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai [sink di supporto ASF](asf-media-sinks.md).

Esistono due modi per creare un'istanza del sink di file ASF. È possibile chiamare [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) o [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate).

Se si chiama [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), è necessario specificare un flusso di byte, per il file di output, in cui il sink scriverà il contenuto ASF durante una sessione di codifica. Il flusso di byte specificato deve avere funzionalità ricercabili e scrivibili in caso contrario, la chiamata a **MFCreateASFMediaSink** ha esito negativo con il \_ codice di errore E non riuscito. Questa chiamata crea un oggetto sink di file in-process e restituisce un puntatore all'interfaccia [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del sink di file.

Se si chiama [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), è necessario specificare l'URL del file di output in cui il sink di file scriverà i dati multimediali. In questo caso, il sink di file crea internamente il flusso di byte. La funzione restituisce un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del sink di file. A

Prendere in considerazione [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) anziché [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)quando la topologia di codifica è progettata come segue:

-   La topologia di codifica è per il percorso del supporto protetto (PMP) e il sink di file viene usato out-of-process.
-   Il nodo di output della topologia viene creato usando il puntatore restituito all'oggetto Activate del sink di file e l'applicazione tiene traccia dei flussi nel sink di file in base ai numeri di flusso.
    > [!Note]  
    > È possibile attivare il sink di file chiamando [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Tuttavia, non è necessario attivare l'oggetto esplicitamente. La sessione multimediale tiene traccia dell'oggetto attivazione e attiva automaticamente il sink di file durante la sessione di codifica.

     

-   Le informazioni sul flusso sono configurate nell'oggetto ContentInfo. Disucssed nella sottosezione successiva.

Dopo aver creato il sink di file ASF, è necessario configurarlo prima di compilare la topologia. Per generare il file di output, è necessario che il sink di file conosca le informazioni seguenti.

-   Informazioni sul flusso di base
-   Informazioni sulla modalità di codifica
-   Metadati

Il sink di file implementa l' [oggetto ContentInfo ASF](asf-contentinfo-object.md) ed espone l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) in modo che possa essere usata da un'applicazione per impostare informazioni correlate ai flussi e alla codifica. A seconda della funzione chiamata per creare il sink di file, esistono due modi per ottenere un riferimento all'interfaccia **IMFASFContentInfo** .

-   Se si chiama la funzione [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) , l'applicazione deve eseguire una query per l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) chiamando **IMFMediaSink:: QueryInterface** sul sink di file restituito.
-   Se si sceglie di chiamare [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), questa funzione prevede che sia presente un oggetto ContentInfo completamente configurato prima della chiamata. A tale scopo, è necessario creare un oggetto ContentInfo vuoto chiamando [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) e quindi configurarlo con tutte le informazioni necessarie. Passare l'oggetto ContentInfo configurato a **MFCreateASFMediaSinkActivate** per ricevere un puntatore all'oggetto Activate del sink. Non è possibile attivare il sink di file utilizzando l'oggetto attivazione restituito, quindi modificare le informazioni di flusso o di codifica.

Per informazioni sulla configurazione di flussi di sink e proprietà specifiche, vedere gli argomenti seguenti:

-   [Aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md)
-   [Aggiunta di metadati al sink di file](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sink di supporti ASF](asf-media-sinks.md)
</dt> <dt>

[Componenti ASF a livello pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



