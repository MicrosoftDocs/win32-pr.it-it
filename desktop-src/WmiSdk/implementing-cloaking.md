---
description: Il cloaking è un'estensione della rappresentazione che consente di controllare meglio il modo in cui COM rappresenta un client su un proxy. Analogamente a molte forme di sicurezza WMI, è possibile impostare il cloaking tramite le interfacce CoSetProxyBlanket e CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementazione del mascheramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232629"
---
# <a name="implementing-cloaking"></a><span data-ttu-id="c0ffc-104">Implementazione del mascheramento</span><span class="sxs-lookup"><span data-stu-id="c0ffc-104">Implementing Cloaking</span></span>

<span data-ttu-id="c0ffc-105">Il cloaking è un'estensione della rappresentazione che consente di controllare meglio il modo in cui COM rappresenta un client su un proxy.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-105">Cloaking is an extension to impersonation that allows for better control over how COM impersonates a client over a proxy.</span></span> <span data-ttu-id="c0ffc-106">Analogamente a molte forme di sicurezza WMI, è possibile impostare il cloaking tramite le interfacce [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="c0ffc-106">Like many forms of WMI security, you set cloaking through the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interfaces.</span></span>

<span data-ttu-id="c0ffc-107">COM offre le seguenti forme di mascheramento:</span><span class="sxs-lookup"><span data-stu-id="c0ffc-107">COM provides the following forms of cloaking:</span></span>

-   <span data-ttu-id="c0ffc-108">Static</span><span class="sxs-lookup"><span data-stu-id="c0ffc-108">Static</span></span>

    <span data-ttu-id="c0ffc-109">COM stabilisce l'identità del token dal thread o dal token del processo nella prima chiamata al proxy.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-109">COM establishes the token identity by the thread or process token on the first call to the proxy.</span></span> <span data-ttu-id="c0ffc-110">Se si usa il cloaking statico con [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), si imposta l'identità del proxy per il ciclo di vita del proxy.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-110">If you use static cloaking with [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), you set the identity of the proxy for the life of the proxy.</span></span>

-   <span data-ttu-id="c0ffc-111">Dynamic</span><span class="sxs-lookup"><span data-stu-id="c0ffc-111">Dynamic</span></span>

    <span data-ttu-id="c0ffc-112">COM ristabilisce l'identità del token dal thread o dal token del processo a ogni chiamata al proxy.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-112">COM reestablishes the token identity from the thread or process token on each call to the proxy.</span></span> <span data-ttu-id="c0ffc-113">Poiché COM controlla l'identità a ogni chiamata, il cloaking dinamico consente un controllo più preciso sull'identità del client.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-113">Because COM checks the identity on each call, dynamic cloaking allows for finer control over the client identity.</span></span> <span data-ttu-id="c0ffc-114">Tuttavia, il mascheramento dinamico è meno efficiente del mascheramento statico.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-114">However, dynamic cloaking is less efficient than static cloaking.</span></span>

<span data-ttu-id="c0ffc-115">Quando si imposta il cloaking insieme al livello di delega della rappresentazione, un server può propagare l'identità di un client tra i server, anche se i server sono remoti.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-115">When you set cloaking in conjunction with the delegation level of impersonation, a server can propagate the identity of a client across servers, even if the servers are remote.</span></span> <span data-ttu-id="c0ffc-116">Se non si Abilita il mascheramento, COM effettua qualsiasi chiamata da un server locale a un server remoto nel contesto del processo server effettivo.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-116">If you do not enable cloaking, COM makes any call from a local server to a remote server under the context of the actual server process.</span></span>

<span data-ttu-id="c0ffc-117">Il mascheramento consente a WMI di rappresentare un client per accedere alle risorse di rete locali e remote tra più limiti del computer.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-117">Cloaking lets WMI impersonate a client to access both local and remote network resources across multiple computer boundaries.</span></span> <span data-ttu-id="c0ffc-118">WMI può passare l'identità del client ai server locali e remoti, ad esempio altre istanze remote di WMI.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-118">WMI can pass the identity of the client to local and remote servers, such as other remote instances of WMI.</span></span> <span data-ttu-id="c0ffc-119">Tali server remoti possono quindi eseguire operazioni nel contesto client iniziale.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-119">Those remote servers can then perform operations under the initial client context.</span></span>

<span data-ttu-id="c0ffc-120">Nella procedura seguente viene descritto come utilizzare il mascheramento e la delega insieme.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-120">The following procedure describes how to use cloaking and delegation together.</span></span>

<span data-ttu-id="c0ffc-121">**Per utilizzare il mascheramento e la delega insieme**</span><span class="sxs-lookup"><span data-stu-id="c0ffc-121">**To use cloaking and delegation together**</span></span>

1.  <span data-ttu-id="c0ffc-122">Impostare il servizio di autenticazione su Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-122">Set the authentication service to Kerberos.</span></span>

    <span data-ttu-id="c0ffc-123">Kerberos è l'unico servizio di autenticazione che supporta il mascheramento e la delega remote.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-123">Kerberos is the only authentication service that supports remote cloaking and delegation.</span></span> <span data-ttu-id="c0ffc-124">Ciò significa che il mascheramento e la delega possono essere utilizzati solo su server remoti.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-124">This means that cloaking and delegation can only be used on remote servers.</span></span>

2.  <span data-ttu-id="c0ffc-125">Contrassegnare l'account di accesso del server come "trusted per la delega" nei servizi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-125">Mark the server login account as "Trusted for Delegation" in the Active Directory services.</span></span>
3.  <span data-ttu-id="c0ffc-126">Contrassegnare l'account di accesso client come "l'account è sensibile e non può essere delegato" nei servizi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-126">Mark the client login account as "Account is sensitive and cannot be delegated" in Active Directory services.</span></span>

<span data-ttu-id="c0ffc-127">Ad esempio, una chiamata al provider di visualizzazione, che può restituire oggetti da più istanze di WMI su più computer, può trarre vantaggio dalla delega e dal mascheramento.</span><span class="sxs-lookup"><span data-stu-id="c0ffc-127">For example, a call to the View Provider, which may return objects from multiple instances of WMI on multiple computers, can benefit from delegation and cloaking.</span></span>

 

 
