---
description: I lettori sono dispositivi standard in un smart card sistema. Vengono controllati tramite i driver e vengono introdotti e rimossi dal sistema tramite Plug and Play o tramite l'elemento Pannello di controllo dispositivi.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Lettori di smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335aabe1d815e9b6d41ccfd820242209da63134797595d8a1c85f009f8551b7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917750"
---
# <a name="smart-card-readers"></a>Lettori di smart card

I lettori sono dispositivi standard in un [*smart card*](../secgloss/s-gly.md) sistema. Vengono controllati tramite i driver e vengono introdotti e rimossi dal sistema tramite Plug and Play o tramite l'elemento Pannello di controllo dispositivi.

Ogni lettore deve essere definito per l'uso da parte [*smart card sottosistema*](../secgloss/s-gly.md). Il sottosistema non è responsabile di alcun lettore non assegnato in modo specifico.

I lettori di smart card possono essere suddivisi in gruppi logici denominati gruppi di lettori. Questi gruppi possono essere definiti dal sottosistema, nonché da amministratori e utenti. Un lettore può appartenere a più gruppi di lettori

Il smart card sottosistema definisce i gruppi seguenti.



| Gruppo                | Descrizione                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCard$AllReaders     | Questo gruppo contiene tutti i lettori nel sistema. Un nuovo lettore assegnato al sottosistema smart card viene automaticamente incluso nel gruppo di lettori a livello di sistema, SCard$AllReaders.                         |
| SCard$DefaultReaders | Questo gruppo predefinito, uno per ogni [*terminale,*](../secgloss/t-gly.md)contiene tutti i lettori assegnati al terminale che non sono riservati per un uso specifico. |



 

 

 
