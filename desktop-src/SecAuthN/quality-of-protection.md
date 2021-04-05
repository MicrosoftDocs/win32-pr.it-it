---
description: La qualità della protezione, identificata dalla direttiva qop, viene innanzitutto specificata dal server nella richiesta digest e quindi confermata dal client nella risposta alla richiesta di verifica.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualità della protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058070"
---
# <a name="quality-of-protection"></a><span data-ttu-id="16bd3-103">Qualità della protezione</span><span class="sxs-lookup"><span data-stu-id="16bd3-103">Quality of Protection</span></span>

<span data-ttu-id="16bd3-104">La qualità della protezione, identificata dalla direttiva qop, viene innanzitutto specificata dal server nella richiesta digest e quindi confermata dal client nella risposta alla richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="16bd3-104">The quality of protection, identified by the qop directive, is first specified by the server in the Digest challenge, and then confirmed by the client in the challenge response.</span></span> <span data-ttu-id="16bd3-105">Se il client richiede una qualità di protezione non supportata dal server, il client deve terminare l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="16bd3-105">If the client requires a quality of protection that the server does not support, the client must terminate the authentication.</span></span>

<span data-ttu-id="16bd3-106">I valori possibili per la direttiva qop sono descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="16bd3-106">The possible values for the qop directive are described in the following table.</span></span>



| <span data-ttu-id="16bd3-107">Valore</span><span class="sxs-lookup"><span data-stu-id="16bd3-107">Value</span></span>                   | <span data-ttu-id="16bd3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16bd3-108">Description</span></span>                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16bd3-109">autenticazione</span><span class="sxs-lookup"><span data-stu-id="16bd3-109">"auth"</span></span>                  | <span data-ttu-id="16bd3-110">Solo autenticazione.</span><span class="sxs-lookup"><span data-stu-id="16bd3-110">Authentication only.</span></span>                                                                                                                         |
| <span data-ttu-id="16bd3-111">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="16bd3-111">"auth-int"</span></span>              | <span data-ttu-id="16bd3-112">Autenticazione e controllo dell' [*integrità*](../secgloss/i-gly.md) mediante le firme.</span><span class="sxs-lookup"><span data-stu-id="16bd3-112">Authentication and [*integrity*](../secgloss/i-gly.md) checking using signatures.</span></span>                  |
| <span data-ttu-id="16bd3-113">(Solo SASL) "auth-conf"</span><span class="sxs-lookup"><span data-stu-id="16bd3-113">(SASL only) "auth-conf"</span></span> | <span data-ttu-id="16bd3-114">Autenticazione, verifica dell'integrità e della riservatezza mediante le firme e la crittografia.</span><span class="sxs-lookup"><span data-stu-id="16bd3-114">Authentication, integrity and confidentiality checking by using signatures and encryption.</span></span> <span data-ttu-id="16bd3-115">Per ulteriori informazioni, vedere [crittografie](ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="16bd3-115">For more information, see [Ciphers](ciphers.md).</span></span> |



 

<span data-ttu-id="16bd3-116">La qualità della protezione è determinata dai flag dei requisiti di contesto passati al SSP Microsoft Digest.</span><span class="sxs-lookup"><span data-stu-id="16bd3-116">Quality of protection is determined by context requirement flags passed to the Microsoft Digest SSP.</span></span> <span data-ttu-id="16bd3-117">Nella tabella seguente sono elencati i flag relativi alla qualità della protezione e il valore risultante della direttiva qop.</span><span class="sxs-lookup"><span data-stu-id="16bd3-117">The following table lists the flags related to quality of protection, and the resulting value of the qop directive.</span></span>



| <span data-ttu-id="16bd3-118">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="16bd3-118">Flag</span></span>                         | <span data-ttu-id="16bd3-119">valore qop</span><span class="sxs-lookup"><span data-stu-id="16bd3-119">qop value</span></span>               |
|------------------------------|-------------------------|
| <span data-ttu-id="16bd3-120">*Xxx* \_ \_riservatezza richieste</span><span class="sxs-lookup"><span data-stu-id="16bd3-120">*XXX*\_REQ\_CONFIDENTIALITY</span></span>  | <span data-ttu-id="16bd3-121">"auth-conf" (solo SASL)</span><span class="sxs-lookup"><span data-stu-id="16bd3-121">"auth-conf" (SASL only)</span></span> |
| <span data-ttu-id="16bd3-122">*Xxx* \_ \_rilevamento riproduzione req \_</span><span class="sxs-lookup"><span data-stu-id="16bd3-122">*XXX*\_REQ\_REPLAY\_DETECT</span></span>   | <span data-ttu-id="16bd3-123">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="16bd3-123">"auth-int"</span></span>              |
| <span data-ttu-id="16bd3-124">*Xxx* \_ \_rilevamento sequenza \_ req</span><span class="sxs-lookup"><span data-stu-id="16bd3-124">*XXX*\_REQ\_SEQUENCE\_DETECT</span></span> | <span data-ttu-id="16bd3-125">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="16bd3-125">"auth-int"</span></span>              |
| <span data-ttu-id="16bd3-126">*Xxx* \_ \_integrità req</span><span class="sxs-lookup"><span data-stu-id="16bd3-126">*XXX*\_REQ\_INTEGRITY</span></span>        | <span data-ttu-id="16bd3-127">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="16bd3-127">"auth-int"</span></span>              |
| <span data-ttu-id="16bd3-128">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="16bd3-128">(none)</span></span>                       | <span data-ttu-id="16bd3-129">autenticazione</span><span class="sxs-lookup"><span data-stu-id="16bd3-129">"auth"</span></span>                  |



 

> [!Note]  
> <span data-ttu-id="16bd3-130">I flag del requisito di contesto specificati dalle applicazioni server hanno un prefisso ASC e quelli specificati dai client sono preceduti da ISC.</span><span class="sxs-lookup"><span data-stu-id="16bd3-130">Context requirement flags specified by server applications have a prefix of ASC, and those specified by clients are prefixed with ISC.</span></span> <span data-ttu-id="16bd3-131">Per determinare i valori dei flag usati dall'applicazione, sostituire uno di questi prefissi per *xxx*.</span><span class="sxs-lookup"><span data-stu-id="16bd3-131">To determine the flag values used by your application, substitute one of these prefixes for *XXX*.</span></span>

 

<span data-ttu-id="16bd3-132">Per informazioni aggiuntive relative al server, vedere [generazione della richiesta digest](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="16bd3-132">For additional server-related information, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

<span data-ttu-id="16bd3-133">Per informazioni aggiuntive relative al client, vedere [generazione della risposta alla richiesta digest](generating-the-digest-challenge-response.md).</span><span class="sxs-lookup"><span data-stu-id="16bd3-133">For additional client-related information, see [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).</span></span>

 

 
