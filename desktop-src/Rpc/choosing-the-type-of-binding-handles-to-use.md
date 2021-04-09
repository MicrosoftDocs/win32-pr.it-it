---
title: Scelta del tipo di handle di associazione da usare
description: Scelta del tipo di handle di associazione da usare
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044428"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Scelta del tipo di handle di associazione da usare

**Procedura consigliata:** Se si sa quale server sarà utilizzato dall'applicazione, utilizzare handle espliciti. In caso contrario, utilizzare il costrutto di handle espliciti ogni volta oppure utilizzare handle generici con routine **\_ Bind** e **\_ UNBIND** .

Non usare handle impliciti o handle automatici. Gli handle impliciti non sono thread-safe e anche se thread safety potrebbe sembrare superfluo, potrebbe essere necessario in seguito. Gli handle automatici hanno un sovraccarico elevato e richiedono un funzionamento corretto del programma di installazione. Le funzionalità di ricerca sono state sostituite dai servizi Active Directory.

Gli handle espliciti sono estremamente efficienti e molte funzionalità interessanti sono disponibili solo per gli handle espliciti. Se, ad esempio, più chiamate RPC saranno destinate allo stesso server, sarà possibile costruire il gestore dell'associazione una sola volta ed effettuare tutte le chiamate. Questo approccio è molto più efficiente rispetto a qualsiasi altro metodo. Se il server a cui la chiamata passerà è sconosciuto, costruire un handle di binding esplicito per ogni chiamata o utilizzare handle di associazione generici.

In Microsoft™ Windows XP, il tempo di esecuzione RPC è piuttosto efficiente per riutilizzare e memorizzare nella cache le chiamate, pertanto se la chiamata *n*+ 1 termina nello stesso server della chiamata *n*, RPC riutilizza le risorse allocate *per la chiamata n,* eludendo la necessità di memorizzare nella cache gli handle di binding per migliorare le prestazioni.

 

 




