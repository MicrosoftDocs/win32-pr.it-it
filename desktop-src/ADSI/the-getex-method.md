---
title: Metodo GetEx
description: Alcuni attributi possono archiviare uno o più valori.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI, uso di IADs GetEx
- ADSI ADSI, utilizzo di, utilizzo del metodo IADs GetEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297643"
---
# <a name="the-getex-method"></a><span data-ttu-id="3956b-105">Metodo GetEx</span><span class="sxs-lookup"><span data-stu-id="3956b-105">The GetEx Method</span></span>

<span data-ttu-id="3956b-106">Alcuni attributi possono archiviare uno o più valori.</span><span class="sxs-lookup"><span data-stu-id="3956b-106">Some attributes can store one or more values.</span></span> <span data-ttu-id="3956b-107">Ad esempio, l'attributo **OtherTelephone** di un oggetto utente in Active Directory è una proprietà che può avere zero, uno o più valori.</span><span class="sxs-lookup"><span data-stu-id="3956b-107">For example, the **otherTelephone** attribute of a user object in Active Directory is a property that can have zero, one, or many values.</span></span> <span data-ttu-id="3956b-108">Gli attributi con più valori sono noti come "attributi multivalore".</span><span class="sxs-lookup"><span data-stu-id="3956b-108">Attributes that have multiple values are known as "multi-valued attributes".</span></span> <span data-ttu-id="3956b-109">Se il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) viene utilizzato per recuperare un attributo multivalore, i risultati devono essere elaborati in modo diverso rispetto a se l'attributo ha un singolo valore.</span><span class="sxs-lookup"><span data-stu-id="3956b-109">If the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve a multi-valued attribute, the results must be processed differently than if the attribute has a single value.</span></span> <span data-ttu-id="3956b-110">I risultati forniti dal metodo [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) , tuttavia, vengono elaborati nello stesso modo, indipendentemente dal fatto che l'attributo abbia un solo valore o più valori.</span><span class="sxs-lookup"><span data-stu-id="3956b-110">The results provided by the [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, however, are processed in the same manner, regardless if the attribute has a single or multiple values.</span></span> <span data-ttu-id="3956b-111">In entrambi i casi, il metodo **IADs:: GetEx** restituisce i valori in una matrice.</span><span class="sxs-lookup"><span data-stu-id="3956b-111">In both cases, the **IADs::GetEx** method returns the values in an array.</span></span>

<span data-ttu-id="3956b-112">Il metodo [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) recupera le proprietà dalla cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="3956b-112">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method retrieves properties from the property cache.</span></span> <span data-ttu-id="3956b-113">Se la proprietà specificata non viene trovata nella cache, **IADs:: GetEx** esegue una chiamata implicita a [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="3956b-113">If the specified property is not found in the cache, **IADs::GetEx** performs an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span>

<span data-ttu-id="3956b-114">Il metodo [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) restituisce una matrice di varianti Variant indipendentemente dal numero di valori restituiti dal server.</span><span class="sxs-lookup"><span data-stu-id="3956b-114">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method returns a variant array of variants regardless of the number of values returned from the server.</span></span> <span data-ttu-id="3956b-115">Questo vale anche se l'attributo contiene solo un valore.</span><span class="sxs-lookup"><span data-stu-id="3956b-115">This is true even if the attribute only contains one value.</span></span>


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="3956b-116">Il metodo [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) può essere usato anche per gli attributi a valore singolo.</span><span class="sxs-lookup"><span data-stu-id="3956b-116">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method can also be used for single-valued attributes.</span></span> <span data-ttu-id="3956b-117">I risultati di un attributo a valore singolo vengono elaborati come i risultati di un attributo multivalore.</span><span class="sxs-lookup"><span data-stu-id="3956b-117">The results of a single-valued attribute are processed the same as the results for a multi-valued attribute.</span></span>


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="3956b-118">Se non è impostato alcun valore per l'attributo, [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) restituisce l'errore "proprietà non trovata nella cache".</span><span class="sxs-lookup"><span data-stu-id="3956b-118">If no value is set for the attribute, [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) returns the error "Property not found in cache".</span></span>

 

 




