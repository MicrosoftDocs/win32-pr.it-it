---
title: DACL null e DACL vuoti (AD DS)
description: La presenza di un elenco di controllo di accesso discrezionale (DACL) null nell'attributo nTSecurityDescriptor di qualsiasi oggetto può creare un grave rischio per la sicurezza.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- Elenchi DACL null e DACL vuoti AD
- Elenchi DACL AD, null e vuoti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956310"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a><span data-ttu-id="455e2-105">DACL null e DACL vuoti (AD DS)</span><span class="sxs-lookup"><span data-stu-id="455e2-105">Null DACLs and Empty DACLs (AD DS)</span></span>

<span data-ttu-id="455e2-106">La presenza di un elenco di controllo di accesso discrezionale (DACL) null nell'attributo [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) di qualsiasi oggetto può creare un grave rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="455e2-106">The presence of a null discretionary access-control list (DACL) in the [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) attribute of any object can create a serious security risk.</span></span> <span data-ttu-id="455e2-107">Un DACL null concede l'accesso completo a tutti gli utenti che lo richiedono; il normale controllo di sicurezza non viene eseguito rispetto all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="455e2-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="455e2-108">Un DACL null non deve essere confuso con un DACL vuoto.</span><span class="sxs-lookup"><span data-stu-id="455e2-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="455e2-109">Un DACL vuoto è un DACL correttamente allocato e inizializzato che non contiene voci di controllo di accesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="455e2-109">An empty DACL is a properly allocated and initialized DACL containing no access-control entries (ACEs).</span></span> <span data-ttu-id="455e2-110">Un DACL vuoto non concede l'accesso all'oggetto a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="455e2-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="455e2-111">Per ulteriori informazioni, vedere [DACL null e DACL vuoti](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="455e2-111">For more information, see [Null DACLs and Empty DACLs](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span></span>

 

 