---
description: Notifiche di fine flusso
ms.assetid: cf2b13bc-5b54-4ac7-8a33-7434126fdf31
title: Notifiche di fine flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fcdfef1225aa5b93b56aeaa0d8ae9d0a8550c9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225466"
---
# <a name="end-of-stream-notifications"></a>Notifiche di fine flusso

Quando viene eseguito un filtro di origine che invia dati, viene chiamato il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input downstream. Il filtro downstream propaga la chiamata al filtro successivo e così via. Quando la chiamata **EndOfStream** raggiunge il renderer, il renderer Invia un evento [**EC \_ complete**](ec-complete.md) al gestore del grafico dei filtri. Se il renderer ha più pin di input, recapita l' \_ evento di completamento EC dopo che ogni pin di input ha ricevuto la notifica di fine del flusso.

Un filtro deve serializzare le chiamate [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) con altre chiamate di streaming, ad esempio [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive). In altre parole, il filtro downstream deve ricevere sempre le chiamate nell'ordine corretto.

In alcuni casi, un filtro downstream potrebbe rilevare la fine del flusso prima che il filtro di origine lo faccia. È ad esempio possibile che il filtro downstream stia analizzando il flusso. In tal caso, il filtro downstream può inviare la notifica di fine flusso, nel qual caso deve restituire S \_ false da [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) fino a quando il grafico non viene arrestato o scaricato. Il \_ valore restituito false informa il filtro di origine per arrestare l'invio di dati.

### <a name="default-handling-of-ec_complete"></a>Gestione predefinita di EC \_ completata

Per impostazione predefinita, il gestore del grafo del filtro non trasmette ogni \_ evento di completamento EC all'applicazione. Al contrario, attende che tutti i flussi segnalino EC \_ completato e quindi Invia un singolo evento EC \_ complete. Quindi, l'applicazione riceve l'evento dopo il completamento di ogni flusso.

Per determinare il numero di flussi, il gestore del grafico dei filtri conta il numero di filtri che supportano la ricerca (tramite [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) o [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)) e un pin di input sottoposto a *rendering* , definito come un pin di input senza output corrispondenti. Il gestore del grafico dei filtri determina se il PIN viene sottoposto a rendering in uno dei due modi seguenti:

-   Il metodo [**Ipin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) del pin restituisce zero nel parametro *nPin* .
-   Il filtro espone l'interfaccia [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) e restituisce il \_ filtro am \_ \_ flag varie \_ è il \_ flag RENDERER.

### <a name="end-of-stream-notifications-in-pull-mode"></a>Notifiche di fine flusso in modalità pull

In una connessione [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) il filtro di origine non invia una notifica di fine del flusso. Instread, questa operazione viene eseguita dal filtro downstream, che in genere è un filtro del parser. Il parser Invia la chiamata [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) downstream. Non invia un upstream al filtro di origine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Distribuzione della fine del flusso](delivering-the-end-of-stream.md)
</dt> </dl>

 

 



