---
description: Gestione autorizzazioni fornisce un'infrastruttura flessibile per l'integrazione del controllo di accesso basato sui ruoli nelle applicazioni. Consente agli amministratori che utilizzano tali applicazioni di fornire l'accesso tramite l'assegnazione di ruoli utente associati a qualifiche professionali.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modello di gestione autorizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350611"
---
# <a name="authorization-manager-model"></a><span data-ttu-id="ecc28-104">Modello di gestione autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="ecc28-104">Authorization Manager Model</span></span>

<span data-ttu-id="ecc28-105">Gestione autorizzazioni fornisce un'infrastruttura flessibile per l'integrazione del controllo di accesso basato sui ruoli nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ecc28-105">Authorization Manager provides a flexible framework for integrating role-based access control into applications.</span></span> <span data-ttu-id="ecc28-106">Consente agli amministratori che utilizzano tali applicazioni di fornire l'accesso tramite l'assegnazione di ruoli utente associati a qualifiche professionali.</span><span class="sxs-lookup"><span data-stu-id="ecc28-106">It enables administrators who use those applications to provide access through assigned user roles that relate to job functions.</span></span>

<span data-ttu-id="ecc28-107">Le applicazioni di Gestione autorizzazioni consentono di archiviare criteri di autorizzazione in formato di archivi autorizzazioni che vengono archiviati in file XML o Active Directory e consentono di applicare criteri di autorizzazione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ecc28-107">Authorization Manager applications store authorization policy in the form of authorization stores that are stored in Active Directory or XML files and apply authorization policy at run time.</span></span>

<span data-ttu-id="ecc28-108">Le applicazioni chiamano quindi un metodo di verifica dell'accesso in fase di esecuzione che controlla l'accesso alle informazioni sui criteri nell'archivio autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="ecc28-108">Applications then call a run-time access check method that checks access against the policy information in the authorization store.</span></span>

<span data-ttu-id="ecc28-109">Il criterio di autorizzazione include le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecc28-109">Authorization policy includes the following parts:</span></span>

-   [<span data-ttu-id="ecc28-110">Archivi, applicazioni e ambiti dei criteri</span><span class="sxs-lookup"><span data-stu-id="ecc28-110">Policy Stores, Applications, and Scopes</span></span>](policy-stores--applications--and-scopes.md)
-   [<span data-ttu-id="ecc28-111">Utenti e gruppi</span><span class="sxs-lookup"><span data-stu-id="ecc28-111">Users and Groups</span></span>](users-and-groups.md)
-   [<span data-ttu-id="ecc28-112">Operazioni e attività</span><span class="sxs-lookup"><span data-stu-id="ecc28-112">Operations and Tasks</span></span>](operations-and-tasks.md)
-   [<span data-ttu-id="ecc28-113">Ruoli</span><span class="sxs-lookup"><span data-stu-id="ecc28-113">Roles</span></span>](roles.md)
-   [<span data-ttu-id="ecc28-114">Regole di business</span><span class="sxs-lookup"><span data-stu-id="ecc28-114">Business Rules</span></span>](business-rules.md)
-   [<span data-ttu-id="ecc28-115">raccolte</span><span class="sxs-lookup"><span data-stu-id="ecc28-115">Collections</span></span>](collections.md)

 

 



