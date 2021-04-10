---
title: Utilizzo di Transport-Level sicurezza sul client
description: Il client specifica il modo in cui il server rappresenta il client quando il client stabilisce l'associazione di stringa.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- RPC (Remote Procedure Call), attività, uso della sicurezza a livello di trasporto nel client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963379"
---
# <a name="using-transport-level-security-on-the-client"></a><span data-ttu-id="af02f-104">Utilizzo di Transport-Level sicurezza sul client</span><span class="sxs-lookup"><span data-stu-id="af02f-104">Using Transport-Level Security on the Client</span></span>

<span data-ttu-id="af02f-105">Il client specifica il modo in cui il server rappresenta il client quando il client stabilisce l'associazione di stringa.</span><span class="sxs-lookup"><span data-stu-id="af02f-105">The client specifies how the server impersonates the client when the client establishes the string binding.</span></span> <span data-ttu-id="af02f-106">Queste informazioni QOS vengono fornite come opzione endpoint nell'associazione di stringa.</span><span class="sxs-lookup"><span data-stu-id="af02f-106">This QOS information is provided as an endpoint option in the string binding.</span></span> <span data-ttu-id="af02f-107">Il client può specificare il livello di rappresentazione, il rilevamento statico o dinamico e il flag solo valido.</span><span class="sxs-lookup"><span data-stu-id="af02f-107">The client can specify the level of impersonation, dynamic or static tracking, and the effective-only flag.</span></span>

<span data-ttu-id="af02f-108">**Per fornire informazioni sulla qualità del servizio per il server**</span><span class="sxs-lookup"><span data-stu-id="af02f-108">**To supply quality-of-service information for the server**</span></span>

1.  <span data-ttu-id="af02f-109">Il client chiama [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) per creare le stringhe dei componenti, incluse le opzioni dell'endpoint, nel contesto di associazione stringa corretto.</span><span class="sxs-lookup"><span data-stu-id="af02f-109">The client calls [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) to create the component strings, including endpoint options, in the correct string-binding context.</span></span>
2.  <span data-ttu-id="af02f-110">Il client chiama [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per ottenere un nuovo handle di associazione e per applicare le informazioni di qualità del servizio per il client.</span><span class="sxs-lookup"><span data-stu-id="af02f-110">The client calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain a new binding handle and to apply the quality-of-service information for the client.</span></span>
3.  <span data-ttu-id="af02f-111">Il client effettua chiamate a procedure remote usando l'handle.</span><span class="sxs-lookup"><span data-stu-id="af02f-111">The client makes remote procedure calls using the handle.</span></span>

<span data-ttu-id="af02f-112">Microsoft RPC supporta le funzionalità di sicurezza di Windows solo in [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) e [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="af02f-112">Microsoft RPC supports Windows security features only on [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) and [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="af02f-113">Le opzioni di sicurezza per gli altri trasporti vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="af02f-113">Security options for other transports are ignored.</span></span>

<span data-ttu-id="af02f-114">Il client può associare i seguenti parametri di sicurezza al binding per il trasporto named pipe [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) o [**ncalrpc**](/windows/desktop/Midl/ncalrpc):</span><span class="sxs-lookup"><span data-stu-id="af02f-114">The client can associate the following security parameters to the binding for the named-pipe transport [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) or [**ncalrpc**](/windows/desktop/Midl/ncalrpc):</span></span>

-   <span data-ttu-id="af02f-115">Identificazione, rappresentazione o anonima.</span><span class="sxs-lookup"><span data-stu-id="af02f-115">Identification, Impersonation, or Anonymous.</span></span> <span data-ttu-id="af02f-116">Specifica il tipo di sicurezza utilizzato.</span><span class="sxs-lookup"><span data-stu-id="af02f-116">Specifies the type of security used.</span></span> <span data-ttu-id="af02f-117">Il valore predefinito è rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="af02f-117">The default is Impersonation.</span></span>
-   <span data-ttu-id="af02f-118">Statico o dinamico.</span><span class="sxs-lookup"><span data-stu-id="af02f-118">Dynamic or Static.</span></span> <span data-ttu-id="af02f-119">Determina se le informazioni di sicurezza associate a un thread sono una copia delle informazioni di sicurezza create nel momento in cui viene eseguita la chiamata di procedura remota (statica) o un puntatore alle informazioni di sicurezza (dinamico).</span><span class="sxs-lookup"><span data-stu-id="af02f-119">Determines whether security information associated with a thread is a copy of the security information created at the time the remote procedure call is made (static) or a pointer to the security information (dynamic).</span></span>

    <span data-ttu-id="af02f-120">Le informazioni di sicurezza statiche non cambiano.</span><span class="sxs-lookup"><span data-stu-id="af02f-120">Static security information does not change.</span></span> <span data-ttu-id="af02f-121">L'impostazione dinamica riflette le impostazioni di sicurezza correnti, comprese le modifiche apportate dopo la chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="af02f-121">The dynamic setting reflects the current security settings, including changes made after the remote procedure call is made.</span></span> <span data-ttu-id="af02f-122">Per [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), il valore predefinito per le connessioni named pipe remote è statico, per le connessioni named pipe locali il valore predefinito è Dynamic.</span><span class="sxs-lookup"><span data-stu-id="af02f-122">For [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), the default for remote named pipe connections is static, for local named pipe connections the default is dynamic.</span></span>

-   <span data-ttu-id="af02f-123">**True** o **false**.</span><span class="sxs-lookup"><span data-stu-id="af02f-123">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="af02f-124">Specifica il valore del flag solo valido.</span><span class="sxs-lookup"><span data-stu-id="af02f-124">Specifies the value of the effective-only flag.</span></span> <span data-ttu-id="af02f-125">Il valore **true** indica che solo i privilegi di token impostati su on al momento della chiamata sono validi.</span><span class="sxs-lookup"><span data-stu-id="af02f-125">A value of **TRUE** indicates that only token privileges set to on at the time of the call are effective.</span></span> <span data-ttu-id="af02f-126">Il valore **false** indica che tutti i privilegi sono disponibili e che l'applicazione può modificarli.</span><span class="sxs-lookup"><span data-stu-id="af02f-126">A value of **FALSE** indicates that all privileges are available and that the application can modify them.</span></span>

<span data-ttu-id="af02f-127">Qualsiasi combinazione di queste impostazioni può essere assegnata all'associazione, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="af02f-127">Any combination of these settings can be assigned to the binding, as shown in the following example:</span></span>

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

<span data-ttu-id="af02f-128">Le impostazioni predefinite dei parametri di sicurezza variano in base al protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="af02f-128">Default security-parameter settings vary according to the transport protocol.</span></span>

<span data-ttu-id="af02f-129">Per ulteriori informazioni sulla sintassi delle opzioni dell'endpoint, vedere [endpoint](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="af02f-129">For additional information about the syntax of the endpoint options, see [endpoint](/windows/desktop/Midl/endpoint).</span></span>

 

 