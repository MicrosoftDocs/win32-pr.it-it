---
description: Un DACL null concede l'accesso completo a tutti gli utenti che lo richiedono. Un DACL vuoto è un DACL correttamente allocato e inizializzato che non contiene voci di controllo di accesso. Un DACL vuoto non concede l'accesso all'oggetto a cui è assegnato.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACL null e DACL vuoti (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317038"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a><span data-ttu-id="36836-105">DACL null e DACL vuoti (autorizzazione)</span><span class="sxs-lookup"><span data-stu-id="36836-105">Null DACLs and Empty DACLs (Authorization)</span></span>

<span data-ttu-id="36836-106">Se l' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) che appartiene al [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) di un oggetto è impostato su **null**, viene creato un DACL null.</span><span class="sxs-lookup"><span data-stu-id="36836-106">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that belongs to an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly) is set to **NULL**, a null DACL is created.</span></span> <span data-ttu-id="36836-107">Un DACL null concede l'accesso completo a tutti gli utenti che lo richiedono; il normale controllo di sicurezza non viene eseguito rispetto all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36836-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="36836-108">Un DACL null non deve essere confuso con un DACL vuoto.</span><span class="sxs-lookup"><span data-stu-id="36836-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="36836-109">Un DACL vuoto è un DACL correttamente allocato e inizializzato che non contiene [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE).</span><span class="sxs-lookup"><span data-stu-id="36836-109">An empty DACL is a properly allocated and initialized DACL that contains no [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs).</span></span> <span data-ttu-id="36836-110">Un DACL vuoto non concede l'accesso all'oggetto a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="36836-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="36836-111">Per un esempio di come creare un DACL, vedere [creazione di un DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="36836-111">For an example of how to create a DACL, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

 
