---
description: Esistono due ingredienti per determinare il comportamento di rappresentazione dell'autorità che il client concede in modo esplicito al server tramite un livello di rappresentazione e la capacità dei server di mascherare la propria identità quando effettuano chiamate per conto dei client.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Mascheramento (Servizi componenti)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748082"
---
# <a name="cloaking-component-services"></a><span data-ttu-id="fab62-103">Mascheramento (Servizi componenti)</span><span class="sxs-lookup"><span data-stu-id="fab62-103">Cloaking (Component Services)</span></span>

<span data-ttu-id="fab62-104">Esistono due ingredienti per determinare il comportamento della rappresentazione: l'autorità che il client concede in modo esplicito il server attraverso un livello di rappresentazione e la capacità del server di mascherare la propria identità quando effettuano chiamate per conto del client.</span><span class="sxs-lookup"><span data-stu-id="fab62-104">There are two ingredients in determining the behavior of impersonation: the authority the client explicitly grants the server through an impersonation level and the server's ability to mask its own identity when making calls on the client's behalf.</span></span> <span data-ttu-id="fab62-105">Questa seconda funzionalità è nota come *mascheramento*.</span><span class="sxs-lookup"><span data-stu-id="fab62-105">This latter capability is known as *cloaking*.</span></span> <span data-ttu-id="fab62-106">Il cloaking ha a che fare con l'identità di sicurezza in cui il server effettua le chiamate.</span><span class="sxs-lookup"><span data-stu-id="fab62-106">Cloaking has to do with the security identity under which the server makes calls.</span></span>

<span data-ttu-id="fab62-107">Quando il server rappresenta il client, ha accesso diretto alle credenziali di sicurezza del client.</span><span class="sxs-lookup"><span data-stu-id="fab62-107">When the server impersonates the client, it has direct access to the client's security credentials.</span></span> <span data-ttu-id="fab62-108">In un senso molto locale, il thread del server acquisisce l'identità del client.</span><span class="sxs-lookup"><span data-stu-id="fab62-108">In a very local sense, the server thread takes on the identity of the client.</span></span> <span data-ttu-id="fab62-109">Tuttavia, quando il server effettua chiamate all'esterno del processo, l'identità del client non verrà necessariamente proiettata come identità con cui viene effettuata la chiamata.</span><span class="sxs-lookup"><span data-stu-id="fab62-109">But when the server makes calls outside of its process, the client identity will not necessarily be projected as the identity under which the call is made.</span></span>

<span data-ttu-id="fab62-110">Quando il mascheramento è abilitato, le chiamate effettuate dal server che rappresenta il client possono essere effettuate con l'identità del client.</span><span class="sxs-lookup"><span data-stu-id="fab62-110">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="fab62-111">Quando il mascheramento è disabilitato, le chiamate dal server verranno effettuate nell'identità del server.</span><span class="sxs-lookup"><span data-stu-id="fab62-111">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

<span data-ttu-id="fab62-112">Sono inoltre disponibili due forme di mascheramento, mascheramento *statico* e *mascheramento dinamico*, che possono essere descritte come segue:</span><span class="sxs-lookup"><span data-stu-id="fab62-112">Moreover, there are two forms of cloaking, *static cloaking* and *dynamic cloaking*, which can be described as follows:</span></span>

-   <span data-ttu-id="fab62-113">Rappresentazione con mascheramento statico.</span><span class="sxs-lookup"><span data-stu-id="fab62-113">Impersonation with static cloaking.</span></span> <span data-ttu-id="fab62-114">L'identità client originale (realizzata come token del thread del server) può essere presentata una volta a un server downstream in una chiamata usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), impostando l'identità client originale una volta sul proxy e il token del thread verrà usato nelle chiamate al metodo successive.</span><span class="sxs-lookup"><span data-stu-id="fab62-114">The original client identity (realized as the server thread token) can be presented once to a downstream server on a call using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), setting the original client identity once on the proxy, and that thread token will be used on subsequent method calls.</span></span>
-   <span data-ttu-id="fab62-115">Rappresentazione con mascheramento dinamico.</span><span class="sxs-lookup"><span data-stu-id="fab62-115">Impersonation with dynamic cloaking.</span></span> <span data-ttu-id="fab62-116">L'identità client originale viene individuata come token del thread del server per ogni chiamata al metodo al server downstream.</span><span class="sxs-lookup"><span data-stu-id="fab62-116">The original client identity is discovered as the server thread token on each method call to the downstream server.</span></span> <span data-ttu-id="fab62-117">In effetti, l'identità presentata può essere determinata dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="fab62-117">In effect, the identity that is presented can be determined dynamically.</span></span> <span data-ttu-id="fab62-118">L'overhead necessario per eseguire questa operazione può essere notevolmente più costoso.</span><span class="sxs-lookup"><span data-stu-id="fab62-118">The overhead required to do this can be considerably more expensive.</span></span>

<span data-ttu-id="fab62-119">Per le applicazioni COM+, la configurazione predefinita è per la funzionalità di mascheramento dinamico.</span><span class="sxs-lookup"><span data-stu-id="fab62-119">For COM+ applications, the default configuration is for dynamic cloaking capability.</span></span> <span data-ttu-id="fab62-120">Questa operazione può essere modificata a livello di programmazione e amministrativa.</span><span class="sxs-lookup"><span data-stu-id="fab62-120">This can be changed programmatically and administratively.</span></span> <span data-ttu-id="fab62-121">Sebbene il mascheramento dinamico possa avere un sovraccarico delle prestazioni, offre la flessibilità che in genere è necessaria per circostanze che richiedono l'uso della rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="fab62-121">While dynamic cloaking can have performance overhead, it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

<span data-ttu-id="fab62-122">Per informazioni più dettagliate sul mascheramento e descrizioni precise dei comportamenti possibili, vedere [mascheramento](/windows/desktop/com/cloaking) nella documentazione com.</span><span class="sxs-lookup"><span data-stu-id="fab62-122">For more detail regarding cloaking and precise descriptions of possible behaviors, see [Cloaking](/windows/desktop/com/cloaking) in the COM documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fab62-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fab62-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fab62-124">Rappresentazione e delega client</span><span class="sxs-lookup"><span data-stu-id="fab62-124">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="fab62-125">Requisiti lato client per la rappresentazione</span><span class="sxs-lookup"><span data-stu-id="fab62-125">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="fab62-126">Requisiti lato server per la rappresentazione</span><span class="sxs-lookup"><span data-stu-id="fab62-126">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
