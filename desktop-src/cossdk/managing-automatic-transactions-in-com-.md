---
description: Nel modello di programmazione COM+ è possibile progettare i componenti in modo da eseguire le operazioni migliori&\# 8212, abilitando la logica di business o stabilendo una connessione di database&\# 8212; e basandosi sul Framework di elaborazione delle transazioni di Microsoft Windows per automatizzare le transazioni.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Gestione delle transazioni automatiche in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524057"
---
# <a name="managing-automatic-transactions-in-com"></a>Gestione delle transazioni automatiche in COM+

Nel modello di programmazione COM+ è possibile progettare i componenti per eseguire le operazioni migliori, ovvero abilitare la logica di business o stabilire una connessione al database, e basarsi sul Framework di elaborazione delle transazioni di Microsoft Windows per automatizzare le transazioni.

## <a name="starting-a-transaction"></a>Avvio di una transazione

COM+ avvia automaticamente una transazione quando si verifica una delle condizioni seguenti:

-   Quando un client non transazionale chiama un componente che richiede una transazione o richiede una nuova transazione.
-   Quando un client transazionale chiama un componente che richiede una nuova transazione.

Se COM+ determina che un oggetto deve disporre di una nuova transazione, avvia prima la transazione e quindi inserisce l'oggetto al suo interno. Il processo include i passaggi seguenti:

1.  COM+ crea un oggetto context, imposta gli attributi di [attivazione](com--just-in-time-activation.md) e [sincronizzazione](com--synchronization.md) JIT su Required e imposta rispettivamente i [flag coerenti e done](consistent-and-done-flags.md) su true e false.
2.  COM+ comunica con il Distributed Transaction Coordinator (DTC) per avviare una transazione. Il DTC coordina la transazione fisica.
3.  Il DTC genera un identificatore di transazione e lo passa nuovamente a COM+. L'identificatore di transazione stabilisce un limite della transazione. Tutti gli oggetti che partecipano alla transazione condividono lo stesso identificatore.
4.  Quando il client crea l'oggetto, COM+ lo attiva all'interno del limite della transazione.

## <a name="ending-a-transaction"></a>Fine di una transazione

COM+ termina una transazione automatica eseguendone il commit o l'interruzione quando si verifica una delle condizioni seguenti:

-   L'oggetto radice della transazione ne completa il lavoro e COM+ lo rilascia. Dopo la disattivazione dell'oggetto radice, la transazione tenta di eseguire il commit.
-   Il client rilascia l'oggetto radice. Senza un riferimento, l'oggetto radice viene disattivato e la transazione tenta di eseguire il commit.
-   La transazione supera la soglia di timeout. La transazione viene interrotta automaticamente se non viene eseguito il commit entro il periodo di timeout della transazione, disattivando tutti gli oggetti associati alla transazione. Il periodo di timeout predefinito per la transazione è di 60 secondi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flag coerenti e done](consistent-and-done-flags.md)
</dt> <dt>

[Velocizzare le transazioni inviando una notifica all'oggetto radice](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[Terminazione di una transazione automatica mediante una chiamata a Tocomplete](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



