---
description: Coniato dai pionieri dell'elaborazione delle transazioni, l'acronimo ACID si basa su Atomic, coerenti, isolated e Durable.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: Proprietà ACID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126600"
---
# <a name="acid-properties"></a>Proprietà ACID

Coniato dai pionieri dell'elaborazione delle transazioni, l'acronimo ACID si basa su Atomic, coerenti, isolated e Durable. Per garantire un comportamento prevedibile, tutte le transazioni devono possedere queste proprietà di base, rafforzando il ruolo di transazioni cruciali come proposizioni all-o-None.

L'elenco seguente contiene una definizione e una descrizione di ogni proprietà ACID:

<dl> <dt>

<span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomica
</dt> <dd>

Una transazione deve essere eseguita una sola volta e deve essere atomica, ovvero tutto il lavoro viene eseguito o nessuno di essi è. Le operazioni all'interno di una transazione condividono in genere una finalità comune e sono interdipendenti. Eseguendo solo un subset di queste operazioni, il sistema potrebbe compromettere la finalità complessiva della transazione. L'atomicità Elimina la possibilità di elaborare solo un subset di operazioni.

</dd> <dt>

<span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Coerente
</dt> <dd>

Una transazione deve mantenere la coerenza dei dati, trasformando uno stato coerente dei dati in un altro stato coerente di dati. Gran parte della responsabilità di mantenere la coerenza spetta allo sviluppatore di applicazioni.

</dd> <dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolato
</dt> <dd>

Una transazione deve essere un'unità di isolamento, il che significa che le transazioni simultanee devono comportarsi come se fossero l'unica transazione in esecuzione nel sistema. Poiché un livello elevato di isolamento può limitare il numero di transazioni simultanee, alcune applicazioni riducono il livello di isolamento in Exchange per una migliore velocità effettiva. Per ulteriori informazioni, vedere [configurazione dei livelli di isolamento delle transazioni](configuring-transaction-isolation-levels.md) .

</dd> <dt>

<span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durevole
</dt> <dd>

Una transazione deve essere reversibile e pertanto deve avere durabilità. Se viene eseguito il commit di una transazione, il sistema garantisce che gli aggiornamenti possano essere mantenuti anche se il computer si arresta immediatamente dopo il commit. La registrazione specializzata consente alla procedura di riavvio del sistema di completare le operazioni non completate richieste dalla transazione, rendendo la transazione durevole.

</dd> </dl>

 

 



