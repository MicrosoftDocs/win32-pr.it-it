---
description: Viene illustrato come modificare i privilegi in un token usando le funzioni AdjustTokenPrivileges e CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Modifica dei privilegi in un token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317741"
---
# <a name="changing-privileges-in-a-token"></a><span data-ttu-id="f2335-103">Modifica dei privilegi in un token</span><span class="sxs-lookup"><span data-stu-id="f2335-103">Changing Privileges in a Token</span></span>

<span data-ttu-id="f2335-104">È possibile modificare i privilegi in un token primario o di rappresentazione in due modi:</span><span class="sxs-lookup"><span data-stu-id="f2335-104">You can change the privileges in either a primary or an impersonation token in two ways:</span></span>

-   <span data-ttu-id="f2335-105">Abilitare o disabilitare i privilegi tramite la funzione [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="f2335-105">Enable or disable privileges by using the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>
-   <span data-ttu-id="f2335-106">Limitare o rimuovere i privilegi tramite la funzione [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .</span><span class="sxs-lookup"><span data-stu-id="f2335-106">Restrict or remove privileges by using the [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) function.</span></span>

<span data-ttu-id="f2335-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) non è in grado di aggiungere o rimuovere privilegi dal token.</span><span class="sxs-lookup"><span data-stu-id="f2335-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) cannot add or remove privileges from the token.</span></span> <span data-ttu-id="f2335-108">Può abilitare solo i privilegi esistenti attualmente disabilitati o disabilitare i privilegi esistenti attualmente abilitati.</span><span class="sxs-lookup"><span data-stu-id="f2335-108">It can only enable existing privileges that are currently disabled or disable existing privileges that are currently enabled.</span></span> <span data-ttu-id="f2335-109">Per esempi, vedere [Abilitazione e disabilitazione dei privilegi in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="f2335-109">For examples, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

<span data-ttu-id="f2335-110">Per assegnare privilegi a un account utente, vedere [assegnazione di privilegi a un account](assigning-privileges-to-an-account.md).</span><span class="sxs-lookup"><span data-stu-id="f2335-110">To assign privileges to a user account, see [Assigning Privileges to an Account](assigning-privileges-to-an-account.md).</span></span>

<span data-ttu-id="f2335-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) offre funzionalità più estese come segue:</span><span class="sxs-lookup"><span data-stu-id="f2335-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) has more extensive capabilities as follows:</span></span>

-   <span data-ttu-id="f2335-112">Rimozione di un privilegio.</span><span class="sxs-lookup"><span data-stu-id="f2335-112">Removing a privilege.</span></span> <span data-ttu-id="f2335-113">Si noti che la rimozione di un privilegio non corrisponde alla disabilitazione di una.</span><span class="sxs-lookup"><span data-stu-id="f2335-113">Note that removing a privilege is not the same as disabling one.</span></span> <span data-ttu-id="f2335-114">Una volta rimosso un privilegio da un token, non è possibile ripristinarlo.</span><span class="sxs-lookup"><span data-stu-id="f2335-114">After a privilege is removed from a token, it cannot be put back.</span></span>
-   <span data-ttu-id="f2335-115">Associazione dell'attributo di sola negazione ai SID nel token.</span><span class="sxs-lookup"><span data-stu-id="f2335-115">Attaching the deny-only attribute to SIDs in the token.</span></span> <span data-ttu-id="f2335-116">Ciò comporta la disattivazione di gruppi o account specifici, ad esempio negando al gruppo Everyone l'accesso DELETE a un determinato file.</span><span class="sxs-lookup"><span data-stu-id="f2335-116">This has the effect of disallowing specific groups or accounts, for example, denying the Everyone group delete access to a particular file.</span></span> <span data-ttu-id="f2335-117">Per altre informazioni sulla restrizione dei SID, vedere [attributi SID in un token di accesso](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span><span class="sxs-lookup"><span data-stu-id="f2335-117">For more information on restricting SIDs, see [SID Attributes in an Access Token](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span></span>
-   <span data-ttu-id="f2335-118">Specificando un elenco di SID di restrizione nel token.</span><span class="sxs-lookup"><span data-stu-id="f2335-118">Specifying a list of restricting SIDs in the token.</span></span> <span data-ttu-id="f2335-119">Per informazioni sulla restrizione dei SID, vedere [token con restrizioni](/windows/desktop/SecAuthZ/restricted-tokens).</span><span class="sxs-lookup"><span data-stu-id="f2335-119">For information about restricting SIDs, see [Restricted Tokens](/windows/desktop/SecAuthZ/restricted-tokens).</span></span>

 

 
