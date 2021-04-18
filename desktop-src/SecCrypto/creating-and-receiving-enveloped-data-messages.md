---
description: Un messaggio in busta digitale è un messaggio crittografato per un destinatario o un set di destinatari.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Creazione e ricezione di messaggi di dati in busta digitale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306470"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a><span data-ttu-id="e94f9-103">Creazione e ricezione di messaggi di dati in busta digitale</span><span class="sxs-lookup"><span data-stu-id="e94f9-103">Creating and Receiving Enveloped Data Messages</span></span>

<span data-ttu-id="e94f9-104">Un messaggio in busta digitale è un messaggio crittografato per un set di destinatari.</span><span class="sxs-lookup"><span data-stu-id="e94f9-104">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="e94f9-105">Nel processo di inviluppo viene generata una chiave di crittografia della sessione e il messaggio viene crittografato con tale chiave.</span><span class="sxs-lookup"><span data-stu-id="e94f9-105">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="e94f9-106">La chiave di crittografia stessa viene quindi crittografata separatamente per ogni destinatario utilizzando le chiavi pubbliche di ogni certificato del destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="e94f9-106">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="e94f9-107">Il messaggio in busta digitale è costituito dal messaggio crittografato, dai certificati dei destinatari desiderati e dal set di chiavi crittografate, uno per ogni destinatario.</span><span class="sxs-lookup"><span data-stu-id="e94f9-107">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="e94f9-108">Il messaggio generato è in formato [*PKCS \# 7*](../secgloss/p-gly.md)/CMS.</span><span class="sxs-lookup"><span data-stu-id="e94f9-108">The message generated is in [*PKCS \#7*](../secgloss/p-gly.md)/CMS format.</span></span>

<span data-ttu-id="e94f9-109">Le sezioni seguenti illustrano le procedure e gli esempi per le attività dei messaggi in busta:</span><span class="sxs-lookup"><span data-stu-id="e94f9-109">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="e94f9-110">Codifica dei dati in busta</span><span class="sxs-lookup"><span data-stu-id="e94f9-110">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)
-   [<span data-ttu-id="e94f9-111">Decodifica dei dati in busta</span><span class="sxs-lookup"><span data-stu-id="e94f9-111">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)
-   [<span data-ttu-id="e94f9-112">Codice alternativo per la codifica di un messaggio in busta digitale</span><span class="sxs-lookup"><span data-stu-id="e94f9-112">Alternate Code for Encoding an Enveloped Message</span></span>](alternate-code-for-encoding-an-enveloped-message.md)
-   [<span data-ttu-id="e94f9-113">Esempio di programma C: codifica di un messaggio firmato in busta</span><span class="sxs-lookup"><span data-stu-id="e94f9-113">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
