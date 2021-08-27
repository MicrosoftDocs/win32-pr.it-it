---
title: Scelta del tipo di handle di associazione da utilizzare
description: Scelta del tipo di handle di associazione da utilizzare
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd35286a5bb88be3094238e0e4c43b701826bca0a7e5ad02d35c5f87f0cbdaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022921"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Scelta del tipo di handle di associazione da utilizzare

**Procedura consigliata:** Se si conosce il server che verrà utilizzato dall'applicazione, usare handle espliciti. In caso contrario, usare il costrutto di handle espliciti ogni volta oppure usare handle generici **\_ con** routine bind **\_ e unbind.**

Non usare handle impliciti o handle automatici. Gli handle impliciti non sono thread-safe e, anche thread safety possono sembrare superflui, potrebbero diventare necessari in un secondo momento. Gli handle automatici hanno un sovraccarico elevato e richiedono una grande quantità di configurazione per funzionare correttamente. Le funzionalità di ricerca sono state sostituite dai servizi Active Directory.

Gli handle espliciti sono altamente efficienti e molte funzionalità interessanti sono disponibili solo per gli handle espliciti. Ad esempio, se più chiamate RPC verranno effettuate nello stesso server, è possibile costruire l'handle di associazione una sola volta ed eseguire tutte le chiamate con esso. Questo approccio è molto più efficiente rispetto a qualsiasi altro metodo. Se il server a cui verrà passata la chiamata è sconosciuto, costruire un handle di associazione esplicito per ogni chiamata o usare handle di associazione generici.

In Microsoft™ Windows XP, il tempo di esecuzione RPC è piuttosto efficiente nel ri-uso e nella memorizzazione nella cache delle chiamate, quindi se la chiamata  *n*+1 finisce sullo stesso server della chiamata *n* th, RPC usa nuovamente le risorse allocate per l'esima chiamata, aggirando la necessità di memorizzare nella cache gli handle di associazione per migliorare le prestazioni.

 

 




