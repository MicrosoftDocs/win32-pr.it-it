---
title: Gruppi su server membri e Windows 2000 Professional
description: Nei server membri e nei computer in cui è in esecuzione Windows 2000 Professional è disponibile un database di sicurezza locale.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Gruppi su server membri e Windows 2000 Professional AD
- gruppi di Active Directory, gruppi su server membri e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328484"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="856c1-105">Gruppi su server membri e Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="856c1-105">Groups on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="856c1-106">Nei server membri e nei computer in cui è in esecuzione Windows 2000 Professional è disponibile un database di sicurezza locale.</span><span class="sxs-lookup"><span data-stu-id="856c1-106">On member servers and computers running on Windows 2000 Professional, there is a local security database.</span></span> <span data-ttu-id="856c1-107">Questo database di sicurezza locale può contenere il proprio utente locale e i gruppi locali il cui ambito è solo il computer in cui sono stati creati.</span><span class="sxs-lookup"><span data-stu-id="856c1-107">This local security database can contain its own local user and local groups whose scope is only the particular computer where they are created.</span></span> <span data-ttu-id="856c1-108">Quando si gestiscono questi tipi di utenti e gruppi su server membri e computer in cui è in esecuzione la workstation Windows NT o Windows 2000 Professional, utilizzare il provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="856c1-108">When managing these types of users and groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="856c1-109">Quando un server membro o un computer in cui è in esecuzione Windows 2000 Professional o Windows 2000 Professional è membro di un dominio Windows 2000, i gruppi o gli utenti del dominio possono essere utilizzati nel database di sicurezza locale per concedere diritti a tale gruppo in quel particolare computer.</span><span class="sxs-lookup"><span data-stu-id="856c1-109">When a member server or a computer running on Windows 2000 Professional or Windows 2000 Professional is a member of a Windows 2000 domain, the groups or users in the domain can be used in the local security database to grant rights to that group on that particular computer.</span></span>

<span data-ttu-id="856c1-110">Quando si gestiscono i gruppi in un dominio Windows 2000 usando ADSI, usare il provider LDAP.</span><span class="sxs-lookup"><span data-stu-id="856c1-110">When managing groups on a Windows 2000 domain using ADSI, use the LDAP provider.</span></span> <span data-ttu-id="856c1-111">Quando si gestiscono gruppi su server membri e computer in cui è in esecuzione la workstation Windows NT o Windows 2000 Professional, utilizzare il provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="856c1-111">When managing groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="856c1-112">È necessario associare almeno un'istanza a ogni provider: 1) eseguire l'associazione al provider LDAP per recuperare ADsPath al gruppo o all'utente che si desidera aggiungere a un gruppo nel database locale e 2) eseguire l'associazione al provider WinNT per aggiungere tale utente o gruppo a un gruppo locale.</span><span class="sxs-lookup"><span data-stu-id="856c1-112">You must bind, at least one instance, to each provider: 1) Bind to the LDAP provider to retrieve the ADsPath to the group or user you want to add to a group in the local database and 2) Bind to the WinNT provider to add that user or group to a local group.</span></span>

 

 




