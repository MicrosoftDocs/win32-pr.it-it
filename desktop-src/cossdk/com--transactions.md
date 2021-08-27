---
description: Transazioni COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f800f637a9faec7564d929f3fe7f638ba36d9556db138283c0e6ff3aee87a4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070801"
---
# <a name="com-transactions"></a>Transazioni COM+

Quando si acquista un libro da una libreria online, si usa una carta di credito per scambiare denaro con un libro. Dopo aver inviato l'ordine, una serie di operazioni correlate (convalida della carta di credito, verifica della disponibilità dell'inventario e così via) garantisce che si otterrà il libro e che la libreria otterrà il denaro. Se una singola operazione della serie ha esito negativo durante lo scambio, l'intero scambio ha esito negativo. Non si ottiene il libro e la libreria non ottiene il denaro.

La tecnologia responsabile di rendere questo scambio online bilanciato e prevedibile è detta elaborazione *delle transazioni.* A livello di codice, *una transazione* è un'unità di lavoro in cui si verifica una serie di operazioni. COM+ usa transazioni a livello di codice per garantire che le risorse non vengano aggiornate in modo permanente a meno che tutte le operazioni all'interno della transazione non vengano completate correttamente. Associando un set di operazioni correlate in una transazione COM+ che ha esito positivo o negativo, è possibile semplificare notevolmente il recupero degli errori.

Negli argomenti seguenti viene illustrata la teoria generale dell'elaborazione delle transazioni, vengono fornite informazioni più generali sulle transazioni in COM+ e vengono forniti suggerimenti pratici per la scrittura di componenti transazionali.



| Argomento                                                                   | Descrizione                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Concetti relativi alle transazioni COM+](com--transactions-concepts.md)<br/> | Presenta termini e concetti di base.<br/>                                  |
| [Attività delle transazioni COM+](com--transactions-tasks.md)<br/>       | Fornisce informazioni pratiche sulla scrittura di componenti transazionali.<br/> |



 

 

 




