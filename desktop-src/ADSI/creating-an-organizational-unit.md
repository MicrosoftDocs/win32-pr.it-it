---
title: Creazione di un'unità organizzativa
description: Ora che si dispone dell'oggetto dominio, è possibile iniziare a creare unità organizzative.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Creazione di un'unità organizzativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955105"
---
# <a name="creating-an-organizational-unit"></a><span data-ttu-id="bda5e-104">Creazione di un'unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="bda5e-104">Creating an Organizational Unit</span></span>

<span data-ttu-id="bda5e-105">Ora che si dispone dell'oggetto dominio, è possibile iniziare a creare unità organizzative.</span><span class="sxs-lookup"><span data-stu-id="bda5e-105">Now that you have the domain object, you can start creating organizational units.</span></span> <span data-ttu-id="bda5e-106">Fabrikam è costituito da due divisioni: vendite e produzione.</span><span class="sxs-lookup"><span data-stu-id="bda5e-106">Fabrikam has two divisions: Sales and Production.</span></span> <span data-ttu-id="bda5e-107">La società sta pianificando di assumere due amministratori di Windows 2000 per gestire ogni divisione.</span><span class="sxs-lookup"><span data-stu-id="bda5e-107">The company is planning to hire two Windows 2000 administrators to manage each division.</span></span> <span data-ttu-id="bda5e-108">Joe worden, come amministratore dell'organizzazione, creerà due nuove unità organizzative nel dominio fabrikam.</span><span class="sxs-lookup"><span data-stu-id="bda5e-108">Joe Worden, as the enterprise administrator, will create two new organizational units under the Fabrikam domain.</span></span> <span data-ttu-id="bda5e-109">Grazie alla creazione di un'unità organizzativa, Joe può raggruppare più oggetti e consentire a un altro utente di gestire questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="bda5e-109">By creating an organizational unit, Joe can group multiple objects together and let someone else manage these objects.</span></span> <span data-ttu-id="bda5e-110">Nell'esempio di codice seguente viene creata l'unità organizzativa Sales (OU).</span><span class="sxs-lookup"><span data-stu-id="bda5e-110">The following code example creates the Sales Organizational Unit (OU).</span></span>


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



<span data-ttu-id="bda5e-111">Il metodo [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) accetta il nome della classe e il nome del nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="bda5e-111">The [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) method accepts the class name and the name of the new object.</span></span> <span data-ttu-id="bda5e-112">A questo punto non viene eseguito il commit dell'oggetto per Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bda5e-112">At this point the object is not committed to Active Directory.</span></span> <span data-ttu-id="bda5e-113">Tuttavia, nel client sarà presente un riferimento a un oggetto ADSI/COM.</span><span class="sxs-lookup"><span data-stu-id="bda5e-113">You, however, will have an ADSI/COM object reference on the client.</span></span> <span data-ttu-id="bda5e-114">Con questo oggetto ADSI è possibile impostare o modificare gli attributi usando il metodo [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="bda5e-114">With this ADSI object, you can set or modify attributes using the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span> <span data-ttu-id="bda5e-115">Il metodo **IADs. Put** accetta il nome dell'attributo e il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="bda5e-115">The **IADs.Put** method accepts the attribute name and the value of the attribute.</span></span> <span data-ttu-id="bda5e-116">Tuttavia, non viene eseguito il commit di alcun elemento nella directory; tutto viene memorizzato nella cache del client.</span><span class="sxs-lookup"><span data-stu-id="bda5e-116">Still, nothing is committed to the directory; everything is cached at the client.</span></span> <span data-ttu-id="bda5e-117">Quando si chiama il metodo [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , viene eseguito il commit delle modifiche, in questo caso la creazione di oggetti e la modifica degli attributi, nella directory.</span><span class="sxs-lookup"><span data-stu-id="bda5e-117">When you call the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method, the changes, in this case, object creation and attribute modification, are committed to the directory.</span></span> <span data-ttu-id="bda5e-118">Queste modifiche sono transazionali, pertanto verrà visualizzato il nuovo oggetto con tutti gli attributi impostati o nessun oggetto.</span><span class="sxs-lookup"><span data-stu-id="bda5e-118">These changes are transacted, meaning that you will see either the new object with all attributes you set, or no object at all.</span></span>

<span data-ttu-id="bda5e-119">È anche possibile annidare unità organizzative.</span><span class="sxs-lookup"><span data-stu-id="bda5e-119">You can also nest organizational units.</span></span> <span data-ttu-id="bda5e-120">Nell'esempio di codice seguente si presuppone che la divisione Sales venga divisa ulteriormente nelle aree East e West.</span><span class="sxs-lookup"><span data-stu-id="bda5e-120">The following code example assumes that the Sales division is divided further into the East and West regions.</span></span>


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



<span data-ttu-id="bda5e-121">Questo vale anche per l'area ovest.</span><span class="sxs-lookup"><span data-stu-id="bda5e-121">This also applies for the West region.</span></span>

<span data-ttu-id="bda5e-122">Per eseguire il binding direttamente all'area est nell'organizzazione vendite, specificare il nome distinto.</span><span class="sxs-lookup"><span data-stu-id="bda5e-122">To bind directly to the East region in the Sales organization, specify the distinguished name.</span></span>


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



<span data-ttu-id="bda5e-123">Se è già stato associato all'oggetto padre (Sales), è possibile eseguire l'associazione all'oggetto figlio (East) dall'oggetto padre utilizzando il nome relativo dell'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="bda5e-123">If you have already bound to the parent object (Sales), you can bind to the child object (East) from the parent object using the relative name of the child object.</span></span>


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



<span data-ttu-id="bda5e-124">Per assicurarsi che gli oggetti siano stati creati, utilizzare lo snap-in MMC utenti e computer Active Directory per visualizzare le nuove unità organizzative.</span><span class="sxs-lookup"><span data-stu-id="bda5e-124">To ensure that the objects have been created, use the Active Directory Users and Computers MMC snap-in to view the new organizational units.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bda5e-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bda5e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bda5e-126">Trasferimento di utenti esistenti all'unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="bda5e-126">Moving Existing Users to the Organizational Unit</span></span>](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




