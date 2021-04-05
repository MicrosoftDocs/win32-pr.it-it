---
title: Rimozione di membri da gruppi in un dominio
description: È possibile rimuovere utenti, gruppi o contatti dai gruppi.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- gruppi AD, rimozione di membri da gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724447"
---
# <a name="removing-members-from-groups-in-a-domain"></a><span data-ttu-id="08299-104">Rimozione di membri da gruppi in un dominio</span><span class="sxs-lookup"><span data-stu-id="08299-104">Removing Members from Groups in a Domain</span></span>

<span data-ttu-id="08299-105">È possibile rimuovere utenti, gruppi o contatti dai gruppi.</span><span class="sxs-lookup"><span data-stu-id="08299-105">You can remove users, groups, or contacts from groups.</span></span> <span data-ttu-id="08299-106">L'attributo **member** dell'oggetto **Group** contiene tutti i membri diretti del gruppo.</span><span class="sxs-lookup"><span data-stu-id="08299-106">The **member** attribute of the **group** object contains all direct members of the group.</span></span>

<span data-ttu-id="08299-107">Il modo più semplice per rimuovere un membro da un gruppo consiste nel chiamare il metodo [**IADsGroup. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) sull'interfaccia [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) dell'oggetto gruppo da cui si vogliono rimuovere i membri.</span><span class="sxs-lookup"><span data-stu-id="08299-107">The simplest way to remove a member from a group is to call the [**IADsGroup.Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) method on the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface of the group object you want to remove members from.</span></span>

 

 