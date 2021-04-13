---
title: Aggiunta di utenti a un gruppo
description: Joe worden, l'amministratore dell'organizzazione, ora aggiungerà Julie Bankert al gruppo di gestione. Per aggiungere un oggetto a un gruppo, usare il metodo IADsGroup. Add.
ms.assetid: 57a9f5b2-2e48-401d-8d3b-eceb711a1df9
ms.tgt_platform: multiple
keywords:
- Aggiunta di utenti a un gruppo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0ac78c0175248cb12e0f47a94ae60e7f1d16c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328460"
---
# <a name="adding-users-to-a-group"></a><span data-ttu-id="bce03-105">Aggiunta di utenti a un gruppo</span><span class="sxs-lookup"><span data-stu-id="bce03-105">Adding Users to a Group</span></span>

<span data-ttu-id="bce03-106">Joe worden, l'amministratore dell'organizzazione, ora aggiungerà Julie Bankert al gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="bce03-106">Joe Worden, the enterprise administrator, will now add Julie Bankert to the Management group.</span></span> <span data-ttu-id="bce03-107">Per aggiungere un oggetto a un gruppo, usare il metodo [**IADsGroup. Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) .</span><span class="sxs-lookup"><span data-stu-id="bce03-107">To add an object to a group, use the [**IADsGroup.Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) method.</span></span>


```VB
Dim grp as IADsGroup

Set grp = GetObject("LDAP://CN=Management,OU=Sales,DC=Fabrikam,DC=COM") 
grp.Add ("LDAP://CN=Julie Bankert,OU=Sales,DC=Fabrikam,DC=COM")
```



## <a name="related-topics"></a><span data-ttu-id="bce03-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bce03-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce03-109">Creazione di un nuovo gruppo</span><span class="sxs-lookup"><span data-stu-id="bce03-109">Creating a New Group</span></span>](creating-a-new-group.md)
</dt> </dl>

 

 




