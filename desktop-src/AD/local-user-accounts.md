---
title: Uso di un account utente locale come account di accesso al servizio
description: Un account utente locale (formato nome \ 0034;. \\ UserName \ 0034;) esiste solo nel database SAM del computer host; non dispone di un oggetto utente in Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84da502e99d2e5cd74e98e9f792e06f74f4852e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116709"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a><span data-ttu-id="6e230-103">Uso di un account utente locale come account di accesso al servizio</span><span class="sxs-lookup"><span data-stu-id="6e230-103">Using a Local User Account as a Service Logon Account</span></span>

<span data-ttu-id="6e230-104">Un account utente locale (formato nome: ". \\ *Nome utente*") esistente solo nel database SAM del computer host; non dispone di un oggetto utente in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6e230-104">A local user account (name format: ".\\*UserName*") exists only in the SAM database of the host computer; it does not have a user object in Active Directory Domain Services.</span></span> <span data-ttu-id="6e230-105">Ciò significa che un account locale non può essere autenticato dal dominio.</span><span class="sxs-lookup"><span data-stu-id="6e230-105">This means that a local account cannot be authenticated by the domain.</span></span> <span data-ttu-id="6e230-106">Di conseguenza, un servizio che viene eseguito nel contesto di sicurezza di un account utente locale non ha accesso alle risorse di rete (ad eccezione di un utente anonimo) e non può supportare l'autenticazione reciproca Kerberos in cui il servizio viene autenticato dai relativi client.</span><span class="sxs-lookup"><span data-stu-id="6e230-106">Consequently, a service that runs in the security context of a local user account does not have access to network resources (except as an anonymous user), and it cannot support Kerberos mutual authentication in which the service is authenticated by its clients.</span></span> <span data-ttu-id="6e230-107">Per questi motivi, gli account utente locali non sono in genere appropriati per i servizi abilitati all'uso di directory.</span><span class="sxs-lookup"><span data-stu-id="6e230-107">For these reasons, local user accounts are typically inappropriate for directory-enabled services.</span></span> <span data-ttu-id="6e230-108">Sul lato più, i bug nel servizio non possono danneggiare il sistema.</span><span class="sxs-lookup"><span data-stu-id="6e230-108">On the plus side, bugs in the service cannot damage the system.</span></span> <span data-ttu-id="6e230-109">Se il servizio può essere eseguito in base a tali limitazioni, dovrebbe.</span><span class="sxs-lookup"><span data-stu-id="6e230-109">If your service can run under those limitations, it should.</span></span>

 

 




