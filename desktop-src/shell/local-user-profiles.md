---
description: Il sistema crea automaticamente un profilo utente locale per ogni utente quando l'utente accede al computer per la prima volta. Il sistema gestisce automaticamente le impostazioni per l'ambiente di lavoro di ogni utente in un profilo utente nel computer locale.
title: Profili utente locale
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980015"
---
# <a name="local-user-profiles"></a><span data-ttu-id="ab6ca-104">Profili utente locale</span><span class="sxs-lookup"><span data-stu-id="ab6ca-104">Local User Profiles</span></span>

<span data-ttu-id="ab6ca-105">Per la sicurezza di Windows è necessario un profilo utente per ogni account utente in un computer.</span><span class="sxs-lookup"><span data-stu-id="ab6ca-105">Windows security requires a user profile for each user account on a computer.</span></span> <span data-ttu-id="ab6ca-106">Il sistema crea automaticamente un *profilo utente locale* per ogni utente quando l'utente accede al computer per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="ab6ca-106">The system automatically creates a *local user profile* for each user when the user logs on to the computer for the first time.</span></span> <span data-ttu-id="ab6ca-107">Il sistema gestisce automaticamente le impostazioni per l'ambiente di lavoro di ogni utente in un profilo utente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="ab6ca-107">The system automatically maintains the settings for each user's work environment in a user profile on the local computer.</span></span>

<span data-ttu-id="ab6ca-108">Windows Vista e versioni successive: i profili utente vengono gestiti tramite l'elemento del pannello di controllo degli **account utente** .</span><span class="sxs-lookup"><span data-stu-id="ab6ca-108">Windows Vista and later: User profiles are managed through the **User Accounts** control panel item.</span></span>

<span data-ttu-id="ab6ca-109">Windows 2000 e Windows XP: per copiare o eliminare un profilo utente, selezionare **sistema** dal pannello di controllo, quindi la scheda **Avanzate** , quindi il pulsante **Impostazioni** nell'area **profilo utente** .</span><span class="sxs-lookup"><span data-stu-id="ab6ca-109">Windows 2000 and Windows XP: To copy or delete a user profile, select **System** from the Control Panel, then the **Advanced** tab, and then the **Settings** button in the **User Profile** area.</span></span>

<span data-ttu-id="ab6ca-110">Il profilo dell'utente non viene caricato automaticamente quando l'utente è connesso tramite la funzione [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="ab6ca-110">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="ab6ca-111">Per caricare un profilo utente a livello di codice, usare la funzione [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="ab6ca-111">To load a user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="ab6ca-112">Per scaricare un profilo utente caricato da **LoadUserProfile**, chiamare la funzione [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="ab6ca-112">To unload a user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
