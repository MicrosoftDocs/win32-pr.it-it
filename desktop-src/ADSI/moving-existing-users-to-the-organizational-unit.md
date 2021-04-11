---
title: Trasferimento di utenti esistenti all'unità organizzativa
description: Quando l'amministratore dell'organizzazione, Joe worden, aggiorna il dominio di Windows NT 4,0 per Active Directory, viene eseguita la migrazione di tutti gli utenti e gruppi ai contenitori di utenti nel dominio fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Trasferimento di utenti esistenti all'unità organizzativa AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220911"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a><span data-ttu-id="250ef-104">Trasferimento di utenti esistenti all'unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="250ef-104">Moving Existing Users to the Organizational Unit</span></span>

<span data-ttu-id="250ef-105">Quando l'amministratore dell'organizzazione, Joe worden, aggiorna il dominio di Windows NT 4,0 per Active Directory, viene eseguita la migrazione di tutti gli utenti e gruppi ai contenitori di utenti nel dominio fabrikam.</span><span class="sxs-lookup"><span data-stu-id="250ef-105">When the enterprise administrator, Joe Worden, upgrades the Windows NT 4.0 domain to Active Directory, all users and groups are migrated to the Users containers in the Fabrikam domain.</span></span> <span data-ttu-id="250ef-106">Joe può ora spostare tali utenti e gruppi nelle unità organizzative appropriate.</span><span class="sxs-lookup"><span data-stu-id="250ef-106">Joe can now move those users and groups to the appropriate organizational units.</span></span> <span data-ttu-id="250ef-107">Un oggetto può anche essere spostato tra domini Windows 2000 correlati tramite ADSI.</span><span class="sxs-lookup"><span data-stu-id="250ef-107">An object can also be moved between related Windows 2000 domains using ADSI.</span></span>

<span data-ttu-id="250ef-108">Nell'esempio di codice seguente Joe sposta "SergioMelchiori" nell'organizzazione delle vendite.</span><span class="sxs-lookup"><span data-stu-id="250ef-108">In the following code example, Joe moves "jeffsmith" to the Sales organization.</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



<span data-ttu-id="250ef-109">Il metodo [**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) accetta il ADsPath dell'oggetto da spostare e il nuovo nome di oggetto (RDN).</span><span class="sxs-lookup"><span data-stu-id="250ef-109">The [**IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) method takes the ADsPath of the object to be moved and the new object name (RDN).</span></span> <span data-ttu-id="250ef-110">Per avere lo stesso nome, è possibile specificare **null** (**vbNullString**) per il parametro *bstrNewName* .</span><span class="sxs-lookup"><span data-stu-id="250ef-110">To keep the same name, you can specify **NULL** (**vbNullString**) for the *bstrNewName* parameter.</span></span> <span data-ttu-id="250ef-111">Per rinominare l'oggetto quando viene spostato, specificare il nuovo nome distinto relativo per il parametro *bstrNewName* .</span><span class="sxs-lookup"><span data-stu-id="250ef-111">To rename the object when it is moved, specify the new relative distinguished name for the *bstrNewName* parameter.</span></span> <span data-ttu-id="250ef-112">Ad esempio, per spostare SergioMelchiori nell'organizzazione vendite e rinominare l'oggetto "SergioMelchiori" in "Jeff \_ Smith" nella stessa operazione, Joe eseguirà il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="250ef-112">For example, to move jeffsmith to the sales organization and rename the "jeffsmith" object to "jeff\_smith" in the same operation, Joe would execute the following code:</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a><span data-ttu-id="250ef-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="250ef-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="250ef-114">Creazione di nuovi utenti nell'unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="250ef-114">Creating New Users in the Organizational Unit</span></span>](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




