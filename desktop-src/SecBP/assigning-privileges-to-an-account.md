---
description: È possibile assegnare privilegi agli account tramite lo snap-in criteri di sicurezza locali (secpol. msc) o chiamando la funzione LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Assegnazione di privilegi a un account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315423"
---
# <a name="assigning-privileges-to-an-account"></a><span data-ttu-id="084e2-103">Assegnazione di privilegi a un account</span><span class="sxs-lookup"><span data-stu-id="084e2-103">Assigning Privileges to an Account</span></span>

<span data-ttu-id="084e2-104">È possibile assegnare privilegi agli account tramite lo snap-in criteri di sicurezza locali (secpol. msc) o chiamando la funzione [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) .</span><span class="sxs-lookup"><span data-stu-id="084e2-104">You can assign privileges to accounts either by using the Local Security Policy Microsoft Management Console (MMC) snap-in (Secpol.msc) or by calling the [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) function.</span></span>

<span data-ttu-id="084e2-105">L'assegnazione di un privilegio a un account non influisce sui token utente esistenti.</span><span class="sxs-lookup"><span data-stu-id="084e2-105">Assigning a privilege to an account does not affect existing user tokens.</span></span> <span data-ttu-id="084e2-106">Un utente deve disconnettersi e quindi eseguire di nuovo l'accesso per ottenere un token di accesso con il privilegio appena assegnato.</span><span class="sxs-lookup"><span data-stu-id="084e2-106">A user must log off and then log back on to get an access token with the newly assigned privilege.</span></span>

<span data-ttu-id="084e2-107">Per assegnare privilegi tramite lo snap-in MMC Criteri di sicurezza locali, modificare l'elenco di utenti per ogni privilegio elencato in **impostazioni di sicurezza/Criteri locali/Assegnazione diritti utente**.</span><span class="sxs-lookup"><span data-stu-id="084e2-107">To assign privileges by using the Local Security Policy MMC snap-in, edit the list of users for each privilege listed under **Security Settings/Local Policies/User Rights Assignment**.</span></span>

 

 
