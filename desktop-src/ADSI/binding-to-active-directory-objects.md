---
title: Associazione a oggetti Active Directory
description: Prima di continuare con questo scenario, è necessario comprendere in che modo gli oggetti ADSI vengono denominati in Active Directory e come associarli. Il binding di un oggetto ADSI connette l'oggetto al servizio directory e consente di accedere ai metodi dell'oggetto.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044073"
---
# <a name="binding-to-active-directory-objects"></a><span data-ttu-id="64127-104">Associazione a oggetti Active Directory</span><span class="sxs-lookup"><span data-stu-id="64127-104">Binding to Active Directory Objects</span></span>

<span data-ttu-id="64127-105">Prima di continuare con questo scenario, è necessario comprendere in che modo gli oggetti ADSI vengono denominati in Active Directory e come associarli.</span><span class="sxs-lookup"><span data-stu-id="64127-105">Before you continue with this scenario, you must understand how ADSI objects are named in Active Directory, and how to bind them.</span></span> <span data-ttu-id="64127-106">Il binding di un oggetto ADSI connette l'oggetto al servizio directory e consente di accedere ai metodi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="64127-106">Binding an ADSI object connects the object with the directory service, and allows you to access the methods of the object.</span></span>

## <a name="adspath"></a><span data-ttu-id="64127-107">ADsPath</span><span class="sxs-lookup"><span data-stu-id="64127-107">ADsPath</span></span>

<span data-ttu-id="64127-108">Un oggetto ADSI viene identificato in modo univoco dalla relativa stringa di associazione, definita anche ADsPath.</span><span class="sxs-lookup"><span data-stu-id="64127-108">An ADSI object is uniquely identified by its binding string, which is also referred to as an ADsPath.</span></span> <span data-ttu-id="64127-109">Un ADsPath è una combinazione di un identificatore a livello di codice (progID) del provider ADSI e del nome distinto (DN) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="64127-109">An ADsPath is a combination of a programmatic identifier (progID) of the ADSI provider, and the distinguished name (DN) of the object.</span></span>

<span data-ttu-id="64127-110">Ecco il formato di un ADsPath:</span><span class="sxs-lookup"><span data-stu-id="64127-110">Here's the format of an ADsPath:</span></span>

<span data-ttu-id="64127-111">"progID://DN"</span><span class="sxs-lookup"><span data-stu-id="64127-111">"progID://DN"</span></span>

-   <span data-ttu-id="64127-112">pogID: identificatore a livello di codice del provider ADSI, ad esempio LDAP o WinNT.</span><span class="sxs-lookup"><span data-stu-id="64127-112">pogID — the programmatic identifier of the ADSI provider, such as LDAP or WinNT.</span></span>

-   <span data-ttu-id="64127-113">://-separa il progID dal DN.</span><span class="sxs-lookup"><span data-stu-id="64127-113">:// — separates the progID from the DN.</span></span>

-   <span data-ttu-id="64127-114">DN: nome distinto dell'oggetto ADSI, ovvero il percorso completo dell'oggetto, in cui il percorso è costituito da nomi distinti relativi (RDNs).</span><span class="sxs-lookup"><span data-stu-id="64127-114">DN — the distinguished name of the ADSI object, which is the full path of the object, where the path consists of relative distinguished names (RDNs).</span></span>

<span data-ttu-id="64127-115">Un RDN è il nome dell'oggetto senza il percorso ed è univoco dagli oggetti di pari livello.</span><span class="sxs-lookup"><span data-stu-id="64127-115">An RDN is the name of the object without the path, and is unique from its sibling objects.</span></span> <span data-ttu-id="64127-116">Un RDN è costituito da un ID e un valore di attributo, ad esempio "DC = Fabrikam", dove DC è l'attributo e Fabrikam è il valore.</span><span class="sxs-lookup"><span data-stu-id="64127-116">An RDN consists of an attribute ID and value, such as "DC=Fabrikam", where DC is the attribute, and Fabrikam is the value.</span></span> <span data-ttu-id="64127-117">Il controller di dominio è un ID di attributo RDN che corrisponde al componente di dominio.</span><span class="sxs-lookup"><span data-stu-id="64127-117">DC is an RDN attribute ID that stands for domain component.</span></span>

<span data-ttu-id="64127-118">Di seguito è riportato un esempio di ADsPath:</span><span class="sxs-lookup"><span data-stu-id="64127-118">Here’s an example of an ADsPath:</span></span>

<span data-ttu-id="64127-119">"LDAP://DC = Fabrikam, DC = com"</span><span class="sxs-lookup"><span data-stu-id="64127-119">"LDAP://DC=Fabrikam,DC=Com"</span></span>

## <a name="binding-the-object"></a><span data-ttu-id="64127-120">Associazione dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="64127-120">Binding the object</span></span>

<span data-ttu-id="64127-121">Ecco come è possibile associare l'oggetto dominio in questo scenario:</span><span class="sxs-lookup"><span data-stu-id="64127-121">Here's how you can bind the domain object in this scenario:</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



<span data-ttu-id="64127-122">Quando si esegue questo esempio di codice, ADSI usa il DN per determinare gli oggetti ADSI da associare.</span><span class="sxs-lookup"><span data-stu-id="64127-122">When you run this code example, ADSI uses the DN to determine the ADSI objects to bind.</span></span> <span data-ttu-id="64127-123">Dopo aver associato tali oggetti, è possibile accedere ai relativi metodi.</span><span class="sxs-lookup"><span data-stu-id="64127-123">After ADSI binds these objects, you can access their methods.</span></span> <span data-ttu-id="64127-124">Nell'esempio di codice precedente viene associato un oggetto di dominio a [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="64127-124">The previous code example binds a domain object to [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="64127-125">È ora possibile usare metodi su tali interfacce, ad esempio [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)e [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span><span class="sxs-lookup"><span data-stu-id="64127-125">You can now use methods on those interfaces such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete), and [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span></span>

<span data-ttu-id="64127-126">Dopo aver associato un oggetto di dominio, è possibile stampare alcuni degli attributi:</span><span class="sxs-lookup"><span data-stu-id="64127-126">After you bind a domain object, you can print some of its attributes:</span></span>


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



<span data-ttu-id="64127-127">Per ulteriori informazioni su ADsPath, vedere [Binding String](binding-string.md).</span><span class="sxs-lookup"><span data-stu-id="64127-127">For more information about ADsPath, see [Binding String](binding-string.md).</span></span> <span data-ttu-id="64127-128">Per ulteriori informazioni sull'associazione, vedere [associazione a un oggetto ADSI](binding-to-an-adsi-object.md).</span><span class="sxs-lookup"><span data-stu-id="64127-128">For more information about binding, see [Binding to an ADSI Object](binding-to-an-adsi-object.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="64127-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64127-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64127-130">Creazione di un'unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="64127-130">Creating an Organizational Unit</span></span>](creating-an-organizational-unit.md)
</dt> </dl>

 

 




