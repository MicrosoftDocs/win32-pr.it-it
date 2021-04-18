---
title: Funzioni utente workstation e workstation
description: Le funzioni di workstation di gestione di rete eseguono attività amministrative su una workstation locale o remota.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300282"
---
# <a name="workstation-and-workstation-user-functions"></a><span data-ttu-id="9c9b2-103">Funzioni utente workstation e workstation</span><span class="sxs-lookup"><span data-stu-id="9c9b2-103">Workstation and Workstation User Functions</span></span>

<span data-ttu-id="9c9b2-104">Le funzioni di workstation di gestione di rete eseguono attività amministrative su una workstation locale o remota.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-104">The network management workstation functions perform administrative tasks on a local or remote workstation.</span></span> <span data-ttu-id="9c9b2-105">Solo un utente o un'applicazione con appartenenza a un gruppo di amministratori, in un server locale o remoto, può eseguire attività amministrative su una workstation per controllarne il funzionamento, l'accesso degli utenti e la condivisione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-105">Only a user or application with admin group membership, on a local or remote server, can perform administrative tasks on a workstation to control its operation, user access, and resource sharing.</span></span> <span data-ttu-id="9c9b2-106">Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="9c9b2-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="9c9b2-107">Le funzioni workstation sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-107">The workstation functions are listed following.</span></span>



| <span data-ttu-id="9c9b2-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="9c9b2-108">Function</span></span>                                   | <span data-ttu-id="9c9b2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c9b2-109">Description</span></span>                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="9c9b2-110">**NetWkstaGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-110">**NetWkstaGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | <span data-ttu-id="9c9b2-111">Restituisce informazioni sugli elementi di configurazione per una workstation.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-111">Returns information about the configuration elements for a workstation.</span></span> |
| [<span data-ttu-id="9c9b2-112">**NetWkstaSetInfo**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-112">**NetWkstaSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | <span data-ttu-id="9c9b2-113">Configura una workstation.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-113">Configures a workstation.</span></span>                                               |



 

<span data-ttu-id="9c9b2-114">Le funzioni workstation consentono l'accesso a due tipi discreti di informazioni sulle workstation:</span><span class="sxs-lookup"><span data-stu-id="9c9b2-114">The workstation functions allow access to two discrete types of workstation information:</span></span>

-   <span data-ttu-id="9c9b2-115">Informazioni di sistema</span><span class="sxs-lookup"><span data-stu-id="9c9b2-115">System information</span></span>
-   <span data-ttu-id="9c9b2-116">Informazioni specifiche della piattaforma</span><span class="sxs-lookup"><span data-stu-id="9c9b2-116">Platform-specific information</span></span>

<span data-ttu-id="9c9b2-117">All'interno di ogni tipo i dati vengono classificati in base all'accesso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-117">Within each type the data is categorized by security access.</span></span> <span data-ttu-id="9c9b2-118">I dati accessibili dal Guest sono un subset dei dati accessibili dagli utenti, che a sua volta costituisce un subset dei dati accessibili dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-118">Data that is guest-accessible is a subset of the data that is user-accessible, which is in turn a subset of the admin-accessible data.</span></span>

<span data-ttu-id="9c9b2-119">Le informazioni sulla workstation sono disponibili ai livelli seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c9b2-119">Workstation information is available at the following levels:</span></span>

-   [<span data-ttu-id="9c9b2-120">**WKSTA \_ INFO \_ 100**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-120">**WKSTA\_INFO\_100**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [<span data-ttu-id="9c9b2-121">**WKSTA \_ INFO \_ 101**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-121">**WKSTA\_INFO\_101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [<span data-ttu-id="9c9b2-122">**WKSTA \_ INFO \_ 102**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-122">**WKSTA\_INFO\_102**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

<span data-ttu-id="9c9b2-123">Le funzioni utente della workstation di gestione di rete consentono l'accesso a informazioni specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-123">The network management workstation user functions allow access to user-specific information.</span></span> <span data-ttu-id="9c9b2-124">Le informazioni specifiche dell'utente sono separate dalle informazioni della workstation perché possono essere presenti più utenti su una workstation.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-124">The user-specific information is separated from the workstation information because there can be more than one user on a workstation.</span></span>

<span data-ttu-id="9c9b2-125">Le funzioni utente della workstation sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-125">The workstation user functions are listed following.</span></span>



| <span data-ttu-id="9c9b2-126">Funzione</span><span class="sxs-lookup"><span data-stu-id="9c9b2-126">Function</span></span>                                           | <span data-ttu-id="9c9b2-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c9b2-127">Description</span></span>                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c9b2-128">**NetWkstaUserEnum**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-128">**NetWkstaUserEnum**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | <span data-ttu-id="9c9b2-129">Elenca le informazioni su tutti gli utenti attualmente connessi alla workstation.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-129">Lists information about all users currently logged on to the workstation.</span></span>           |
| [<span data-ttu-id="9c9b2-130">**NetWkstaUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-130">**NetWkstaUserGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | <span data-ttu-id="9c9b2-131">Restituisce informazioni su un utente attualmente connesso.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-131">Returns information about one currently logged-on user.</span></span>                             |
| [<span data-ttu-id="9c9b2-132">**NetWkstaUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-132">**NetWkstaUserSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | <span data-ttu-id="9c9b2-133">Imposta le informazioni specifiche dell'utente per gli elementi di configurazione di una workstation.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-133">Sets the user-specific information for the configuration elements of a workstation.</span></span> |



 

<span data-ttu-id="9c9b2-134">Le informazioni sull'utente della workstation sono disponibili ai livelli seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c9b2-134">Workstation user information is available at the following levels:</span></span>

-   [<span data-ttu-id="9c9b2-135">**\_Informazioni utente \_ WKSTA \_ 0**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-135">**WKSTA\_USER\_INFO\_0**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [<span data-ttu-id="9c9b2-136">**\_Informazioni utente \_ WKSTA \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-136">**WKSTA\_USER\_INFO\_1**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [<span data-ttu-id="9c9b2-137">**\_Informazioni utente \_ WKSTA \_ 1101**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-137">**WKSTA\_USER\_INFO\_1101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 