---
title: Strategia di controllo delle versioni e fallback
description: Quando un'applicazione rileva un aggiornamento parziale utilizzando una delle tecniche precedenti o legge un set di oggetti la cui data effettiva non è ancora stata raggiunta, l'applicazione deve gestire la situazione normalmente.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- ANNUNCIO sulle strategie di controllo delle versioni e fallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855378"
---
# <a name="versioning-and-fallback-strategies"></a>Strategia di controllo delle versioni e fallback

Quando un'applicazione rileva un aggiornamento parziale utilizzando una delle tecniche precedenti o legge un set di oggetti la cui data effettiva non è ancora stata raggiunta, l'applicazione deve gestire la situazione normalmente. Per alcune applicazioni, la risposta normale consiste nel "eseguire il fallback" a una versione precedente degli oggetti in questione. Active Directory Domain Services non forniscono una funzionalità di controllo delle versioni: le applicazioni che desiderano questa funzionalità devono fornirle autonomamente. Gli approcci al controllo delle versioni includono il mantenimento dei valori "ultimi noti" memorizzati nella cache in locale e l'archiviazione di più insiemi di oggetti nella directory, ad esempio nei contenitori "obsoleti", "correnti" e "nuovi". Sono possibili molti altri schemi.

Le implementazioni devono prestare attenzione a evitare conseguenze impreviste. Una versione precedente degli oggetti deve essere utilizzata solo quando viene rilevato un aggiornamento parziale o i nuovi oggetti non sono ancora "efficaci". Il fallback perché qualcosa nell'applicazione "non funziona" potrebbe aggirare l'intento di un amministratore. Ad esempio, due computer che in precedenza potevano comunicare potrebbero non essere in grado di eseguire questa operazione a causa di una modifica nei criteri di Internet Protocol Security (IPsec). Se questo comportamento è intenzionale per la parte dell'amministratore, i sistemi interessati non devono eseguire il fallback ai criteri che consentivano la comunicazione, perché si tratta di una violazione della sicurezza.

 

 




