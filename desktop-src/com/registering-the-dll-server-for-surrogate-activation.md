---
title: Registrazione del server DLL per l'attivazione surrogata
description: Registrazione del server DLL per l'attivazione surrogata
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730466"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a><span data-ttu-id="4878d-103">Registrazione del server DLL per l'attivazione surrogata</span><span class="sxs-lookup"><span data-stu-id="4878d-103">Registering the DLL Server for Surrogate Activation</span></span>

<span data-ttu-id="4878d-104">Un server DLL verrà caricato in un processo surrogato nelle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4878d-104">A DLL server will be loaded into a surrogate process under the following conditions:</span></span>

-   <span data-ttu-id="4878d-105">È necessario specificare un valore AppID nella chiave CLSID nel registro di sistema e una chiave [AppID](appid-key.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="4878d-105">There must be an AppID value specified under the CLSID key in the registry, and a corresponding [AppID](appid-key.md) key.</span></span>
-   <span data-ttu-id="4878d-106">In una chiamata di attivazione, viene impostato il bit del [**\_ \_ server locale CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) e la chiave CLSID non specifica [LocalServer32](localserver32.md), [LocalServer](localserver.md)o [LocalService](localservice.md).</span><span class="sxs-lookup"><span data-stu-id="4878d-106">In an activation call, the [**CLSCTX\_LOCAL\_SERVER**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) bit is set and the CLSID key does not specify [LocalServer32](localserver32.md), [LocalServer](localserver.md), or [LocalService](localservice.md).</span></span> <span data-ttu-id="4878d-107">Se sono impostati altri bit **CLSCTX** , viene seguito l' [**algoritmo di elaborazione**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)per i flag di esecuzione in-process, locali o remoti.</span><span class="sxs-lookup"><span data-stu-id="4878d-107">If other **CLSCTX** bits are set, the [**processing algorithm**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)for the in-process, local, or remote execution flags is followed.</span></span>
-   <span data-ttu-id="4878d-108">La chiave CLSID contiene la sottochiave [InprocServer32](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="4878d-108">The CLSID key contains the [InprocServer32](inprocserver32.md) subkey.</span></span>
-   <span data-ttu-id="4878d-109">La DLL proxy/stub specificata nella chiave **InprocServer32** esiste.</span><span class="sxs-lookup"><span data-stu-id="4878d-109">The proxy/stub DLL specified in the **InprocServer32** key exists.</span></span>
-   <span data-ttu-id="4878d-110">Il valore [DllSurrogate](dllsurrogate.md) esiste sotto la chiave **AppID** .</span><span class="sxs-lookup"><span data-stu-id="4878d-110">The [DllSurrogate](dllsurrogate.md) value exists under the **AppID** key.</span></span>

<span data-ttu-id="4878d-111">Se è presente un **LocalServer**, **LocalServer32** o **LocalService**, che indica l'esistenza di un file exe, il server o il servizio exe viene sempre avviato in preferenza al caricamento di un server DLL in un processo surrogato.</span><span class="sxs-lookup"><span data-stu-id="4878d-111">If there is a **LocalServer**, **LocalServer32**, or **LocalService**, indicating the existence of an EXE, the EXE server or service will always be launched in preference to loading a DLL server into a surrogate process.</span></span>

<span data-ttu-id="4878d-112">È necessario specificare il valore denominato **DllSurrogate** per l'attivazione surrogata.</span><span class="sxs-lookup"><span data-stu-id="4878d-112">The **DllSurrogate** named-value must be specified for surrogate activation to occur.</span></span> <span data-ttu-id="4878d-113">L'attivazione si riferisce alle chiamate a una delle funzioni di attivazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="4878d-113">Activation refers to calls to any of the following activation functions:</span></span>

-   [<span data-ttu-id="4878d-114">**CoGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="4878d-114">**CoGetClassObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [<span data-ttu-id="4878d-115">**CoCreateInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="4878d-115">**CoCreateInstanceEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [<span data-ttu-id="4878d-116">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="4878d-116">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [<span data-ttu-id="4878d-117">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="4878d-117">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [<span data-ttu-id="4878d-118">**IMoniker:: BindToObject**</span><span class="sxs-lookup"><span data-stu-id="4878d-118">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

<span data-ttu-id="4878d-119">Per avviare un'istanza del surrogato fornito dal sistema, impostare il valore di **DllSurrogate** su una stringa vuota o su **null**.</span><span class="sxs-lookup"><span data-stu-id="4878d-119">To launch an instance of the system-supplied surrogate, set the value of **DllSurrogate** either to an empty string or to **NULL**.</span></span> <span data-ttu-id="4878d-120">Per specificare l'avvio di un surrogato personalizzato, impostare il valore sul percorso del surrogato.</span><span class="sxs-lookup"><span data-stu-id="4878d-120">To specify the launch of a custom surrogate, set the value to the path of the surrogate.</span></span>

<span data-ttu-id="4878d-121">Se vengono specificati sia [RemoteServerName](remoteservername.md) che **DllSurrogate** per lo stesso AppID, il valore **RemoteServerName** viene ignorato e il valore **DllSurrogate** causa un'attivazione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="4878d-121">If both [RemoteServerName](remoteservername.md) and **DllSurrogate** are specified for the same AppID, the **RemoteServerName** value is ignored and the **DllSurrogate** value causes an activation on the local computer.</span></span> <span data-ttu-id="4878d-122">Per l'attivazione surrogata remota, specificare **RemoteServerName** ma non **DllSurrogate** nel client e specificare **DllSurrogate** nel server.</span><span class="sxs-lookup"><span data-stu-id="4878d-122">For remote surrogate activation, specify **RemoteServerName** but not **DllSurrogate** on the client, and specify **DllSurrogate** on the server.</span></span>

<span data-ttu-id="4878d-123">Un server DLL progettato per essere sempre eseguito da solo nel proprio processo surrogato è migliore per la configurazione con un AppID uguale al relativo CLSID.</span><span class="sxs-lookup"><span data-stu-id="4878d-123">A DLL server that is designed to always run alone in its own surrogate process is best configured with an AppID equal its CLSID.</span></span> <span data-ttu-id="4878d-124">In **AppID** è sufficiente specificare un valore denominato **DllSurrogate** con un valore di stringa vuoto.</span><span class="sxs-lookup"><span data-stu-id="4878d-124">Under **AppID**, simply specify a **DllSurrogate** named-value with an empty string value.</span></span>

<span data-ttu-id="4878d-125">È consigliabile configurare un server DLL progettato per essere eseguito da solo nel proprio processo surrogato e per servire più client in una rete con un valore [RunAs](runas.md) specificato nella chiave del registro di sistema **AppID** .</span><span class="sxs-lookup"><span data-stu-id="4878d-125">It is best to configure a DLL server that is designed to run alone in its own surrogate process and to service multiple clients across a network with a [RunAs](runas.md) value specified under the **AppID** registry key.</span></span> <span data-ttu-id="4878d-126">Se **RunAs** specifica "utente interattivo" o un'identità utente specifica dipende dall'interfaccia utente, dalla sicurezza e da altri requisiti del server.</span><span class="sxs-lookup"><span data-stu-id="4878d-126">Whether the **RunAs** specifies "Interactive User" or a specific user identity depends upon the user interface, security, and other server requirements.</span></span> <span data-ttu-id="4878d-127">Quando si specifica un valore **RunAs** , viene caricata solo un'istanza del server per il servizio di tutti i client, indipendentemente dall'identità del client.</span><span class="sxs-lookup"><span data-stu-id="4878d-127">When a **RunAs** value is specified, only one instance of the server is loaded to service all of the clients, regardless of the identity of the client.</span></span> <span data-ttu-id="4878d-128">D'altra parte, non configurare il server con **RunAs** se si intende disporre di un'istanza del server DLL in esecuzione in surrogato per servire ogni identità client remota.</span><span class="sxs-lookup"><span data-stu-id="4878d-128">On the other hand, do not configure the server with **RunAs** if the intention is to have one instance of the DLL server running in surrogate to service each remote client identity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4878d-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4878d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4878d-130">Requisiti del server DLL</span><span class="sxs-lookup"><span data-stu-id="4878d-130">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="4878d-131">Condivisione surrogati</span><span class="sxs-lookup"><span data-stu-id="4878d-131">Surrogate Sharing</span></span>](surrogate-sharing.md)
</dt> </dl>

 

 