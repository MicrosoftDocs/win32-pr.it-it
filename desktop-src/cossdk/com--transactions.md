---
description: Transazioni COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401465"
---
# <a name="com-transactions"></a>Transazioni COM+

Quando si acquista un libro da una libreria online, si usa una carta di credito per scambiare denaro per un libro. Una volta inviato l'ordine, una serie di operazioni correlate (convalida della carta di credito, verifica della disponibilità dell'inventario e così via) garantisce la disponibilità del libro e l'ottenimento del denaro da parte della libreria. Se una singola operazione della serie ha esito negativo durante lo scambio, l'intero scambio avrà esito negativo. Non è possibile ottenere il libro e la libreria non ottiene il denaro.

La tecnologia responsabile dell'esecuzione di questo scambio online bilanciato e prevedibile è detta *elaborazione delle transazioni*. A livello di codice, una *transazione* è un'unità di lavoro in cui si verifica una serie di operazioni. COM+ utilizza transazioni programmatiche per garantire che le risorse non vengano aggiornate in modo permanente, a meno che tutte le operazioni all'interno della transazione non vengano completate. Associando insieme un set di operazioni correlate in una transazione COM+ che ha esito positivo o negativo completamente, è possibile semplificare notevolmente il ripristino degli errori.

Negli argomenti seguenti viene introdotta la teoria generale dell'elaborazione delle transazioni, vengono fornite informazioni dettagliate sulle transazioni in COM+ e vengono presentati suggerimenti pratici per la scrittura di componenti transazionali.



| Argomento                                                                   | Descrizione                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Concetti sulle transazioni COM+](com--transactions-concepts.md)<br/> | Vengono presentati termini e concetti di base.<br/>                                  |
| [Attività delle transazioni COM+](com--transactions-tasks.md)<br/>       | Vengono fornite informazioni pratiche sulla scrittura di componenti transazionali.<br/> |



 

 

 




