---
description: Tutte le normali operazioni RSA/SChannel e Diffie-Hellman/SChannel utilizzano la \_ coppia di chiavi pubblica/privata di scambio chiavi.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Utilizzo della coppia di chiavi pubblica/privata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315369"
---
# <a name="publicprivate-key-pair-usage"></a>Utilizzo della coppia di chiavi pubblica/privata

Tutte le normali operazioni [*RSA*](../secgloss/r-gly.md)/Schannel e [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel usano la \_ coppia di [*chiavi pubblica/privata*](../secgloss/p-gly.md)di scambio chiavi. Per fornire l' [*autenticazione*](../secgloss/a-gly.md)del server, il lato server delle operazioni Schannel deve avere accesso al certificato [*X. 509*](../secgloss/x-gly.md) che contiene la chiave pubblica e l'accesso alla [*chiave privata*](../secgloss/p-gly.md)corrispondente. Il lato client di [*Schannel*](../secgloss/s-gly.md) richiede il certificato con la chiave pubblica e l'accesso alla relativa chiave privata se viene implementata l'autenticazione client.

Poiché i motori di protocollo Schannel non utilizzano mai la \_ coppia di chiavi pubblica/privata con firma, la coppia di chiavi non deve essere supportata da un nuovo CSP che supporta solo RSA/SChannel o Diffie-Hellman/SChannel.

Se un motore di protocollo usa un pacchetto di crittografia di esportazione SSL 3,0 con una coppia di chiavi a chiave di scambio con una lunghezza superiore a \_ 512 bit, il server deve usare una coppia di chiavi RSA aggiuntiva. Questa coppia di chiavi aggiuntiva è sempre esattamente 512 bit e può essere temporanea. La coppia viene archiviata come \_ elemento at Key Exchange in un contenitore di chiavi di proprietà del motore del protocollo. Un handle a questo contenitore di chiavi viene in genere acquisito all'avvio del motore del protocollo.

Diffie-Hellman supporta solo [*CALG \_ DH \_ EPHEM*](../secgloss/c-gly.md) e usa le normali chiavi pubbliche RSA o DSS.

 

 
