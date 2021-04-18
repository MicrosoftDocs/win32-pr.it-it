---
description: I nomi di peer vengono utilizzati dal protocollo PNRP (Peer Name Resolution Protocol), da peer Identity Manager e dall'infrastruttura di raggruppamento peer.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Nomi di peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312240"
---
# <a name="peer-names"></a><span data-ttu-id="25ca6-103">Nomi di peer</span><span class="sxs-lookup"><span data-stu-id="25ca6-103">Peer Names</span></span>

<span data-ttu-id="25ca6-104">I nomi di peer vengono utilizzati dal protocollo PNRP (Peer Name Resolution Protocol), da peer Identity Manager e dall'infrastruttura di raggruppamento peer.</span><span class="sxs-lookup"><span data-stu-id="25ca6-104">Peer names are used by Peer Name Resolution Protocol (PNRP), the Peer Identity Manager, and the Peer Grouping Infrastructure.</span></span> <span data-ttu-id="25ca6-105">I nomi dei peer sono nomi stabili per le risorse, ad esempio computer, utenti, gruppi o servizi.</span><span class="sxs-lookup"><span data-stu-id="25ca6-105">Peer names are stable names for resources such as computers, users, groups, or services.</span></span> <span data-ttu-id="25ca6-106">PNRP usa i nomi dei peer per identificare i nodi in una rete peer.</span><span class="sxs-lookup"><span data-stu-id="25ca6-106">PNRP uses peer names to identify nodes in a peer network.</span></span>

> [!Note]  
> <span data-ttu-id="25ca6-107">Un endpoint utilizzato dall'infrastruttura peer è in realtà una tupla costituita da un indirizzo IPv4 o IPv6, una porta e un protocollo (TCP o UDP).</span><span class="sxs-lookup"><span data-stu-id="25ca6-107">An endpoint that the Peer Infrastructure uses is actually a tuple that consists of an IPv4 or IPv6 address, port, and protocol (either TCP or UDP).</span></span> <span data-ttu-id="25ca6-108">Un nome peer può avere più di una tupla.</span><span class="sxs-lookup"><span data-stu-id="25ca6-108">One peer name can have more than one tuple.</span></span>

 

<span data-ttu-id="25ca6-109">Un nome peer è una stringa di testo con il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="25ca6-109">A peer name is a text string that has the following format:</span></span>

-   <span data-ttu-id="25ca6-110">"Authority. Classificator"</span><span class="sxs-lookup"><span data-stu-id="25ca6-110">"Authority.Classifier"</span></span>

<span data-ttu-id="25ca6-111">Il valore di un'autorità varia a seconda che il nome sia protetto o non protetto.</span><span class="sxs-lookup"><span data-stu-id="25ca6-111">The value of an Authority depends on whether the name is secure or unsecured.</span></span> <span data-ttu-id="25ca6-112">Il classificatore di un nome peer è una stringa.</span><span class="sxs-lookup"><span data-stu-id="25ca6-112">The Classifier of a peer name is a string.</span></span> <span data-ttu-id="25ca6-113">Un classificatore può essere un qualsiasi nome che contiene 150 o meno caratteri UNICODE.</span><span class="sxs-lookup"><span data-stu-id="25ca6-113">A Classifier can be any name that contains 150 or less UNICODE characters.</span></span> <span data-ttu-id="25ca6-114">I nomi di peer fanno distinzione tra maiuscole e minuscole e possono essere registrati come protetti o non protetti.</span><span class="sxs-lookup"><span data-stu-id="25ca6-114">Peer names are case-sensitive and can be registered as secured or unsecured.</span></span> <span data-ttu-id="25ca6-115">L'elenco seguente identifica alcuni esempi di nomi peer:</span><span class="sxs-lookup"><span data-stu-id="25ca6-115">The following list identifies some examples of peer names:</span></span>

-   <span data-ttu-id="25ca6-116">"0. MyUnsecuredPeerName"</span><span class="sxs-lookup"><span data-stu-id="25ca6-116">"0.MyUnsecuredPeerName"</span></span>
-   <span data-ttu-id="25ca6-117">"0. JohnDoe. Games"</span><span class="sxs-lookup"><span data-stu-id="25ca6-117">"0.JohnDoe.Games"</span></span>
-   <span data-ttu-id="25ca6-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d. JohnDoe</span><span class="sxs-lookup"><span data-stu-id="25ca6-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d.JohnDoe"</span></span>

## <a name="secure-peer-names"></a><span data-ttu-id="25ca6-119">Nomi peer sicuri</span><span class="sxs-lookup"><span data-stu-id="25ca6-119">Secure Peer Names</span></span>

<span data-ttu-id="25ca6-120">Per un nome sicuro, l'autorità è l'hash SHA (Secure Hash Algorithm) della chiave pubblica del nome peer e restituisce una stringa esadecimale di 40 caratteri.</span><span class="sxs-lookup"><span data-stu-id="25ca6-120">For a secure name, the Authority is the Secure Hash Algorithm (SHA) hash of the public key of the peer name, and results in a 40 character hexadecimal string.</span></span> <span data-ttu-id="25ca6-121">Un nome peer sicuro può essere registrato solo con PNRP dal proprietario o dal delegato del proprietario del nome peer.</span><span class="sxs-lookup"><span data-stu-id="25ca6-121">A secure peer name can only be registered with PNRP by the owner or delegate of the peer name owner.</span></span> <span data-ttu-id="25ca6-122">È necessario creare un nome peer protetto chiamando [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span><span class="sxs-lookup"><span data-stu-id="25ca6-122">A secured peer name must be created by calling [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span></span>

## <a name="unsecured-peer-names"></a><span data-ttu-id="25ca6-123">Nomi peer non protetti</span><span class="sxs-lookup"><span data-stu-id="25ca6-123">Unsecured Peer Names</span></span>

<span data-ttu-id="25ca6-124">Per un nome non protetto, l'autorità è zero (0) e il classificatore è l'unica parte significativa del nome peer, che crea un nome peer non protetto senza un' [identità](identity-manager-api.md)associata.</span><span class="sxs-lookup"><span data-stu-id="25ca6-124">For an unsecured name, the Authority is zero (0), and the Classifier is the only significant part of the peer name, which creates an unsecured peer name without an associated [identity](identity-manager-api.md).</span></span> <span data-ttu-id="25ca6-125">I nomi di peer non protetti vengono usati nella registrazione e nella risoluzione dei nomi PNRP.</span><span class="sxs-lookup"><span data-stu-id="25ca6-125">Unsecured peer names are used in PNRP name registration and resolution.</span></span> <span data-ttu-id="25ca6-126">I nomi di peer non protetti forniscono un modo utile per registrare e risolvere le risorse che non richiedono la risoluzione dei nomi sicura.</span><span class="sxs-lookup"><span data-stu-id="25ca6-126">Unsecured peer names provide a useful way to register and resolve resources that do not require secure name resolution.</span></span> <span data-ttu-id="25ca6-127">Qualsiasi nodo può tuttavia pubblicare qualsiasi nome non protetto.</span><span class="sxs-lookup"><span data-stu-id="25ca6-127">However, any node can publish any unsecured name.</span></span> <span data-ttu-id="25ca6-128">Le applicazioni interessate dalla sicurezza devono assicurarsi che siano solide e sicure nell'utilizzo di nomi di peer non protetti.</span><span class="sxs-lookup"><span data-stu-id="25ca6-128">Applications concerned with security must ensure that they are robust and secure in their consumption of unsecured peer names.</span></span>

> [!Note]  
> <span data-ttu-id="25ca6-129">Chiunque può registrare un nome peer non protetto con PNRP.</span><span class="sxs-lookup"><span data-stu-id="25ca6-129">Anyone can register an unsecured peer name with PNRP.</span></span>

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a><span data-ttu-id="25ca6-130">PNRP e l'istanza del nome peer più vicina</span><span class="sxs-lookup"><span data-stu-id="25ca6-130">PNRP and the Nearest Peer Name Instance</span></span>

<span data-ttu-id="25ca6-131">Può essere presente più di un'istanza di un nome peer.</span><span class="sxs-lookup"><span data-stu-id="25ca6-131">There can be more than one instance of a peer name.</span></span> <span data-ttu-id="25ca6-132">Quando si usa [PNRP](pnrp-namespace-provider-api.md) per risolvere un nome peer, esiste il concetto di un'istanza del nome peer **più vicina** , il che significa che il nome ha una posizione del servizio più vicina al membro di **sericat** specificato in [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) o [**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="25ca6-132">When using [PNRP](pnrp-namespace-provider-api.md) to resolve a peer name, there is a concept of a **nearest** peer name instance, which means that the name has a service location closest to the **saHint** member specified in [**PNRPINFO\_V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) or [**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span></span> <span data-ttu-id="25ca6-133">Se non viene fornito alcun hint, più vicino a uno degli indirizzi IP locali.</span><span class="sxs-lookup"><span data-stu-id="25ca6-133">If no hint is supplied, closest to one of the local IP addresses.</span></span>

 

 
