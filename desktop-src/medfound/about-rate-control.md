---
description: Informazioni sul controllo della frequenza
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Informazioni sul controllo della frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306765"
---
# <a name="about-rate-control"></a>Informazioni sul controllo della frequenza

In Media Foundation la *velocità di riproduzione* viene espressa come rapporto tra la velocità di riproduzione corrente e la frequenza di riproduzione normale. Ad esempio, una frequenza di 2,0 è due volte la velocità normale e 0,5 è la velocità della metà normale. I valori negativi indicano la riproduzione inversa. Una velocità di riproduzione di-2,0 viene riprodotta all'indietro nel flusso al doppio della velocità normale. Una frequenza pari a zero causa il rendering di un frame; Successivamente, il clock di presentazione non avanza. Per ottenere un altro frame alla velocità pari a zero, è necessario che l'applicazione cerchi una nuova posizione.

Le applicazioni utilizzano le interfacce seguenti per controllare la velocità di riproduzione.

-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). Usato per individuare le frequenze di riproduzione più veloci e più lente possibili.
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Usato per modificare la velocità di riproduzione.

Per ottenere queste due interfacce, chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nella sessione multimediale. L'identificatore del servizio è MF \_ rate \_ Control \_ Service.

Tramite il servizio di controllo della velocità, un'applicazione può implementare una riproduzione veloce e inversa.

## <a name="thinning"></a>Diradamento

L' *assottigliamento* è un processo che riduce il numero di campioni in un flusso, per ridurre la velocità complessiva dei bit. Per i video, il assottigliamento viene in genere eseguito eliminando i frame Delta e distribuendo solo i fotogrammi chiave. Spesso la pipeline è in grado di supportare frequenze di riproduzione più veloci usando la riproduzione diluita, perché la velocità dei dati è inferiore perché i frame Delta non sono decodificati.

Il assottigliamento non modifica i timestamp o le durate degli esempi. Se, ad esempio, la velocità nominale del flusso video è 25 fotogrammi al secondo, la durata di ogni fotogramma viene comunque contrassegnata come 40 millisecondi, anche se l'origine del supporto sta eliminando tutti i frame Delta. Ciò significa che ci sarà un gap di tempo tra la fine di un frame e l'inizio del successivo.

## <a name="scrubbing"></a>Pulitura

Lo *scrubbing* è il processo di ricerca immediata di punti specifici nel flusso interagendo con una barra di scorrimento, una sequenza temporale o un'altra rappresentazione visiva del tempo. Il termine deriva dall'era dei lettori di nastri da bobina a bobina quando il dondolo di una bobina per individuare una sezione era come la pulitura della testa di riproduzione con il nastro.

Lo scrubbing viene implementato in Media Foundation impostando la velocità di riproduzione su zero. Per ulteriori informazioni, vedere [come eseguire lo scrubbing](how-to-perform-scrubbing.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[Ricerca, avanzamento rapido e riproduzione inversa](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[Interfacce del servizio](service-interfaces.md)
</dt> </dl>

 

 



