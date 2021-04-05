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
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a>Aggiunta di una classe ausiliaria a un'istanza di oggetto

Negli esempi di codice seguenti viene illustrato come utilizzare ADSI e LDAP per aggiungere dinamicamente una classe ausiliaria a un'istanza di oggetto esistente. Gli esempi presuppongono che una classe ausiliaria denominata **Vehicle** sia definita nello schema Active Directory e che la classe **Vehicle** disponga di un attributo **Vin** .

Quando si aggiunge dinamicamente una classe ausiliaria a un'istanza dell'oggetto, è necessario specificare contemporaneamente i valori per tutti gli attributi **musthave** obbligatori nella classe. Negli esempi seguenti viene illustrato come eseguire questa operazione con l'attributo "Vin", che si presuppone sia obbligatorio.

Nell'esempio C++ riportato di seguito viene associato a un oggetto e viene utilizzato [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) per aggiungere la classe ausiliaria all'elenco di classi nella proprietà **objectClass** dell'oggetto. Nell'esempio viene usato [**IADs. Put**](/windows/desktop/api/iads/nf-iads-iads-put) per impostare il valore dell'attributo **Vin** . Infine, chiama [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit delle modifiche nella directory.


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



 

 