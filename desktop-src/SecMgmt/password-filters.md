---
description: Filtri password
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtri password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233682"
---
# <a name="password-filters"></a><span data-ttu-id="99d03-103">Filtri password</span><span class="sxs-lookup"><span data-stu-id="99d03-103">Password Filters</span></span>

<span data-ttu-id="99d03-104">I filtri password consentono di implementare i criteri password e le notifiche di modifica.</span><span class="sxs-lookup"><span data-stu-id="99d03-104">Password filters provide a way for you to implement password policy and change notification.</span></span>

<span data-ttu-id="99d03-105">Quando viene effettuata una richiesta di modifica della password, l' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) chiama i filtri password registrati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="99d03-105">When a password change request is made, the [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) calls the password filters registered on the system.</span></span> <span data-ttu-id="99d03-106">Ogni filtro password viene chiamato due volte: prima per convalidare la nuova password e quindi, dopo che tutti i filtri hanno convalidato la nuova password, per notificare ai filtri che è stata apportata la modifica.</span><span class="sxs-lookup"><span data-stu-id="99d03-106">Each password filter is called twice: first to validate the new password and then, after all filters have validated the new password, to notify the filters that the change has been made.</span></span> <span data-ttu-id="99d03-107">Questo processo viene illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="99d03-107">The following illustration shows this process.</span></span>

![richiesta di modifica della password](images/pswdfilte.png)

<span data-ttu-id="99d03-109">La notifica di modifica della password viene usata per sincronizzare le modifiche delle password con i database degli account esterni.</span><span class="sxs-lookup"><span data-stu-id="99d03-109">Password change notification is used to synchronize password changes to foreign account databases.</span></span>

<span data-ttu-id="99d03-110">I filtri password vengono usati per applicare i criteri password.</span><span class="sxs-lookup"><span data-stu-id="99d03-110">Password filters are used to enforce password policy.</span></span> <span data-ttu-id="99d03-111">I filtri convalidano le nuove password e indicano se la nuova password è conforme ai criteri di password implementati.</span><span class="sxs-lookup"><span data-stu-id="99d03-111">Filters validate new passwords and indicate whether the new password conforms to the implemented password policy.</span></span>

<span data-ttu-id="99d03-112">Per una panoramica dell'uso dei filtri password, vedere [using password filters](using-password-filters.md).</span><span class="sxs-lookup"><span data-stu-id="99d03-112">For an overview of using password filters, see [Using Password Filters](using-password-filters.md).</span></span>

<span data-ttu-id="99d03-113">Per un elenco delle funzioni di filtro delle password, vedere [funzioni di filtro delle password](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="99d03-113">For a list of password filter functions, see [Password Filter Functions](management-functions.md).</span></span>

<span data-ttu-id="99d03-114">Negli argomenti seguenti vengono fornite ulteriori informazioni sui filtri password:</span><span class="sxs-lookup"><span data-stu-id="99d03-114">The following topics provide more information about password filters:</span></span>

-   [<span data-ttu-id="99d03-115">Considerazioni sulla programmazione del filtro password</span><span class="sxs-lookup"><span data-stu-id="99d03-115">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
-   [<span data-ttu-id="99d03-116">Imposizione avanzata delle password e Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="99d03-116">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)

 

 
