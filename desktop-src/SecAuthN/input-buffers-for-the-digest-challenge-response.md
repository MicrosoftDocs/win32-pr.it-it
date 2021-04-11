---
description: Per l'autenticazione HTTP con Microsoft Digest sono necessari tre buffer di input per generare una risposta di verifica. Nella tabella seguente vengono riepilogati i buffer.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Buffer di input per la risposta di verifica del digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128306"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a><span data-ttu-id="ad5da-104">Buffer di input per la risposta di verifica del digest</span><span class="sxs-lookup"><span data-stu-id="ad5da-104">Input Buffers for the Digest Challenge Response</span></span>

<span data-ttu-id="ad5da-105">Per l'autenticazione HTTP con Microsoft Digest sono necessari tre buffer di input per generare una risposta di verifica.</span><span class="sxs-lookup"><span data-stu-id="ad5da-105">HTTP authentication using Microsoft Digest requires three input buffers to generate a challenge response.</span></span> <span data-ttu-id="ad5da-106">Nella tabella seguente vengono riepilogati i buffer.</span><span class="sxs-lookup"><span data-stu-id="ad5da-106">The following table summarizes these buffers.</span></span>



| <span data-ttu-id="ad5da-107">Numero buffer</span><span class="sxs-lookup"><span data-stu-id="ad5da-107">Buffer number</span></span> | <span data-ttu-id="ad5da-108">Contiene</span><span class="sxs-lookup"><span data-stu-id="ad5da-108">Contains</span></span>                                                                                                                                             | <span data-ttu-id="ad5da-109">Tipo di buffer</span><span class="sxs-lookup"><span data-stu-id="ad5da-109">Buffer type</span></span>                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ad5da-110">0</span><span class="sxs-lookup"><span data-stu-id="ad5da-110">0</span></span>             | <span data-ttu-id="ad5da-111">Richiesta di verifica ricevuta dal server</span><span class="sxs-lookup"><span data-stu-id="ad5da-111">Challenge received from the Server</span></span>                                                                                                                   | <span data-ttu-id="ad5da-112">\_token SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="ad5da-112">SECBUFFER\_TOKEN</span></span>                                            |
| <span data-ttu-id="ad5da-113">1</span><span class="sxs-lookup"><span data-stu-id="ad5da-113">1</span></span>             | <span data-ttu-id="ad5da-114">Metodo HTTP</span><span class="sxs-lookup"><span data-stu-id="ad5da-114">HTTP Method</span></span>                                                                                                                                          | <span data-ttu-id="ad5da-115">\_parametri SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="ad5da-115">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="ad5da-116">2</span><span class="sxs-lookup"><span data-stu-id="ad5da-116">2</span></span>             | <span data-ttu-id="ad5da-117">H (entità)</span><span class="sxs-lookup"><span data-stu-id="ad5da-117">H(Entity)</span></span>                                                                                                                                            | <span data-ttu-id="ad5da-118">\_parametri SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="ad5da-118">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="ad5da-119">3</span><span class="sxs-lookup"><span data-stu-id="ad5da-119">3</span></span>             | <span data-ttu-id="ad5da-120">[*Nome dell'entità servizio*](../secgloss/s-gly.md) (SPN) del server di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ad5da-120">The [*service principal name*](../secgloss/s-gly.md) (SPN) of the target server.</span></span> | <span data-ttu-id="ad5da-121">**SECBUFFER \_ \_host di destinazione** \| **SECBUFFER \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="ad5da-121">**SECBUFFER\_TARGET\_HOST** \| **SECBUFFER\_READONLY**</span></span>      |
| <span data-ttu-id="ad5da-122">4</span><span class="sxs-lookup"><span data-stu-id="ad5da-122">4</span></span>             | <span data-ttu-id="ad5da-123">Valori dei token delle associazioni di canale</span><span class="sxs-lookup"><span data-stu-id="ad5da-123">Channel bindings token values</span></span>                                                                                                                        | <span data-ttu-id="ad5da-124">**SECBUFFER \_ \_associazioni di canale** \| **SECBUFFER \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="ad5da-124">**SECBUFFER\_CHANNEL\_BINDINGS** \| **SECBUFFER\_READONLY**</span></span> |



 

<span data-ttu-id="ad5da-125">Il buffer zero contiene la richiesta digest ricevuta dal server in risposta alla richiesta iniziale di una risorsa protetta da Access.</span><span class="sxs-lookup"><span data-stu-id="ad5da-125">Buffer zero contains the Digest challenge received from the server in response to the initial request for an access-protected resource.</span></span>

<span data-ttu-id="ad5da-126">Il buffer 1 contiene la rappresentazione di stringa del metodo, ad esempio "GET" o "POST".</span><span class="sxs-lookup"><span data-stu-id="ad5da-126">Buffer 1 contains the string representation of the method, such as "GET" or "POST".</span></span> <span data-ttu-id="ad5da-127">Il metodo viene usato nel calcolo di a2, come descritto in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span><span class="sxs-lookup"><span data-stu-id="ad5da-127">The method is used in the calculation of A2, as described in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span></span>

<span data-ttu-id="ad5da-128">Buffer 2 è l'hash [*MD5*](../secgloss/m-gly.md) del corpo entità del messaggio, come descritto nella RFC 2617.</span><span class="sxs-lookup"><span data-stu-id="ad5da-128">Buffer 2 is the [*MD5*](../secgloss/m-gly.md) hash of the message's entity-body as described in RFC 2617.</span></span>

<span data-ttu-id="ad5da-129">Il buffer 3 contiene il nome SPN del server di destinazione in formato UTF-8 quando il digest viene utilizzato con le associazioni di canale.</span><span class="sxs-lookup"><span data-stu-id="ad5da-129">Buffer 3 contains the SPN of the target server in UTF-8 formatting when Digest is used with channel bindings.</span></span>

<span data-ttu-id="ad5da-130">Il buffer 4 contiene il valore del token di associazione del canale quando il digest viene utilizzato con le associazioni di canale.</span><span class="sxs-lookup"><span data-stu-id="ad5da-130">Buffer 4 contains the channel binding token value when Digest is used with channel bindings.</span></span>

## <a name="input-buffers-for-sasl"></a><span data-ttu-id="ad5da-131">Buffer di input per SASL</span><span class="sxs-lookup"><span data-stu-id="ad5da-131">Input Buffers for SASL</span></span>

<span data-ttu-id="ad5da-132">Specificare solo il buffer zero.</span><span class="sxs-lookup"><span data-stu-id="ad5da-132">Supply buffer zero only.</span></span> <span data-ttu-id="ad5da-133">Per la compatibilità con altri SSP, è possibile chiamare [**InitializeSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) senza una richiesta server valida.</span><span class="sxs-lookup"><span data-stu-id="ad5da-133">For compatibility with other SSPs, you may call [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) without a valid server challenge.</span></span> <span data-ttu-id="ad5da-134">In questo caso il parametro *Pinput* deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="ad5da-134">In this case the *pInput* parameter should be set to **NULL**.</span></span>

 

 
