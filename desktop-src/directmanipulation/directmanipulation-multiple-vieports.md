---
description: Quando si usano più viewport, l'hit testing determina quali viewport sono interessati dall'input dell'utente prendendo la posizione sullo schermo di un contatto e determinando quale rettangolo di visualizzazione raggiunge il contatto.
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: Uso di più viewport in DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: e422d99d8a71fbf24af5fc60641da7ac808b54215c56e5d81b8c222226ef8452
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787523"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a>Uso di più viewport in DirectManipulation

Quando si usano più viewport, *l'hit testing* determina quali viewport sono interessati dall'input dell'utente prendendo la posizione sullo schermo di un contatto e determinando quale rettangolo di visualizzazione raggiunge il contatto.

Uno scenario comune nella manipolazione [diretta consiste](direct-manipulation-portal.md) nell'inserire un viewport all'interno di un altro, noto anche come *annidamento dei viewport.* Se il contatto raggiunge più di un viewport, l'ordine delle chiamate  [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) da [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) della finestra determina la relazione padre-figlio dei viewport annidati.

Regola: l'elemento figlio deve chiamare [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)prima di chiamare l'elemento padre.

![Diagramma che illustra la gerarchia degli hit test](images/dm-art-8.png)

Un contatto entra in un viewport. [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) deve essere chiamato prima sul viewport arancione (figlio) e quindi sul viewport verde (padre) per stabilire la gerarchia corretta.

## <a name="targeting-the-correct-viewport"></a>Destinazione del viewport corretto

Un contatto può essere associato a un numero qualsiasi di viewport e ogni contatto può essere assegnato a un set diverso di viewport.

Ogni viewport può essere configurato per supportare interazioni specifiche, in base alle esigenze.

In base a queste impostazioni, [la manipolazione diretta identifica](direct-manipulation-portal.md) il viewport che gestisce l'input. Il viewport più figlio nella gerarchia di hit testing ha la prima possibilità di gestire l'input. Tuttavia, sia il concatenamento che l'innalzamento di livello padre possono modificare il viewport che gestisce l'input.

## <a name="chaining"></a>Concatenamento

Quando viene raggiunta la fine del contenuto durante una [manipolazione,](direct-manipulation-portal.md) la manipolazione diretta applica un effetto limite per indicare che il contenuto non può andare oltre. Tuttavia, se un viewport figlio è *concatenato* a un viewport padre, questo effetto viene eliminato. Il viewport predecessore più vicino nella gerarchia di hit testing che supporta la manipolazione gestisce invece l'input. Se la direzione della manipolazione è inversa in modo che il predecessore torni al punto in cui è stato attivato il concatenamento, la manipolazione "nonchain" e il controllo vengono nuovamente restituiti al viewport figlio.

![Diagramma che mostra la manipolazione concatenata](images/dm-art-9.png)

Quando l'utente esegue la panoramica del viewport figlio fino al bordo del contenuto, la manipolazione viene concatenata al riquadro di visualizzazione padre e l'utente inizia invece a eseguire la panoramica del contenuto padre.

> [!Note]  
> Gli assi X e Y si concatenano indipendentemente l'uno dall'altro, quindi se una panoramica diagonale raggiunge il limite x prima del limite y, la manipolazione sposta l'elemento padre nella direzione x continuando a spostare l'elemento figlio nella direzione y. Per abilitare o disabilitare il concatenamento, chiamare [**l'API SetChaining**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) nel viewport figlio.

### <a name="rails"></a>Rotaie

La specifica delle guide nella configurazione di un viewport influisce sul modo in cui l'input viene concatenato dal viewport. In particolare, l'input non può essere concatenato da un viewport figlio con guide al relativo elemento padre nella modalità di panoramica "non srotolato" delle guide. Per concatenare l'input quando sono impostate le guide, l'utente deve avere una panoramica verticale o orizzontale ed essere bloccato alle guide.

### <a name="zooming"></a>Zoom

Se un viewport figlio è annidato all'interno di un elemento padre ed entrambi sono configurati per lo zoom, una manipolazione dello zoom può essere concatenata da figlio a padre. Tuttavia, se la manipolazione continua, funziona solo sull'elemento padre e non può essere "scambiata" con l'elemento figlio. Se l'utente concatena uno zoom da figlio a [padre,](direct-manipulation-portal.md) la manipolazione diretta sospende l'elemento figlio finché tutti i contatti associati alla manipolazione non vengono rimossi dallo schermo. A questo punto, l'elemento figlio viene rilasciato dalla sospensione e l'utente può eseguire una panoramica del viewport figlio.

## <a name="gesture-targeting-parent-promotion"></a>Destinazione del movimento: promozione padre

*La destinazione del movimento* è il processo in base al quale [la manipolazione](direct-manipulation-portal.md) diretta raggruppa i contatti e determina quale riquadro di visualizzazione elabora l'input. *La promozione* padre si riferisce ai casi in cui l'input viene trasferito dall'elemento figlio all'elemento padre. Ad esempio, quando un utente posiziona due contatti e avvicina le dita all'interno di un viewport figlio configurato solo per lo scorrimento, l'input viene promosso all'elemento padre in modo che si verifichi lo zoom. La promozione dell'elemento padre viene eseguita indipendentemente dal fatto che il concatenamento sia abilitato nel viewport figlio.

A differenza del concatenamento, la promozione padre non viene inversa. Il viewport padre continua a elaborare l'input di interazione fino a quando tutti i contatti non vengono eliminati (i viewport figlio non interrompino l'elaborazione dell'input).
