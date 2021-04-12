---
title: Disattivazione della sicurezza delle chiamate
description: La sicurezza delle chiamate determina se un client dispone dell'autorizzazione per chiamare i metodi di un server. Esistono due modi per disabilitare la sicurezza delle chiamate, che prevede l'uso di Dcomcnfg.exe per modificare il registro di sistema, mentre l'altro richiede chiamate a CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395530"
---
# <a name="turning-off-call-security"></a><span data-ttu-id="9d551-104">Disattivazione della sicurezza delle chiamate</span><span class="sxs-lookup"><span data-stu-id="9d551-104">Turning Off Call Security</span></span>

<span data-ttu-id="9d551-105">La sicurezza delle chiamate determina se un client dispone dell'autorizzazione per chiamare i metodi di un server.</span><span class="sxs-lookup"><span data-stu-id="9d551-105">Call security determines whether a client has permission to call a server's methods.</span></span> <span data-ttu-id="9d551-106">Esistono due modi per disabilitare la sicurezza delle chiamate: uno prevede l'uso di Dcomcnfg.exe per modificare il registro di sistema, mentre l'altro richiede chiamate a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="9d551-106">There are two ways to disable call security: One involves using Dcomcnfg.exe to modify the registry, and the other requires calls to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

-   [<span data-ttu-id="9d551-107">Disattivazione della sicurezza delle chiamate tramite DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="9d551-107">Turning Off Call Security Using DCOMCNFG</span></span>](#turning-off-call-security-using-dcomcnfg)
-   [<span data-ttu-id="9d551-108">Disattivazione della sicurezza delle chiamate a livello di codice</span><span class="sxs-lookup"><span data-stu-id="9d551-108">Turning Off Call Security Programmatically</span></span>](#turning-off-call-security-programmatically)
-   [<span data-ttu-id="9d551-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d551-109">Related topics</span></span>](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a><span data-ttu-id="9d551-110">Disattivazione della sicurezza delle chiamate tramite DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="9d551-110">Turning Off Call Security Using DCOMCNFG</span></span>

<span data-ttu-id="9d551-111">Per modificare il registro di sistema, è possibile disattivare la sicurezza delle chiamate utilizzando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="9d551-111">Call security can most easily be turned off by using Dcomcnfg.exe to modify the registry.</span></span> <span data-ttu-id="9d551-112">Tuttavia, l'utilizzo di Dcomcnfg.exe per disattivare la sicurezza funziona solo se il client e il server non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="9d551-112">However, using Dcomcnfg.exe to turn security off will work only if both the client and the server do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="9d551-113">Questo perché quando viene chiamato **CoInitializeSecurity** , DCOM ignora le impostazioni del registro di sistema e usa i valori specificati in **CoInitializeSecurity** .</span><span class="sxs-lookup"><span data-stu-id="9d551-113">This is because when **CoInitializeSecurity** is called, DCOM ignores the registry settings and uses the values supplied to **CoInitializeSecurity** instead.</span></span>

<span data-ttu-id="9d551-114">Per disattivare la sicurezza con Dcomcnfg.exe, sia il client che il server devono impostare i livelli di autenticazione su nessuno.</span><span class="sxs-lookup"><span data-stu-id="9d551-114">To turn off security with Dcomcnfg.exe, both the client and the server must set their Authentication Levels to None.</span></span> <span data-ttu-id="9d551-115">È necessario completare i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d551-115">The following steps must be completed:</span></span>

1.  <span data-ttu-id="9d551-116">Eseguire Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="9d551-116">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="9d551-117">Nella pagina **applicazioni** selezionare l'applicazione che rappresenta il server.</span><span class="sxs-lookup"><span data-stu-id="9d551-117">On the **Applications** page, select the application that represents the server.</span></span> <span data-ttu-id="9d551-118">Fare clic sul pulsante delle **Proprietà** (o fare doppio clic sull'applicazione selezionata).</span><span class="sxs-lookup"><span data-stu-id="9d551-118">Click the **Properties** button (or double-click the selected application).</span></span>
3.  <span data-ttu-id="9d551-119">Fare clic sulla scheda **General** (Generale).</span><span class="sxs-lookup"><span data-stu-id="9d551-119">Click the **General** tab.</span></span>
4.  <span data-ttu-id="9d551-120">Nella casella di riepilogo **livello di autenticazione predefinito** selezionare **(nessuno)**.</span><span class="sxs-lookup"><span data-stu-id="9d551-120">From the **Default Authentication Level** list box, select **(None)**.</span></span>
5.  <span data-ttu-id="9d551-121">Per applicare le modifiche, fare clic sul pulsante **applica** . Tuttavia, le modifiche non vengono applicate a tutte le istanze in esecuzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d551-121">Click the **Apply** button to apply changes; however, changes are not applied to any running instances of the application.</span></span>
6.  <span data-ttu-id="9d551-122">Se il client viene visualizzato nell'elenco della pagina *applicazioni* , ripetere i passaggi da 2 a 5, scegliendo il client anziché il server per il passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="9d551-122">If the client appears on the list on the *Applications* page, repeat steps 2 through 5, choosing the client instead of the server for step 2.</span></span> <span data-ttu-id="9d551-123">Fare quindi clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d551-123">Then click the **OK** button.</span></span> <span data-ttu-id="9d551-124">Se il client non è presente nell'elenco, è possibile eseguire una delle tre operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d551-124">If the client is not on the list, you can do one of the following three things:</span></span>
    -   <span data-ttu-id="9d551-125">È possibile impostare il livello di autenticazione del client su None a livello di computer utilizzando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="9d551-125">You can set the client's Authentication Level to None on a computer-wide basis by using Dcomcnfg.exe.</span></span> <span data-ttu-id="9d551-126">Vedere l'avviso e la procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="9d551-126">(See the warning and the procedure below.)</span></span>
    -   <span data-ttu-id="9d551-127">È possibile impostare il livello di autenticazione del client su None a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="9d551-127">You can set the client's authentication level to None programmatically.</span></span>
    -   <span data-ttu-id="9d551-128">È possibile creare una chiave [AppID](appid-key.md) per il client per indicare un livello di autenticazione None.</span><span class="sxs-lookup"><span data-stu-id="9d551-128">You can create an [AppID](appid-key.md) key for the client to indicate an authentication level of None.</span></span> <span data-ttu-id="9d551-129">(Vedere [impostazione della sicurezza Process-Wide tramite il registro di sistema](setting-processwide-security-through-the-registry.md)).</span><span class="sxs-lookup"><span data-stu-id="9d551-129">(See [Setting Process-Wide Security Through the Registry](setting-processwide-security-through-the-registry.md).)</span></span>

<span data-ttu-id="9d551-130">Per impostare il livello di autenticazione su None a livello di computer:</span><span class="sxs-lookup"><span data-stu-id="9d551-130">To set the Authentication Level to None on a computer-wide basis:</span></span>

> [!Note]  
> <span data-ttu-id="9d551-131">L'impostazione del livello di autenticazione a livello di computer su None è estremamente non sicura.</span><span class="sxs-lookup"><span data-stu-id="9d551-131">Setting the computer-wide Authentication Level to None is extremely unsecure.</span></span>

 

1.  <span data-ttu-id="9d551-132">Eseguire Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="9d551-132">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="9d551-133">Scegliere la scheda **proprietà predefinite** .</span><span class="sxs-lookup"><span data-stu-id="9d551-133">Choose the **Default Properties** tab.</span></span>
3.  <span data-ttu-id="9d551-134">Nella casella di riepilogo **livello di autenticazione predefinito** scegliere **(nessuno)**.</span><span class="sxs-lookup"><span data-stu-id="9d551-134">From the **Default Authentication Level** list box, choose **(None)**.</span></span>
4.  <span data-ttu-id="9d551-135">Fare clic sul pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="9d551-135">Click the **OK** button.</span></span>

## <a name="turning-off-call-security-programmatically"></a><span data-ttu-id="9d551-136">Disattivazione della sicurezza delle chiamate a livello di codice</span><span class="sxs-lookup"><span data-stu-id="9d551-136">Turning Off Call Security Programmatically</span></span>

<span data-ttu-id="9d551-137">Per disattivare la protezione delle chiamate a livello di codice, sia il client che il server devono chiamare **CoInitializeSecurity**, impostando il livello di autenticazione nel parametro *dwAuthnLevel* sul \_ \_ livello auth C AuthN \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9d551-137">To turn call security off programmatically, both the client and the server must call **CoInitializeSecurity**, setting the authentication level in the *dwAuthnLevel* parameter to RPC\_C\_AUTHN\_LEVEL\_NONE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d551-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d551-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d551-139">Disattivazione della sicurezza di attivazione</span><span class="sxs-lookup"><span data-stu-id="9d551-139">Turning Off Activation Security</span></span>](turning-off-activation-security.md)
</dt> </dl>

 

 




