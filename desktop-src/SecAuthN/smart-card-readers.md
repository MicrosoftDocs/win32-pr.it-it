---
description: I lettori sono dispositivi standard in un sistema di smart card. Sono controllati tramite driver e vengono introdotti e rimossi dal sistema tramite Plug and Play o tramite l'elemento dispositivi del pannello di controllo.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Lettori di smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316225"
---
# <a name="smart-card-readers"></a>Lettori di smart card

I lettori sono dispositivi standard in un sistema di [*Smart Card*](../secgloss/s-gly.md) . Sono controllati tramite driver e vengono introdotti e rimossi dal sistema tramite Plug and Play o tramite l'elemento dispositivi del pannello di controllo.

Ogni lettore deve essere definito per l'uso da parte del [*sottosistema Smart Card*](../secgloss/s-gly.md). Il sottosistema non è responsabile di alcun lettore non fornito in modo specifico.

I lettori di smart card possono essere divisi in gruppi logici denominati gruppi di Reader. Questi gruppi possono essere definiti dal sottosistema, nonché definiti da amministratori e utenti. Un reader può appartenere a più di un gruppo di Reader

Il sottosistema Smart Card definisce i gruppi seguenti.



| Gruppo                | Descrizione                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $ AllReaders spaventato     | Questo gruppo contiene tutti i lettori del sistema. Un nuovo lettore assegnato al sottosistema smart card viene incluso automaticamente nel gruppo di lettori a livello di sistema, SCard $ AllReaders.                         |
| $ DefaultReaders spaventato | Questo gruppo predefinito, uno per ogni [*terminale*](../secgloss/t-gly.md), contiene tutti i lettori assegnati al terminale che non sono riservati per un uso specifico. |



 

 

 
