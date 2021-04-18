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
# <a name="publicprivate-key-pair-usage"></a><span data-ttu-id="62a61-103">Utilizzo della coppia di chiavi pubblica/privata</span><span class="sxs-lookup"><span data-stu-id="62a61-103">Public/Private Key Pair Usage</span></span>

<span data-ttu-id="62a61-104">Tutte le normali operazioni [*RSA*](../secgloss/r-gly.md)/Schannel e [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel usano la \_ coppia di [*chiavi pubblica/privata*](../secgloss/p-gly.md)di scambio chiavi.</span><span class="sxs-lookup"><span data-stu-id="62a61-104">All normal [*RSA*](../secgloss/r-gly.md)/Schannel and [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel operations use the AT\_KEYEXCHANGE [*public/private key pair*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="62a61-105">Per fornire l' [*autenticazione*](../secgloss/a-gly.md)del server, il lato server delle operazioni Schannel deve avere accesso al certificato [*X. 509*](../secgloss/x-gly.md) che contiene la chiave pubblica e l'accesso alla [*chiave privata*](../secgloss/p-gly.md)corrispondente.</span><span class="sxs-lookup"><span data-stu-id="62a61-105">To provide server [*authentication*](../secgloss/a-gly.md), the server-side of Schannel operations must have access to its [*X.509*](../secgloss/x-gly.md) certificate containing its public key and access to the matching [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="62a61-106">Il lato client di [*Schannel*](../secgloss/s-gly.md) richiede il certificato con la chiave pubblica e l'accesso alla relativa chiave privata se viene implementata l'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="62a61-106">The client-side of [*Schannel*](../secgloss/s-gly.md) needs its certificate with its public key and access to its private key if client authentication is implemented.</span></span>

<span data-ttu-id="62a61-107">Poiché i motori di protocollo Schannel non utilizzano mai la \_ coppia di chiavi pubblica/privata con firma, la coppia di chiavi non deve essere supportata da un nuovo CSP che supporta solo RSA/SChannel o Diffie-Hellman/SChannel.</span><span class="sxs-lookup"><span data-stu-id="62a61-107">Since Schannel protocol engines never use the AT\_SIGNATURE public/private key pair, that key pair need not be supported by a new CSP supporting only RSA/Schannel or Diffie-Hellman/Schannel.</span></span>

<span data-ttu-id="62a61-108">Se un motore di protocollo usa un pacchetto di crittografia di esportazione SSL 3,0 con una coppia di chiavi a chiave di scambio con una lunghezza superiore a \_ 512 bit, il server deve usare una coppia di chiavi RSA aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="62a61-108">If a protocol engine uses an SSL 3.0 export cipher suite with an AT\_KEYEXCHANGE key pair larger than 512 bits, the server must use an additional RSA key pair.</span></span> <span data-ttu-id="62a61-109">Questa coppia di chiavi aggiuntiva è sempre esattamente 512 bit e può essere temporanea.</span><span class="sxs-lookup"><span data-stu-id="62a61-109">This additional key pair is always exactly 512 bits and it can be ephemeral.</span></span> <span data-ttu-id="62a61-110">La coppia viene archiviata come \_ elemento at Key Exchange in un contenitore di chiavi di proprietà del motore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="62a61-110">The pair is stored as an AT\_KEYEXCHANGE element in a key container owned by the protocol engine.</span></span> <span data-ttu-id="62a61-111">Un handle a questo contenitore di chiavi viene in genere acquisito all'avvio del motore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="62a61-111">A handle to this key container is typically acquired at protocol engine startup.</span></span>

<span data-ttu-id="62a61-112">Diffie-Hellman supporta solo [*CALG \_ DH \_ EPHEM*](../secgloss/c-gly.md) e usa le normali chiavi pubbliche RSA o DSS.</span><span class="sxs-lookup"><span data-stu-id="62a61-112">Diffie-Hellman supports only [*CALG\_DH\_EPHEM*](../secgloss/c-gly.md) and uses normal RSA or DSS public keys.</span></span>

 

 
