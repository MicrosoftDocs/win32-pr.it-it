---
description: Quando si usano più viewport, fare clic su testingdetermines quali viewport sono interessati dall'input dell'utente, prendendo la posizione dello schermo di un contatto e determinando il rettangolo del viewport a cui si riscontri il contatto.
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: Uso di più viewport in DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 627a97a7c9563ca0af9decf79b18340343dda345
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104568730"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a>Uso di più viewport in DirectManipulation

Quando si usano più viewport, l' *hit testing* determina quali viewport sono interessati dall'input dell'utente, prendendo la posizione dello schermo di un contatto e determinando quale rettangolo del viewport si riscontri il contatto.

Uno scenario comune nella [manipolazione diretta](direct-manipulation-portal.md) consiste nell'inserire un viewport all'interno di un altro, noto anche come *viewport annidamento*. Se il contatto raggiunge più di un viewport, l'ordine delle chiamate di  [**secontatto**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) dall'oggetto [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) della finestra determina la relazione padre-figlio dei viewport nidificati.

Rule: l'elemento figlio deve chiamare [**secontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)prima di chiamare il padre.

![diagramma che mostra gerarchia di hit testing](images/dm-art-8.png)

Un contatto si arresta in un riquadro di visualizzazione. Per stabilire la gerarchia corretta, è innanzitutto necessario chiamare il metodo [**secontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) sul viewport arancione (figlio) e quindi il viewport verde (padre).

## <a name="targeting-the-correct-viewport"></a>Destinazione del viewport corretto

Un contatto può essere associato a un numero qualsiasi di viewport e ogni contatto può essere assegnato a un set di viewport diverso.

Ogni Viewport può essere configurato in modo da supportare interazioni specifiche, in base alle esigenze.

In base a queste impostazioni, la [manipolazione diretta](direct-manipulation-portal.md) identifica il viewport che gestisce l'input. Il viewport più figlio nella gerarchia di hit testing ha la prima possibilità di gestire l'input. Tuttavia, sia il concatenamento che l'innalzamento di livello padre possono modificare quale viewport gestisce l'input.

## <a name="chaining"></a>Concatenamento

Quando viene raggiunta la fine del contenuto durante una manipolazione, la [manipolazione diretta](direct-manipulation-portal.md) applica un effetto limite per indicare che il contenuto non può andare oltre. Tuttavia, se un viewport figlio viene *concatenato* a un viewport padre, questo effetto viene eliminato. Al contrario, il viewport predecessore più vicino nella gerarchia di hit testing che supporta la manipolazione, gestisce l'input. Se la direzione della manipolazione è invertita in modo tale che il predecessore torni fino al punto in cui è stato attivato il concatenamento, la manipolazione "unchains" e il controllo vengono trasferiti di nuovo al viewport figlio.

![diagramma che mostra la manipolazione concatenata](images/dm-art-9.png)

Quando l'utente esegue il panning del viewport figlio fino al bordo del contenuto, la manipolazione "concatena" al viewport padre e l'utente inizia a eseguire il panning del contenuto padre.

> [!Note]  
> La catena degli assi X e Y indipendentemente l'una dall'altra, quindi se una padella diagonale raggiunge il limite x prima del limite Y, la manipolazione sposta l'elemento padre nella direzione x continuando a spostare l'elemento figlio nella direzione y. Per abilitare o disabilitare il concatenamento, chiamare l'API di [**concatenamento**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) nel viewport figlio.

### <a name="rails"></a>Rails

La specifica delle guide nella configurazione di un viewport influiscono sul modo in cui l'input viene concatenato dal viewport. In particolare, l'input non può essere concatenato da un viewport figlio recintato al relativo elemento padre nella modalità di panning "senza guida". Per concatenare l'input quando sono impostate le guide, è necessario che l'utente sia stato stroncato verticalmente o orizzontalmente ed essere bloccato sulle guide.

### <a name="zooming"></a>Zoom

Se un viewport figlio è annidato all'interno di un elemento padre ed entrambi sono configurati per lo zoom, una manipolazione dello zoom può essere concatenata da figlio a padre. Tuttavia, se la manipolazione continua, funziona solo sull'elemento padre e non può "decatenare" al figlio. Se l'utente concatena uno zoom da figlio a padre, la [manipolazione diretta](direct-manipulation-portal.md) sospende l'elemento figlio fino a quando tutti i contatti associati alla manipolazione non vengono rimossi dallo schermo. A questo punto, l'elemento figlio viene rilasciato dalla sospensione e l'utente può fare il panning del viewport figlio.

## <a name="gesture-targeting-parent-promotion"></a>Destinazione movimento: promozione padre

La *destinazione del movimento* è il processo mediante il quale i gruppi di [manipolazione diretta](direct-manipulation-portal.md) riuniscono i contatti e determinano quale viewport elabora l'input. La *Promozione padre* si riferisce ai casi in cui l'input viene trasferito dal figlio al padre. Ad esempio, quando un utente inserisce due contatti e pizzica all'interno di un viewport figlio configurato solo per lo scorrimento, l'input viene promosso all'elemento padre in modo che si verifichi lo zoom. La promozione padre si verifica indipendentemente dal fatto che il concatenamento sia abilitato nel viewport figlio.

A differenza del concatenamento, la promozione padre non è invertita. Il viewport padre continua a elaborare l'input interazione fino a quando non vengono rimossi tutti i contatti (i viewport figlio interrompono l'elaborazione dell'input).
