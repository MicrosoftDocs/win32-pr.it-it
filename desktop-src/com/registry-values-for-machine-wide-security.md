---
title: Valori del registro di sistema per System-Wide sicurezza
description: Valori del registro di sistema per System-Wide sicurezza
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955331"
---
# <a name="registry-values-for-system-wide-security"></a><span data-ttu-id="d2f2f-103">Valori del registro di sistema per System-Wide sicurezza</span><span class="sxs-lookup"><span data-stu-id="d2f2f-103">Registry Values for System-Wide Security</span></span>

<span data-ttu-id="d2f2f-104">Non è consigliabile modificare le impostazioni di sicurezza a livello di sistema, in quanto questa operazione influirà su tutte le applicazioni server COM che non impostano una sicurezza a livello di processo e potrebbe impedire il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="d2f2f-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="d2f2f-105">Se si modificano le impostazioni di sicurezza a livello di sistema in modo da influire sulle impostazioni di sicurezza per una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM.</span><span class="sxs-lookup"><span data-stu-id="d2f2f-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="d2f2f-106">Per ulteriori informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione Process-Wide sicurezza](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="d2f2f-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="d2f2f-107">Determinati valori del registro di sistema vengono utilizzati per determinare le impostazioni di sicurezza per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="d2f2f-107">Certain values in the registry are used to determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="d2f2f-108">È possibile utilizzare Dcomcnfg.exe per modificare queste impostazioni di sicurezza predefinite per un computer.</span><span class="sxs-lookup"><span data-stu-id="d2f2f-108">You can use Dcomcnfg.exe to modify these default security settings for a computer.</span></span> <span data-ttu-id="d2f2f-109">Per le procedure dettagliate che descrivono come usare Dcomcnfg.exe a questo scopo, vedere [impostazione della sicurezza System-Wide tramite DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="d2f2f-109">For step-by-step procedures that describe how to use Dcomcnfg.exe for this purpose, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="d2f2f-110">Un altro modo per modificare le impostazioni predefinite a livello di sistema consiste nel modificare direttamente i valori del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d2f2f-110">Another way to change default system-wide settings is to manipulate registry values directly.</span></span> <span data-ttu-id="d2f2f-111">Tuttavia, solo gli amministratori e il sistema hanno accesso completo alla parte del registro di sistema che contiene le impostazioni predefinite per la protezione delle chiamate a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="d2f2f-111">However, only administrators and the system have full access to the portion of the registry that contains the default system-wide call-security settings.</span></span> <span data-ttu-id="d2f2f-112">Tutti gli altri utenti hanno solo l'accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="d2f2f-112">All other users have read-access only.</span></span>

<span data-ttu-id="d2f2f-113">I valori denominati che influiscono sulle impostazioni predefinite di sicurezza a livello di sistema sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2f2f-113">The named values that affect system-wide security defaults are as follows:</span></span>

-   [<span data-ttu-id="d2f2f-114">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="d2f2f-114">DefaultLaunchPermission</span></span>](defaultlaunchpermission.md)
-   [<span data-ttu-id="d2f2f-115">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="d2f2f-115">DefaultAccessPermission</span></span>](defaultaccesspermission.md)
-   [<span data-ttu-id="d2f2f-116">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="d2f2f-116">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
-   [<span data-ttu-id="d2f2f-117">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="d2f2f-117">LegacyImpersonationLevel</span></span>](legacyimpersonationlevel.md)
-   [<span data-ttu-id="d2f2f-118">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="d2f2f-118">LegacySecureReferences</span></span>](legacysecurereferences.md)
-   [<span data-ttu-id="d2f2f-119">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="d2f2f-119">SRPRunningObjectChecks</span></span>](srprunningobjectchecks.md)
-   [<span data-ttu-id="d2f2f-120">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="d2f2f-120">SRPActivateAsActivatorChecks</span></span>](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a><span data-ttu-id="d2f2f-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2f2f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2f2f-122">Impostazione della sicurezza Process-Wide</span><span class="sxs-lookup"><span data-stu-id="d2f2f-122">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




