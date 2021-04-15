---
title: Sicurezza attivazione
description: Sicurezza attivazione
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474406"
---
# <a name="activation-security"></a><span data-ttu-id="da0b1-103">Sicurezza attivazione</span><span class="sxs-lookup"><span data-stu-id="da0b1-103">Activation Security</span></span>

<span data-ttu-id="da0b1-104">La sicurezza per l'attivazione (detta anche sicurezza di avvio) consente di controllare gli utenti che possono avviare un server.</span><span class="sxs-lookup"><span data-stu-id="da0b1-104">Activation security (also called launch security) helps control who can launch a server.</span></span> <span data-ttu-id="da0b1-105">La sicurezza per l'attivazione viene applicata automaticamente da Gestione controllo servizi (SCM) di un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="da0b1-105">Activation security is automatically applied by the service control manager (SCM) of a particular computer.</span></span> <span data-ttu-id="da0b1-106">Al momento della ricezione di una richiesta da parte di un client per l'attivazione di un oggetto (come descritto in [funzioni helper](instance-creation-helper-functions.md)per la creazione di istanze), SCM controlla la richiesta rispetto alle informazioni di sicurezza di attivazione archiviate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="da0b1-106">Upon receipt of a request from a client to activate an object (as described in [Instance Creation Helper Functions](instance-creation-helper-functions.md)), the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="da0b1-107">La sicurezza dell'attivazione viene verificata anche per le attivazioni dello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="da0b1-107">(Activation security is also checked for same-computer activations.)</span></span>

<span data-ttu-id="da0b1-108">Quando si determina l'identità del client, l'attivazione esamina il flag di mascheramento impostato nella chiamata del client a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="da0b1-108">When determining the identity of the client, activation examines the cloaking flag set in the client's call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="da0b1-109">Se viene impostato il flag di mascheramento (per mascheramento statico o dinamico), viene utilizzato il token del thread, se presente, per determinare l'identità del client.</span><span class="sxs-lookup"><span data-stu-id="da0b1-109">If the cloaking flag is set (for either dynamic or static cloaking), the thread token is used, if present, to determine the identity of the client.</span></span> <span data-ttu-id="da0b1-110">Se non è impostato alcun mascheramento, viene utilizzato il token di processo anziché il token del thread.</span><span class="sxs-lookup"><span data-stu-id="da0b1-110">If no cloaking is set, the process token is used instead of the thread token.</span></span>

<span data-ttu-id="da0b1-111">Per ulteriori informazioni sulla sicurezza dell'attivazione, vedere [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) e [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span><span class="sxs-lookup"><span data-stu-id="da0b1-111">For more information about activation security, see [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) and [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="da0b1-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da0b1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da0b1-113">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="da0b1-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 