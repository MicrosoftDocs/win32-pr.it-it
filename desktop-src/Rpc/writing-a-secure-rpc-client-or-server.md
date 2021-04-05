---
title: Scrittura di un client o un server RPC sicuro
description: In questa sezione vengono fornite le procedure consigliate per la scrittura di un client o un server RPC protetto.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- RPC (Remote Procedure Call), procedure consigliate, scrittura di un client o un server protetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047107"
---
# <a name="writing-a-secure-rpc-client-or-server"></a><span data-ttu-id="29354-104">Scrittura di un client o un server RPC sicuro</span><span class="sxs-lookup"><span data-stu-id="29354-104">Writing a Secure RPC Client or Server</span></span>

<span data-ttu-id="29354-105">In questa sezione vengono fornite le procedure consigliate per la scrittura di un client o un server RPC protetto.</span><span class="sxs-lookup"><span data-stu-id="29354-105">This section provides best practice recommendations for writing a secure RPC client or server.</span></span>

<span data-ttu-id="29354-106">Le informazioni contenute in questa sezione si applicano a Windows 2000 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29354-106">The information in this section applies to Windows 2000 and Windows XP.</span></span> <span data-ttu-id="29354-107">Questa sezione si applica a tutte le sequenze di protocollo, incluso [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="29354-107">This section applies to all protocol sequences, including [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="29354-108">Gli sviluppatori tendono a pensare che **ncalrpc** non sia una destinazione probabile per un attacco, che non è vero in un server terminal in cui potenzialmente centinaia di utenti hanno accesso a un servizio, e compromettere o persino arrestare un servizio può comportare l'acquisizione di un accesso aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="29354-108">Developers tend to think **ncalrpc** is not a probable target for an attack, which is not true on a terminal server where potentially hundreds of users have access to a service, and compromising or even bringing down a service can lead to acquiring extra access.</span></span>

<span data-ttu-id="29354-109">Questa sezione è divisa negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="29354-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="29354-110">Provider di sicurezza da usare</span><span class="sxs-lookup"><span data-stu-id="29354-110">Which Security Provider To Use</span></span>](which-security-provider-to-use.md)
-   [<span data-ttu-id="29354-111">Controllo dell'autenticazione client</span><span class="sxs-lookup"><span data-stu-id="29354-111">Controlling Client Authentication</span></span>](controlling-client-authentication.md)
-   [<span data-ttu-id="29354-112">Scelta di un livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="29354-112">Choosing an Authentication Level</span></span>](choosing-an-authentication-level.md)
-   [<span data-ttu-id="29354-113">Scelta delle opzioni QOS di sicurezza</span><span class="sxs-lookup"><span data-stu-id="29354-113">Choosing Security QOS Options</span></span>](choosing-security-qos-options.md)
-   [<span data-ttu-id="29354-114">Errore comune: supponendo che RpcServerRegisterAuthInfo impedisca a utenti non autorizzati di chiamare il server</span><span class="sxs-lookup"><span data-stu-id="29354-114">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [<span data-ttu-id="29354-115">Callback</span><span class="sxs-lookup"><span data-stu-id="29354-115">Callbacks</span></span>](callbacks.md)
-   [<span data-ttu-id="29354-116">Sessioni null</span><span class="sxs-lookup"><span data-stu-id="29354-116">Null Sessions</span></span>](null-sessions.md)
-   [<span data-ttu-id="29354-117">Usare il flag/robust</span><span class="sxs-lookup"><span data-stu-id="29354-117">Use the /robust Flag</span></span>](use-the-robust-flag.md)
-   [<span data-ttu-id="29354-118">Tecniche IDL per una migliore progettazione di interfacce e metodi</span><span class="sxs-lookup"><span data-stu-id="29354-118">IDL Techniques for Better Interface and Method Design</span></span>](idl-techniques-for-better-interface-and-method-design.md)
-   [<span data-ttu-id="29354-119">Handle di contesto Strict e di tipo strict</span><span class="sxs-lookup"><span data-stu-id="29354-119">Strict and Type Strict Context Handles</span></span>](strict-and-type-strict-context-handles.md)
-   [<span data-ttu-id="29354-120">Non considerare attendibile il peer</span><span class="sxs-lookup"><span data-stu-id="29354-120">Do Not Trust Your Peer</span></span>](do-not-trust-your-peer.md)
-   [<span data-ttu-id="29354-121">Non utilizzare la sicurezza degli endpoint</span><span class="sxs-lookup"><span data-stu-id="29354-121">Do Not Use Endpoint Security</span></span>](do-not-use-endpoint-security.md)
-   [<span data-ttu-id="29354-122">Prestare attenzione ad altri endpoint RPC in esecuzione nello stesso processo</span><span class="sxs-lookup"><span data-stu-id="29354-122">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [<span data-ttu-id="29354-123">Verificare che il server sia quello che dichiara di essere</span><span class="sxs-lookup"><span data-stu-id="29354-123">Verify The Server Is Who It Claims To Be</span></span>](verify-the-server-is-who-it-claims-to-be.md)
-   [<span data-ttu-id="29354-124">Usare le sequenze di protocollo mainstream</span><span class="sxs-lookup"><span data-stu-id="29354-124">Use Mainstream Protocol Sequences</span></span>](use-mainstream-protocol-sequences.md)
-   [<span data-ttu-id="29354-125">Quanto è sicuro il server RPC?</span><span class="sxs-lookup"><span data-stu-id="29354-125">How Secure is my RPC Server Now?</span></span>](how-secure-is-my-rpc-server-now.md)

 

 