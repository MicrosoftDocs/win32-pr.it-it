---
description: I seguenti elementi API vengono usati con i profili utente.
title: Riferimento ai profili utente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5d4c4f585eda66674059f402dbd73f106a3e4f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980711"
---
# <a name="user-profiles-reference"></a><span data-ttu-id="d3094-103">Riferimento ai profili utente</span><span class="sxs-lookup"><span data-stu-id="d3094-103">User Profiles Reference</span></span>

<span data-ttu-id="d3094-104">I seguenti elementi API vengono usati con i profili utente.</span><span class="sxs-lookup"><span data-stu-id="d3094-104">The following API elements are used with user profiles.</span></span>

## <a name="functions"></a><span data-ttu-id="d3094-105">Funzioni</span><span class="sxs-lookup"><span data-stu-id="d3094-105">Functions</span></span>



| <span data-ttu-id="d3094-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="d3094-106">Function</span></span>                                                                   | <span data-ttu-id="d3094-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3094-107">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3094-108">**CreateEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="d3094-108">**CreateEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | <span data-ttu-id="d3094-109">Recupera le variabili di ambiente per l'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="d3094-109">Retrieves the environment variables for the specified user.</span></span>                                                   |
| [<span data-ttu-id="d3094-110">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="d3094-110">**CreateProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | <span data-ttu-id="d3094-111">Crea un nuovo profilo utente.</span><span class="sxs-lookup"><span data-stu-id="d3094-111">Creates a new user profile.</span></span> <span data-ttu-id="d3094-112">(Solo Windows Vista e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="d3094-112">(Windows Vista and later only.)</span></span>                                                   |
| [<span data-ttu-id="d3094-113">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="d3094-113">**DeleteProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | <span data-ttu-id="d3094-114">Elimina il profilo utente e tutte le impostazioni relative agli utenti dal computer specificato.</span><span class="sxs-lookup"><span data-stu-id="d3094-114">Deletes the user profile and all user-related settings from the specified computer.</span></span>                           |
| [<span data-ttu-id="d3094-115">**DestroyEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="d3094-115">**DestroyEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | <span data-ttu-id="d3094-116">Libera le variabili di ambiente create dalla funzione [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) .</span><span class="sxs-lookup"><span data-stu-id="d3094-116">Frees environment variables created by the [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) function.</span></span> |
| [<span data-ttu-id="d3094-117">**ExpandEnvironmentStringsForUser**</span><span class="sxs-lookup"><span data-stu-id="d3094-117">**ExpandEnvironmentStringsForUser**</span></span>](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | <span data-ttu-id="d3094-118">Espande la stringa di origine usando il blocco dell'ambiente stabilito per l'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="d3094-118">Expands the source string by using the environment block established for the specified user.</span></span>                  |
| [<span data-ttu-id="d3094-119">**GetAllUsersProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="d3094-119">**GetAllUsersProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | <span data-ttu-id="d3094-120">Recupera il percorso della radice del profilo All Users.</span><span class="sxs-lookup"><span data-stu-id="d3094-120">Retrieves the path to the root of the All Users profile.</span></span>                                                      |
| [<span data-ttu-id="d3094-121">**GetDefaultUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="d3094-121">**GetDefaultUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | <span data-ttu-id="d3094-122">Recupera il percorso della radice del profilo utente predefinito.</span><span class="sxs-lookup"><span data-stu-id="d3094-122">Retrieves the path to the root of the Default User profile.</span></span>                                                   |
| [<span data-ttu-id="d3094-123">**GetProfilesDirectory**</span><span class="sxs-lookup"><span data-stu-id="d3094-123">**GetProfilesDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | <span data-ttu-id="d3094-124">Recupera il percorso della directory radice in cui sono archiviati tutti i profili utente.</span><span class="sxs-lookup"><span data-stu-id="d3094-124">Retrieves the path to the root directory where all user profiles are stored.</span></span>                                  |
| [<span data-ttu-id="d3094-125">**GetProfileType**</span><span class="sxs-lookup"><span data-stu-id="d3094-125">**GetProfileType**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | <span data-ttu-id="d3094-126">Recupera il tipo di profilo caricato per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="d3094-126">Retrieves the type of profile loaded for the current user.</span></span>                                                    |
| [<span data-ttu-id="d3094-127">**GetUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="d3094-127">**GetUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | <span data-ttu-id="d3094-128">Recupera il percorso della directory radice del profilo utente specificato.</span><span class="sxs-lookup"><span data-stu-id="d3094-128">Retrieves the path to the root directory of the specified user's profile.</span></span>                                     |
| [<span data-ttu-id="d3094-129">**LoadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="d3094-129">**LoadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | <span data-ttu-id="d3094-130">Carica il profilo utente specificato.</span><span class="sxs-lookup"><span data-stu-id="d3094-130">Loads the specified user's profile.</span></span>                                                                           |
| [<span data-ttu-id="d3094-131">**UnloadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="d3094-131">**UnloadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | <span data-ttu-id="d3094-132">Scarica un profilo utente caricato dalla funzione [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="d3094-132">Unloads a user's profile that was loaded by the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span>          |



 

<span data-ttu-id="d3094-133">La funzione [**CreateUserProfileEx**](createuserprofileex.md) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="d3094-133">The [**CreateUserProfileEx**](createuserprofileex.md) function is not supported.</span></span>

## <a name="structures"></a><span data-ttu-id="d3094-134">Strutture</span><span class="sxs-lookup"><span data-stu-id="d3094-134">Structures</span></span>



| <span data-ttu-id="d3094-135">Struttura</span><span class="sxs-lookup"><span data-stu-id="d3094-135">Structure</span></span>                          | <span data-ttu-id="d3094-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3094-136">Description</span></span>                                |
|------------------------------------|--------------------------------------------|
| [<span data-ttu-id="d3094-137">**PROFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="d3094-137">**PROFILEINFO**</span></span>](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | <span data-ttu-id="d3094-138">Contiene informazioni su un profilo utente.</span><span class="sxs-lookup"><span data-stu-id="d3094-138">Contains information about a user profile.</span></span> |



 

 

 



