---
title: Requisiti di sicurezza delle funzioni di gestione di rete
description: La chiamata di alcune funzioni di gestione della rete non richiede l'appartenenza speciale al gruppo.
ms.assetid: 846a5b81-d5bf-4275-a898-38e6ba308b8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b0987509294f03b8737aae5e721abf5dbdd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517037"
---
# <a name="network-management-function-security-requirements"></a><span data-ttu-id="b9eb8-103">Requisiti di sicurezza delle funzioni di gestione di rete</span><span class="sxs-lookup"><span data-stu-id="b9eb8-103">Network management function security requirements</span></span>

<span data-ttu-id="b9eb8-104">La chiamata di alcune funzioni di gestione della rete non richiede l'appartenenza speciale al gruppo.</span><span class="sxs-lookup"><span data-stu-id="b9eb8-104">Calling some of the network management functions does not require special group membership.</span></span> <span data-ttu-id="b9eb8-105">Per le altre funzioni è necessario che gli utenti dispongano di un livello di privilegio specifico per l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="b9eb8-105">Other functions require that users have a specific privilege level to execute successfully.</span></span> <span data-ttu-id="b9eb8-106">Quando applicabile, la sezione Note nella pagina di riferimento di una funzione indica il livello di privilegio che un utente deve avere per eseguire la funzione specifica.</span><span class="sxs-lookup"><span data-stu-id="b9eb8-106">When applicable, the Remarks section on a function's reference page indicates the privilege level a user must have to execute the particular function.</span></span>

<span data-ttu-id="b9eb8-107">I requisiti di sicurezza che si applicano ai controller di dominio Active Directory possono essere diversi da quelli che si applicano ai server e alle workstation.</span><span class="sxs-lookup"><span data-stu-id="b9eb8-107">Security requirements that apply to Active Directory domain controllers can differ from those that apply to servers and workstations.</span></span>

<span data-ttu-id="b9eb8-108">Per ulteriori informazioni e per un elenco delle funzioni interessate, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9eb8-108">For more information, and a list of affected functions, see the following topics:</span></span>

-   [<span data-ttu-id="b9eb8-109">Requisiti per le funzioni di gestione della rete nei controller di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="b9eb8-109">Requirements for Network Management functions on Active Directory domain controllers</span></span>](requirements-for-network-management-functions-on-active-directory-domain-controllers.md)
-   [<span data-ttu-id="b9eb8-110">Requisiti per le funzioni di gestione della rete su server e workstation</span><span class="sxs-lookup"><span data-stu-id="b9eb8-110">Requirements for Network Management functions on servers and workstations</span></span>](requirements-for-network-management-functions-on-servers-and-workstations.md)

<span data-ttu-id="b9eb8-111">Per ulteriori informazioni sul controllo dell'accesso agli oggetti a protezione diretta, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control), [privilegi](/windows/desktop/SecAuthZ/privileges)e [oggetti a protezione diretta](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="b9eb8-111">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span>

<span data-ttu-id="b9eb8-112">Per ulteriori informazioni sui descrittori di sicurezza specifici utilizzati durante i controlli di accesso, vedere la pagina di riferimento per le singole funzioni.</span><span class="sxs-lookup"><span data-stu-id="b9eb8-112">For more information about specific security descriptors that are used during access checks, see the individual function reference page.</span></span> <span data-ttu-id="b9eb8-113">Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="b9eb8-113">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 