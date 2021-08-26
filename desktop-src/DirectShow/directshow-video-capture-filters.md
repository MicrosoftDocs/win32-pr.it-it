---
description: DirectShow Filtri di acquisizione video
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: DirectShow Filtri di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cafe2815376ddb2a099c309228ba1bf24ae9315f305edb7312b88dd1196f82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966331"
---
# <a name="directshow-video-capture-filters"></a>DirectShow Filtri di acquisizione video

I filtri di acquisizione DirectShow alcune funzionalità che li distinguono da altri tipi di filtri. Anche se [Capture Graph Builder](capture-graph-builder.md) nasconde molti dei dettagli, è buona idea leggere questa sezione per avere una conoscenza generale DirectShow grafici di acquisizione.

**Aggiungere categorie**

Un filtro di acquisizione spesso ha due o più pin di output che recapitano lo stesso tipo di dati, ad esempio un pin di anteprima e un pin di acquisizione. Pertanto, i tipi di supporti non sono un buon modo per distinguere i pin. I pin vengono invece distinti in base alla relativa funzionalità, identificata tramite un GUID, denominato *categoria di pin*.

Per una descrizione di come eseguire query sui pin per la categoria, vedere [Uso delle categorie di pin](working-with-pin-categories.md). Per la maggior parte delle applicazioni, tuttavia, non è necessario eseguire query direttamente su pin. I vari metodi [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) accettano invece parametri che specificano la categoria di pin su cui operare. Capture Graph Builder individua automaticamente il pin corretto.

**Pin di anteprima e pin di acquisizione**

Alcuni dispositivi di acquisizione video hanno pin di output separati per l'anteprima e l'acquisizione. Il segnaposto di anteprima viene usato per eseguire il rendering del video sullo schermo, mentre il segnaposto di acquisizione viene usato per scrivere video in un file.

Un segnaposto di anteprima e un segnaposto di acquisizione hanno le differenze seguenti:

-   Un segnaposto di anteprima elimina i fotogrammi in base alle esigenze per mantenere la velocità effettiva sul pin di acquisizione.
-   Ogni fotogramma di un segnaposto di acquisizione viene contrassegnato con il timestamp con l'ora del flusso in cui è stato acquisito il frame. Un segnaposto di anteprima non indica il timestamp degli esempi forniti.

Il motivo per cui i fotogrammi di anteprima non hanno timestamp è che il grafico dei filtri introduce una piccola quantità di latenza nel flusso. Se il tempo di acquisizione viene usato come ora di presentazione, il renderer video considera ogni campione leggermente in ritardo. In questo modo il renderer video può rilasciare fotogrammi mentre tenta di recuperare. La rimozione dei timestamp garantisce che il renderer presenti ogni campione all'arrivo, senza eliminare fotogrammi.

La categoria di pin per i pin di anteprima è PIN \_ CATEGORY \_ PREVIEW. La categoria per i pin di acquisizione è PIN \_ CATEGORY \_ CAPTURE.

**Pin di porta video**

Una porta video è una connessione hardware tra un dispositivo video (ad esempio un sintonizzatore TV analogico) e la scheda video. Una porta video consente al dispositivo di inviare dati video direttamente alla scheda grafica. Il video viene visualizzato sullo schermo usando una sovrimpressione hardware. Una porta video potrebbe essere un cavo effettivo che connette due dispositivi su schede separate; oppure potrebbe trattarsi di una connessione cablata nella stessa scheda.

Il vantaggio di una porta video è che il video passa direttamente alla memoria video, senza alcun lavoro da parte della CPU. Tuttavia, le porte video hanno alcuni svantaggi:

-   Una porta video usa sempre la superficie di sovrapposizione durante l'acquisizione, indipendentemente dal fatto che si voglia visualizzare in anteprima il video.
-   Il capovolgimento tra i fotogrammi viene eseguito automaticamente, il che rende difficile sincronizzare il capovolgimento con altre operazioni video.

Se un dispositivo di acquisizione usa una porta video, il filtro di acquisizione dispone di un pin della porta video anziché di un pin di anteprima. La categoria di pin per i pin della porta video è PIN \_ CATEGORY \_ VIDEOPORT.

Ogni filtro di acquisizione ha almeno un pin di acquisizione. Inoltre, potrebbe avere un pin di anteprima o un pin della porta video, ma mai entrambi. I filtri possono avere più pin di acquisizione e pin di anteprima, ognuno dei quali offre un tipo di supporto separato. Di conseguenza, un singolo filtro può avere un pin di acquisizione video, un segnaposto di anteprima video, un segnaposto di acquisizione audio e un pin di anteprima audio. Non esiste tuttavia alcun equivalente a una porta video per l'audio.

**Filtri WDM upstream**

Windows I dispositivi WDM (Driver Model) possono richiedere alcuni filtri aggiuntivi a monte dal filtro di acquisizione. Questi filtri includono quanto segue:

-   [Filtro siner TV](tv-tuner-filter.md). Controlla l'ottimizzazione per i sintonizzatori TV analogici.
-   [Filtro audio TV](tv-audio-filter.md). Controlla le impostazioni audio per i sintonizzatori TV analogici.
-   [Filtro barra incrociata video analogico](analog-video-crossbar-filter.md). Instrada i segnali video e audio attraverso il dispositivo hardware. Ad esempio, un dispositivo potrebbe avere più input, ad esempio S-Video e video composito. Il filtro barra incrociata consente all'applicazione di selezionare l'input.

Anche se si tratta di filtri separati DirectShow, in genere rappresentano lo stesso dispositivo hardware. Ogni filtro controlla una funzione diversa del dispositivo. I filtri sono connessi tramite pin, ma nessun dato multimediale viene spostato tra le connessioni dei pin. Pertanto, i pin su questi filtri non si connettono stabilendo un tipo di supporto. Usano invece valori GUID denominati *mediums.* I GUID medi sono definiti in modo univoco per un determinato minidriver del dispositivo. Ad esempio, il filtro Siner TV e il filtro Acquisizione video per la stessa scheda TV supporteranno entrambi lo stesso supporto, che consente all'applicazione di compilare correttamente il grafico.

In pratica, se si usa **ICaptureGraphBuilder2** per compilare i grafici di acquisizione, questi filtri vengono aggiunti automaticamente al grafico. Per una descrizione più dettagliata, vedere [Filtri del driver di classe WDM.](wdm-class-driver-filters.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'acquisizione di video in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



