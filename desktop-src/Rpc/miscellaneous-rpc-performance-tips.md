---
title: Suggerimenti sulle prestazioni RPC varie
description: In questa sezione vengono illustrati i suggerimenti sulle prestazioni varie per lo sviluppo di server RPC ad alte prestazioni. In questa sezione vengono forniti numerosi suggerimenti che fanno riferimento al client RPC. Lo sviluppo di un client RPC consente al server RPC di eseguire meno lavoro.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044347"
---
# <a name="miscellaneous-rpc-performance-tips"></a><span data-ttu-id="a08b9-105">Suggerimenti sulle prestazioni RPC varie</span><span class="sxs-lookup"><span data-stu-id="a08b9-105">Miscellaneous RPC Performance Tips</span></span>

<span data-ttu-id="a08b9-106">In questa sezione vengono illustrati i suggerimenti sulle prestazioni varie per lo sviluppo di server RPC ad alte prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a08b9-106">This section discusses miscellaneous performance tips for developing high performance RPC servers.</span></span> <span data-ttu-id="a08b9-107">In questa sezione vengono forniti numerosi suggerimenti che fanno riferimento al client RPC.</span><span class="sxs-lookup"><span data-stu-id="a08b9-107">This section provides many tips that refer to the RPC client.</span></span> <span data-ttu-id="a08b9-108">Lo sviluppo di un client RPC consente al server RPC di eseguire meno lavoro.</span><span class="sxs-lookup"><span data-stu-id="a08b9-108">Developing an RPC client properly enables the RPC server to perform less work.</span></span>

## <a name="use-kerberos"></a><span data-ttu-id="a08b9-109">Usa Kerberos</span><span class="sxs-lookup"><span data-stu-id="a08b9-109">Use Kerberos</span></span>

<span data-ttu-id="a08b9-110">Se si utilizza la sicurezza, utilizzare Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a08b9-110">If security is used, use Kerberos.</span></span> <span data-ttu-id="a08b9-111">Sul lato server, Kerberos non richiede l'accesso al KDC.</span><span class="sxs-lookup"><span data-stu-id="a08b9-111">On the server side, Kerberos does not require access to the KDC.</span></span> <span data-ttu-id="a08b9-112">In questo modo, il carico di lavoro viene spostato dal server al client, che fornisce server con prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="a08b9-112">This moves the workload from the server to the client, which provides better performing servers.</span></span>

## <a name="use-static-identity-tracking"></a><span data-ttu-id="a08b9-113">USA rilevamento identità statico</span><span class="sxs-lookup"><span data-stu-id="a08b9-113">Use Static Identity Tracking</span></span>

<span data-ttu-id="a08b9-114">Se si usa la sicurezza, provare a usare il rilevamento statico delle identità.</span><span class="sxs-lookup"><span data-stu-id="a08b9-114">If security is used, try to use static identity tracking.</span></span> <span data-ttu-id="a08b9-115">Il rilevamento statico delle identità è più economico in termini di utilizzo delle risorse rispetto al rilevamento dinamico delle identità.</span><span class="sxs-lookup"><span data-stu-id="a08b9-115">Static identity tracking is cheaper in terms of resource usage than dynamic identity tracking.</span></span> <span data-ttu-id="a08b9-116">Se l'identità del client viene modificata e il server non è in grado di riconoscere la modifica, utilizzare il rilevamento dinamico anziché creare un handle di associazione diverso per ogni identità.</span><span class="sxs-lookup"><span data-stu-id="a08b9-116">If the client identity changes, and the server should not be aware of the change, use dynamic tracking instead of creating a different binding handle for each identity.</span></span> <span data-ttu-id="a08b9-117">Tuttavia, se l'identità è la stessa, assicurarsi che RPC sia a conoscenza di tale fatto, in modo da evitare che RPC effettui verifiche per l'identità modificata ogni volta.</span><span class="sxs-lookup"><span data-stu-id="a08b9-117">But if the identity is the same, ensure RPC is aware of that fact to avoid having RPC make checks for changed identity every time.</span></span>

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a><span data-ttu-id="a08b9-118">Usare la funzione RpcGetAuthorizationContextForClient</span><span class="sxs-lookup"><span data-stu-id="a08b9-118">Use the RpcGetAuthorizationContextForClient Function</span></span>

<span data-ttu-id="a08b9-119">Se è necessario controllare l'accesso in Windows XP, usare la funzione [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) .</span><span class="sxs-lookup"><span data-stu-id="a08b9-119">If you need to check access in Windows XP, use the [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) function.</span></span> <span data-ttu-id="a08b9-120">I contesti Authz risultanti consentono controlli di accesso molto veloci, che vengono memorizzati nella cache in modo efficiente in base al tempo di esecuzione RPC.</span><span class="sxs-lookup"><span data-stu-id="a08b9-120">The resulting Authz contexts enables very fast access checks, which are efficiently cached by the RPC run time.</span></span>

## <a name="do-not-modify-the-token-unless-necessary"></a><span data-ttu-id="a08b9-121">Non modificare il token a meno che non sia necessario</span><span class="sxs-lookup"><span data-stu-id="a08b9-121">Do Not Modify the Token Unless Necessary</span></span>

<span data-ttu-id="a08b9-122">Se viene utilizzato il rilevamento dinamico delle identità, non modificare il token del thread o del processo, a meno che non sia assolutamente necessario.</span><span class="sxs-lookup"><span data-stu-id="a08b9-122">If dynamic identity tracking is used, do not modify the thread/process token unless absolutely necessary.</span></span> <span data-ttu-id="a08b9-123">Anche se è stato modificato in impostazioni precedenti, il token è spesso abbastanza diverso dal sistema di sicurezza per attivare la creazione di un nuovo contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a08b9-123">Even if it is modified to settings it previously had, the token often is sufficiently different to the security system to trigger the establishment of a new security context.</span></span>

## <a name="consider-mixed-mode-serialization-for-context-handles"></a><span data-ttu-id="a08b9-124">Considerare la serializzazione in modalità mista per gli handle</span><span class="sxs-lookup"><span data-stu-id="a08b9-124">Consider Mixed Mode Serialization for Context Handles</span></span>

<span data-ttu-id="a08b9-125">La modalità di serializzazione predefinita per l'handle di contesto viene serializzata (esclusiva).</span><span class="sxs-lookup"><span data-stu-id="a08b9-125">The default serialization mode for context handle is serialized (exclusive).</span></span> <span data-ttu-id="a08b9-126">Si consiglia di effettuare tutte le chiamate che non modificano lo stato dell'handle di contesto in modalità di serializzazione condivisa.</span><span class="sxs-lookup"><span data-stu-id="a08b9-126">Consider making all calls that do not modify the state of the context handle in shared serialization mode.</span></span> <span data-ttu-id="a08b9-127">Per ulteriori informazioni, vedere [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) .</span><span class="sxs-lookup"><span data-stu-id="a08b9-127">See [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) for more information.</span></span>

 

 




