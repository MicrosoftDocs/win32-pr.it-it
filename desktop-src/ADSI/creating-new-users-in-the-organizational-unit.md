---
title: Creazione di nuovi utenti nell'unità organizzativa
description: Terry Adams è stato assunto nell'organizzazione vendite di Fabrikam. Il suo report diretto è Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Creazione di nuovi utenti nell'unità organizzativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470806"
---
# <a name="creating-new-users-in-the-organizational-unit"></a><span data-ttu-id="78bc5-105">Creazione di nuovi utenti nell'unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="78bc5-105">Creating New Users in the Organizational Unit</span></span>

<span data-ttu-id="78bc5-106">Terry Adams è stato assunto nell'organizzazione vendite di Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="78bc5-106">Terry Adams was hired into the Fabrikam Sales organization.</span></span> <span data-ttu-id="78bc5-107">Il suo report diretto è Patrick Hines.</span><span class="sxs-lookup"><span data-stu-id="78bc5-107">His direct report is Patrick Hines.</span></span>

<span data-ttu-id="78bc5-108">Come illustrato nell'esempio di codice seguente, Joe Andreani, l'amministratore dell'organizzazione, creerà un nuovo account per l'utente.</span><span class="sxs-lookup"><span data-stu-id="78bc5-108">As shown in the following code example, Joe Andreshak, the enterprise administrator, will create a new account for him.</span></span>


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



<span data-ttu-id="78bc5-109">Quando si crea un nuovo utente, è necessario specificare un **sAMAccountName**.</span><span class="sxs-lookup"><span data-stu-id="78bc5-109">When creating a new user, you must specify a **sAMAccountName**.</span></span> <span data-ttu-id="78bc5-110">Si tratta di un attributo obbligatorio per la classe utente.</span><span class="sxs-lookup"><span data-stu-id="78bc5-110">This is a mandatory attribute for the user class.</span></span> <span data-ttu-id="78bc5-111">Prima di poter creare un'istanza di un oggetto, è necessario impostare tutti gli attributi obbligatori.</span><span class="sxs-lookup"><span data-stu-id="78bc5-111">Before an instance of an object can be created, all mandatory attributes must be set.</span></span> <span data-ttu-id="78bc5-112">Il **sAMAccountName** verrà generato automaticamente se non ne viene specificato uno per un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="78bc5-112">The **sAMAccountName** will automatically be generated if one is not specified for a new user.</span></span>

<span data-ttu-id="78bc5-113">Quando si crea un nuovo utente, è necessario impostare tutti gli attributi necessari nella cache locale prima di chiamare il metodo [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="78bc5-113">When creating a new user, all of the required attributes must be set in the local cache before the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

<span data-ttu-id="78bc5-114">Joe, in qualità di amministratore, può assegnare la password di Terry usando il metodo [**IADsUser. sepassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="78bc5-114">Joe, as an administrator, can assign Terry's password using the [**IADsUser.SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="78bc5-115">Il metodo **IADsUser. sepassword** non funzionerà fino a quando non viene chiamato il metodo [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="78bc5-115">The **IADsUser.SetPassword** method will not work until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method has been called.</span></span>

<span data-ttu-id="78bc5-116">Joe Abilita quindi l'account utente impostando la proprietà [**IADsUser. accountdisabled**](iadsuser-property-methods.md) su **false**.</span><span class="sxs-lookup"><span data-stu-id="78bc5-116">Then, Joe enables the user account by setting the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property to **FALSE**.</span></span>

<span data-ttu-id="78bc5-117">Nell'esempio di codice seguente viene illustrato come impostare Terry come responsabile di Patrick.</span><span class="sxs-lookup"><span data-stu-id="78bc5-117">The following code example shows how to set Terry as Patrick's manager.</span></span>


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



<span data-ttu-id="78bc5-118">Ci si potrebbe chiedere cosa accade se Terry cambia il proprio nome, si sposta in un'altra organizzazione o lascia l'azienda.</span><span class="sxs-lookup"><span data-stu-id="78bc5-118">You may wonder what happens if Terry changes his name, moves to a different organization, or leaves the company.</span></span> <span data-ttu-id="78bc5-119">Chi gestisce il collegamento diretto al report?</span><span class="sxs-lookup"><span data-stu-id="78bc5-119">Who maintains this manager-direct report link?</span></span> <span data-ttu-id="78bc5-120">Per ulteriori informazioni e per risolvere il problema, vedere [riorganizzazione](reorganization.md).</span><span class="sxs-lookup"><span data-stu-id="78bc5-120">For more information, and the solution to this problem, see [Reorganization](reorganization.md).</span></span> <span data-ttu-id="78bc5-121">Poiché lo schema di Active Directory è estendibile, è possibile modellare gli oggetti in modo da includere relazioni di stile del rapporto dirette da gestione analoghe.</span><span class="sxs-lookup"><span data-stu-id="78bc5-121">Because the Active Directory schema is extensible, you can model your objects to include similar manager-direct report style relationships.</span></span>

<span data-ttu-id="78bc5-122">Prima di passare all'attività successiva, esaminare un esempio di codice che Mostra come Joe visualizzerà i dipendenti diretti di Terry.</span><span class="sxs-lookup"><span data-stu-id="78bc5-122">Before going on to the next task, look at a code example that shows how Joe would view Terry's direct reports.</span></span>


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



<span data-ttu-id="78bc5-123">In questo esempio di codice Patrick verrà visualizzato come report diretto di Terry, anche se l'attributo **DirectReports** non è mai stato modificato.</span><span class="sxs-lookup"><span data-stu-id="78bc5-123">In this code example, Patrick will display as Terry's direct report, even though the **directReports** attribute was never modified.</span></span> <span data-ttu-id="78bc5-124">Questa operazione viene eseguita automaticamente Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78bc5-124">Active Directory does this automatically.</span></span>

<span data-ttu-id="78bc5-125">Nel mondo della directory, un attributo può avere uno o più valori.</span><span class="sxs-lookup"><span data-stu-id="78bc5-125">In the directory world, an attribute can have single or multiple values.</span></span> <span data-ttu-id="78bc5-126">Poiché **DirectReports** ha più valori, è possibile ottenere queste informazioni esaminando lo schema, è più semplice usare il metodo [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) , che restituisce una matrice di valori, indipendentemente dal fatto che vengano restituiti valori singoli o multipli.</span><span class="sxs-lookup"><span data-stu-id="78bc5-126">Because **directReports** has multiple values, you can get this information by looking at the schema, it is easier to use the [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, which returns an array of values regardless of whether single or multiple values are returned.</span></span>

<span data-ttu-id="78bc5-127">Lo snap-in Active Directory utenti e computer consente di visualizzare i report diretti e le relazioni di gestione nella pagina delle proprietà dell'utente.</span><span class="sxs-lookup"><span data-stu-id="78bc5-127">The Active Directory Users and Computers snap-in lets you view direct reports and manager relationships on the user's property page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78bc5-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78bc5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78bc5-129">Aggiunta di utenti a un gruppo</span><span class="sxs-lookup"><span data-stu-id="78bc5-129">Adding Users to a Group</span></span>](adding-users-to-a-group.md)
</dt> </dl>

 

 




