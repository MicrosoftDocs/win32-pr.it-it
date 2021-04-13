---
description: Il messaggio in busta digitale è costituito dal messaggio crittografato, dai certificati dei destinatari desiderati e dal set di chiavi crittografate, uno per ogni destinatario. Il messaggio generato è in \# formato PKCS 7/cms.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Creazione e ricezione di messaggi di dati in busta digitale in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343151"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a><span data-ttu-id="f18a8-104">Creazione e ricezione di messaggi di dati in busta digitale in CAPICOM</span><span class="sxs-lookup"><span data-stu-id="f18a8-104">Creating and Receiving Enveloped Data Messages in CAPICOM</span></span>

<span data-ttu-id="f18a8-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f18a8-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f18a8-106">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f18a8-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="f18a8-107">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="f18a8-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="f18a8-108">Un messaggio in busta digitale è un messaggio crittografato per un set di destinatari.</span><span class="sxs-lookup"><span data-stu-id="f18a8-108">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="f18a8-109">Nel processo di inviluppo viene generata una chiave di crittografia della sessione e il messaggio viene crittografato con tale chiave.</span><span class="sxs-lookup"><span data-stu-id="f18a8-109">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="f18a8-110">La chiave di crittografia stessa viene quindi crittografata separatamente per ogni destinatario utilizzando le chiavi pubbliche di ogni certificato del destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="f18a8-110">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="f18a8-111">Il messaggio in busta digitale è costituito dal messaggio crittografato, dai certificati dei destinatari desiderati e dal set di chiavi crittografate, uno per ogni destinatario.</span><span class="sxs-lookup"><span data-stu-id="f18a8-111">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="f18a8-112">Il messaggio generato è in \# formato PKCS 7/cms.</span><span class="sxs-lookup"><span data-stu-id="f18a8-112">The message generated is in PKCS \#7/CMS format.</span></span>

<span data-ttu-id="f18a8-113">Le sezioni seguenti illustrano le procedure e gli esempi per le attività dei messaggi in busta:</span><span class="sxs-lookup"><span data-stu-id="f18a8-113">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="f18a8-114">Invio di un messaggio di dati in busta</span><span class="sxs-lookup"><span data-stu-id="f18a8-114">Sending an Enveloped Data Message</span></span>](sending-an-enveloped-data-message.md)
-   [<span data-ttu-id="f18a8-115">Ricezione di un messaggio di dati in busta</span><span class="sxs-lookup"><span data-stu-id="f18a8-115">Receiving an Enveloped Data Message</span></span>](receiving-an-enveloped-data-message.md)

 

 



