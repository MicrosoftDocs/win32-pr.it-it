---
description: Informazioni sul controllo della frequenza
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Informazioni sul controllo della frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ae8ad5bcfaaf415c888418a7a6bd5d77f72434150e30fcac071d078b8ee6d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035659"
---
# <a name="about-rate-control"></a>Informazioni sul controllo della frequenza

In Media Foundation, la velocità *di riproduzione* è espressa come rapporto tra la velocità di riproduzione corrente e la velocità di riproduzione normale. Ad esempio, una velocità di 2,0 è il doppio della velocità normale e 0,5 è la velocità metà normale. I valori negativi indicano la riproduzione inversa. Una velocità di riproduzione di -2.0 viene riprodotta all'indietro nel flusso al doppio della velocità normale. Con una frequenza pari a zero viene eseguito il rendering di un frame. Successivamente, l'orologio di presentazione non avanza. Per ottenere un altro frame alla frequenza zero, l'applicazione deve cercare una nuova posizione.

Le applicazioni usano le interfacce seguenti per controllare la velocità di riproduzione.

-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). Consente di individuare le velocità di riproduzione più veloci e lente possibili.
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Usato per modificare la velocità di riproduzione.

Per ottenere queste due interfacce, chiamare [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nella sessione multimediale. L'identificatore del servizio è MF \_ RATE \_ CONTROL \_ SERVICE.

Usando il servizio di controllo della frequenza, un'applicazione può implementare la riproduzione in avanti e inversa.

## <a name="thinning"></a>Assottigliamento

*Il thinning* è qualsiasi processo che riduce il numero di campioni in un flusso, per ridurre la velocità in bit complessiva. Per i video, il thinning viene in genere ottenuto eliminando i fotogrammi differenziali e recapitando solo i fotogrammi chiave. Spesso la pipeline può supportare velocità di riproduzione più veloci usando la riproduzione con thinning, perché la velocità dei dati è inferiore perché i fotogrammi differenziali non vengono decodificati.

Il thinning non modifica i timestamp o le durate dei campioni. Ad esempio, se la frequenza nominale del flusso video è di 25 fotogrammi al secondo, la durata di ogni fotogramma è ancora contrassegnata come 40 millisecondi, anche se l'origine multimediale sta eliminando tutti i fotogrammi differenziali. Ciò significa che ci sarà un intervallo di tempo tra la fine di un fotogramma e l'inizio del successivo.

## <a name="scrubbing"></a>Pulitura

*Lo scrubbing* è il processo di ricerca istantanea di punti specifici nel flusso interagendo con una barra di scorrimento, una sequenza temporale o un'altra rappresentazione visiva del tempo. Il termine deriva dall'era dei lettori di nastri reel-to-reel quando si scorreva un rullo avanti e indietro per individuare una sezione era come eseguire lo scrubbing della testa di riproduzione con il nastro.

Lo scrubbing viene implementato in Media Foundation impostando la velocità di riproduzione su zero. Per altre informazioni, vedere [How to Perform Scrubbing](how-to-perform-scrubbing.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[Ricerca, avanzamento rapido e riproduzione inversa](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[Interfacce del servizio](service-interfaces.md)
</dt> </dl>

 

 



