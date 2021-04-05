---
title: Aggiunta di una classe ausiliaria a un'istanza di oggetto
description: Negli esempi di codice seguenti viene illustrato come utilizzare ADSI e LDAP per aggiungere dinamicamente una classe ausiliaria a un'istanza di oggetto esistente.
ms.assetid: 739dd372-3bda-4d94-8daf-f71e3091cfb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6b1f61bffe9081350949cccddc70fee83a568
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046564"
---
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a><span data-ttu-id="ff051-103">Aggiunta di una classe ausiliaria a un'istanza di oggetto</span><span class="sxs-lookup"><span data-stu-id="ff051-103">Adding an Auxiliary Class to an Object Instance</span></span>

<span data-ttu-id="ff051-104">Negli esempi di codice seguenti viene illustrato come utilizzare ADSI e LDAP per aggiungere dinamicamente una classe ausiliaria a un'istanza di oggetto esistente.</span><span class="sxs-lookup"><span data-stu-id="ff051-104">The following code examples show how to use ADSI and LDAP to dynamically add an auxiliary class to an existing object instance.</span></span> <span data-ttu-id="ff051-105">Gli esempi presuppongono che una classe ausiliaria denominata **Vehicle** sia definita nello schema Active Directory e che la classe **Vehicle** disponga di un attributo **Vin** .</span><span class="sxs-lookup"><span data-stu-id="ff051-105">The examples assume that an auxiliary class named **vehicle** is defined in the Active Directory schema, and that the **vehicle** class has a **vin** attribute.</span></span>

<span data-ttu-id="ff051-106">Quando si aggiunge dinamicamente una classe ausiliaria a un'istanza dell'oggetto, è necessario specificare contemporaneamente i valori per tutti gli attributi **musthave** obbligatori nella classe.</span><span class="sxs-lookup"><span data-stu-id="ff051-106">When you dynamically add an auxiliary class to an object instance, you must simultaneously specify values for any mandatory **mustHave** attributes in the class.</span></span> <span data-ttu-id="ff051-107">Negli esempi seguenti viene illustrato come eseguire questa operazione con l'attributo "Vin", che si presuppone sia obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ff051-107">The following examples show how to do this with the "vin" attribute, which is assumed to be mandatory.</span></span>

<span data-ttu-id="ff051-108">Nell'esempio C++ riportato di seguito viene associato a un oggetto e viene utilizzato [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) per aggiungere la classe ausiliaria all'elenco di classi nella proprietà **objectClass** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ff051-108">The following C++ example binds to an object, and uses [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) to append the auxiliary class to the list of classes in the object's **objectClass** property.</span></span> <span data-ttu-id="ff051-109">Nell'esempio viene usato [**IADs. Put**](/windows/desktop/api/iads/nf-iads-iads-put) per impostare il valore dell'attributo **Vin** .</span><span class="sxs-lookup"><span data-stu-id="ff051-109">Then the example uses [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put) to set the value of the **vin** attribute.</span></span> <span data-ttu-id="ff051-110">Infine, chiama [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit delle modifiche nella directory.</span><span class="sxs-lookup"><span data-stu-id="ff051-110">Finally, it calls [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>


```C++
LPWSTR pszAuxClass[]={L"vehicle"};
LPWSTR pszVIN[]={L"df897dsfsa-0"};
VARIANT var;

VariantInit(&var);

ADsOpenObject(L"cn=johnd,cn=users,dc=fabrikam,dc=com", 
    NULL, 
    NULL, 
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,  
    (VOID**)&pIADs);

ADsBuildVarArrayStr(pszAuxClass, 1, &var);
pIADs->PutEx(ADS_PROPERTY_APPEND, CComBSTR("objectClass"), var);
ADsBuildVarArrayStr( pszVIN, 1, &var);
pIADs->Put(CComBSTR("vin"), var);
pIADs->SetInfo();

if(pIADs)
    pIADs->Release();

VariantClear(&var);
```



 

 