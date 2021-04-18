---
description: Sostituzioni amministratore
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Sostituzioni amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312071"
---
# <a name="administrator-overrides"></a><span data-ttu-id="a4a83-103">Sostituzioni amministratore</span><span class="sxs-lookup"><span data-stu-id="a4a83-103">Administrator Overrides</span></span>

<span data-ttu-id="a4a83-104">Windows dispone di un singolo elenco di controllo di accesso (ACL) predefinito per tutti gli oggetti Criteri di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a4a83-104">Windows has a single default access control list (ACL) on all power policy objects.</span></span> <span data-ttu-id="a4a83-105">L'ACL concede le autorizzazioni di lettura, scrittura e modifica ai membri del gruppo Authenticated Users.</span><span class="sxs-lookup"><span data-stu-id="a4a83-105">The ACL grants read, write, and change permissions to members of the Authenticated Users group.</span></span> <span data-ttu-id="a4a83-106">A tutti gli altri utenti viene concessa l'autorizzazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a4a83-106">All other users are granted read-only permission.</span></span> <span data-ttu-id="a4a83-107">Le applicazioni che chiamano funzioni dei criteri di risparmio energia possono determinare se un utente dispone delle autorizzazioni per un'impostazione di risparmio energia specificata tramite la funzione [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="a4a83-107">Applications that call power policy functions can determine whether a user has permissions for a specified power setting by using the [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) function.</span></span>

<span data-ttu-id="a4a83-108">È possibile eseguire l'override delle impostazioni di risparmio energia tramite Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="a4a83-108">Power settings may be overridden via Group Policy.</span></span> <span data-ttu-id="a4a83-109">Le sostituzioni possono essere impostate tramite criteri di gruppo di dominio o criteri di gruppo locali.</span><span class="sxs-lookup"><span data-stu-id="a4a83-109">Overrides can be set through domain group policy or local group policy.</span></span> <span data-ttu-id="a4a83-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) segnala se per un'impostazione di risparmio energia specificata è presente un override di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="a4a83-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) will report if a specified power setting has a group policy override.</span></span>

<span data-ttu-id="a4a83-111">Lo strumento da riga di comando **PowerCfg.exe** Visualizza un messaggio di errore quando non è possibile completare un comando perché l'utente non dispone delle autorizzazioni per modificare l'impostazione di risparmio energia o perché per l'impostazione di risparmio energia è stato eseguito un override di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="a4a83-111">The command line tool **PowerCfg.exe** displays an error message when a command cannot be completed either because the user did not have permissions to change the power setting or because the power setting has a group policy override.</span></span>

<span data-ttu-id="a4a83-112">L'applicazione Opzioni risparmio energia nel pannello di controllo non offre il supporto per la configurazione delle autorizzazioni di accesso ai criteri di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a4a83-112">The Power Options application in Control Panel does not provide support for configuring power policy access permissions.</span></span> <span data-ttu-id="a4a83-113">La modifica delle autorizzazioni deve essere eseguita tramite **PowerCfg.exe**.</span><span class="sxs-lookup"><span data-stu-id="a4a83-113">Changing permissions must be done via **PowerCfg.exe**.</span></span>

 

 



