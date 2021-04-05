---
title: Determinazione delle esigenze di sicurezza
description: La modalità di configurazione della sicurezza COM per l'applicazione dipende dal tipo di sicurezza necessario per l'applicazione. Esistono diverse situazioni comuni che determinano le operazioni da eseguire.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714434"
---
# <a name="determining-your-security-needs"></a><span data-ttu-id="9037c-104">Determinazione delle esigenze di sicurezza</span><span class="sxs-lookup"><span data-stu-id="9037c-104">Determining Your Security Needs</span></span>

<span data-ttu-id="9037c-105">La modalità di configurazione della sicurezza COM per l'applicazione dipende dal tipo di sicurezza necessario per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9037c-105">How you set up COM security for your application depends on what kind of security your application needs.</span></span> <span data-ttu-id="9037c-106">Esistono diverse situazioni comuni che determinano le operazioni da eseguire.</span><span class="sxs-lookup"><span data-stu-id="9037c-106">There are several common situations that determine what you should do.</span></span>

<span data-ttu-id="9037c-107">Se si decide di utilizzare le impostazioni predefinite di sicurezza COM, non è necessario eseguire anythingâ.</span><span class="sxs-lookup"><span data-stu-id="9037c-107">If you decide to use the COM security defaults, you do not have to do anythingâ€”COM handles it all.</span></span> <span data-ttu-id="9037c-108">Per informazioni sulle impostazioni predefinite, vedere [valori predefiniti di sicurezza com](com-security-defaults.md).</span><span class="sxs-lookup"><span data-stu-id="9037c-108">For information on what these default settings are, see [COM Security Defaults](com-security-defaults.md).</span></span>

<span data-ttu-id="9037c-109">È anche possibile impedire qualsiasi chiamata remota nel computer disabilitando completamente DCOM (COM tra computer remoti).</span><span class="sxs-lookup"><span data-stu-id="9037c-109">You can also prevent any remote calls into your machine by disabling DCOM altogether (COM between remote computers).</span></span> <span data-ttu-id="9037c-110">Per ulteriori informazioni, vedere [impostazione di System-Wide sicurezza tramite DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="9037c-110">For more information, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="9037c-111">Per le applicazioni legacy o nuove, è possibile impostare la sicurezza a livello di processo nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9037c-111">For legacy or new applications, you can set process-wide security in the registry.</span></span> <span data-ttu-id="9037c-112">Per ulteriori informazioni, vedere [impostazione della sicurezza Processwide tramite il registro di sistema](setting-processwide-security-through-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="9037c-112">For more information, see [Setting Processwide Security Through the Registry](setting-processwide-security-through-the-registry.md).</span></span>

<span data-ttu-id="9037c-113">È anche possibile eseguire l'override delle impostazioni di sicurezza predefinite per le chiamate a determinate interfacce nel processo, impostando la sicurezza predefinita per la parte restante del processo, in modo da consentire a COM di gestire i casi generali.</span><span class="sxs-lookup"><span data-stu-id="9037c-113">You can also override default security settings for calls to certain interfaces in the process while setting default security for the remainder of the process (to allow COM to handle the general cases).</span></span> <span data-ttu-id="9037c-114">Per ulteriori informazioni, vedere [impostazione della sicurezza a livello di proxy di interfaccia](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="9037c-114">For more information, see [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="9037c-115">Per i requisiti di sicurezza complessi, è possibile gestire tutta la sicurezza a livello di codice anziché consentire a COM di gestirla.</span><span class="sxs-lookup"><span data-stu-id="9037c-115">For complex security requirements, you can handle all security programmatically rather than allowing COM to handle it for you.</span></span> <span data-ttu-id="9037c-116">A tale scopo, chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per disabilitare l'autenticazione automatica e quindi controllare tutte le impostazioni di sicurezza impostando la sicurezza in base al proxy per interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9037c-116">To do this, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to disable automatic authentication, and then control all the security settings by setting security on a per-interface proxy basis.</span></span> <span data-ttu-id="9037c-117">Per altre informazioni, vedere [impostazione della sicurezza Processwide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) e [impostazione della sicurezza a livello di proxy di interfaccia](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="9037c-117">For more information, see [Setting Processwide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) and [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="9037c-118">In alcuni scenari potrebbe essere necessario disattivare completamente la protezione.</span><span class="sxs-lookup"><span data-stu-id="9037c-118">In some scenarios, you might want to turn off security completely.</span></span> <span data-ttu-id="9037c-119">Si potrebbe decidere che l'applicazione non necessita di alcuna sicurezza oppure è possibile disabilitare la sicurezza durante il tempo di sviluppo, in modo da poter abilitare le funzionalità di sicurezza singolarmente.</span><span class="sxs-lookup"><span data-stu-id="9037c-119">You might decide that your application does not need any security, or you might want to disable security during development time so that you can enable security features individually.</span></span> <span data-ttu-id="9037c-120">Per informazioni su come disabilitare la sicurezza COM, [vedere Disattivazione della sicurezza.](turning-off-security.md)</span><span class="sxs-lookup"><span data-stu-id="9037c-120">To learn how to disable COM security, see [Turning Off Security](turning-off-security.md).</span></span>

<span data-ttu-id="9037c-121">La sicurezza in COM si basa sui servizi di autenticazione amministrati dai pacchetti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="9037c-121">Security in COM relies on authentication services administered by security packages.</span></span> <span data-ttu-id="9037c-122">NTLMSSP funziona bene per molte applicazioni, ma non offre una sicurezza più affidabile offerta da altri pacchetti.</span><span class="sxs-lookup"><span data-stu-id="9037c-122">NTLMSSP works well for many applications but does not provide the more robust security offered by other packages.</span></span> <span data-ttu-id="9037c-123">Pertanto, COM supporta il pacchetto di sicurezza Schannel e il protocollo di sicurezza Kerberos V5.</span><span class="sxs-lookup"><span data-stu-id="9037c-123">Therefore, COM supports the Schannel security package and the Kerberos v5 security protocol.</span></span> <span data-ttu-id="9037c-124">Per altri dettagli sull'uso di questi pacchetti di sicurezza, vedere [pacchetti com e di sicurezza](com-and-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="9037c-124">For more details on using these security packages, see [COM and Security Packages](com-and-security-packages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9037c-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9037c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9037c-126">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="9037c-126">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




