---
title: Modifica degli attributi con l'interfaccia IDirectoryObject
description: Oltre agli IAD Put e IADs PutEx, è possibile usare il metodo IDirectoryObject SetObjectAttributes per modificare i valori degli attributi. Per usare questo metodo, è necessario compilare una struttura ADS \_ ATTR \_ INFO per ogni attributo da modificare.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Modifica degli attributi con l'interfaccia ADSI IDirectoryObject
- IDirectoryObject ADSI , Uso di per modificare attributi
- ADSI ADSI, codice di esempio C/C++, uso di IDirectoryObject per modificare gli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fa7d75d3e0dce489f676dafb36992c95a1cba2e9856bbbaf49f14806a6c1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179029"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>Modifica degli attributi con l'interfaccia IDirectoryObject

Oltre a [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P utEx,**](/windows/desktop/api/Iads/nf-iads-iads-putex)è possibile usare il metodo [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) per modificare i valori degli attributi. Per usare questo metodo, è necessario compilare una [**struttura ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) per ogni attributo da modificare.

Il [**metodo IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) consente di modificare gli attributi a valore singolo e multivalore. Questa funzione fornisce controlli operativi simili, ad esempio clear, append, delete e update, a quelli trovati nel metodo [**IADs::P utEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex) Le costanti di controllo includono:

-   [**ADS \_ ATTR \_ CLEAR**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ UPDATE**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ APPEND**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ DELETE**](adsi-attribute-modification-types.md)

Specificando [**ADS \_ ATTR \_ UPDATE**](adsi-attribute-modification-types.md) verrà attivata un'operazione lato server che può essere a elevato utilizzo di risorse. Ad esempio, avviare l'operazione per aggiornare un lungo elenco di appartenenze a gruppi. In generale, evitare di usare questa operazione a meno che la modifica non implica un numero ridotto di attributi nella directory. Per modificare un lungo elenco di appartenenze a gruppi, l'approccio più efficiente consiste nel leggere l'elenco dalla directory sottostante, apportare modifiche e archiviare nuovamente l'elenco aggiornato nella directory.

> [!Note]  
> Analogamente a [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P utEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) con [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), viene eseguito il commit completo o l'eliminazione delle modifiche degli attributi in Active Directory. Se una o più modifiche non sono consentite e pertanto non possono essere eseguite, nessuna delle modifiche collettive apportate agli attributi viene eseguita nella directory.

 

## <a name="example"></a>Esempio

L'esempio di codice seguente illustra come modificare attributi singoli e multivalore con il [**metodo IDirectoryObject::SetObjectAttributes.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)


```C++
HRESULT hr;
LPCWSTR pwszADsPath = L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com";
IDirectoryObject *pDirObject = NULL;

// Bind to the object.
hr = ADsGetObject(pwszADsPath, IID_IDirectoryObject, (void**)&pDirObject);
if(SUCCEEDED(hr))
{ 
    ADSVALUE adsvFaxNumber;
    ADSVALUE rgadsvOtherTelephones[2];
     
    // Set the new FAX number.
    adsvFaxNumber.dwType = ADSTYPE_CASE_IGNORE_STRING; 
    adsvFaxNumber.CaseIgnoreString = L"425-707-9790";

    // Set the first telephone number.
    rgadsvOtherTelephones[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[0].CaseIgnoreString = L"425-707-9791";

    // Set the second telephone number.
    rgadsvOtherTelephones[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[1].CaseIgnoreString = L"425-707-9792";

    ADS_ATTR_INFO attrInfo[2];

    // Setup the facsimileTelephoneNumber attribute data.
    attrInfo[0].pszAttrName = L"facsimileTelephoneNumber";
    attrInfo[0].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[0].dwADsType = adsvFaxNumber.dwType;
    attrInfo[0].pADsValues = &adsvFaxNumber;
    attrInfo[0].dwNumValues = 1;

    // Setup the otherTelephone attribute data.
    attrInfo[1].pszAttrName = L"otherTelephone";
    attrInfo[1].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[1].dwADsType = rgadsvOtherTelephones[0].dwType;
    attrInfo[1].pADsValues = rgadsvOtherTelephones;
    attrInfo[1].dwNumValues = sizeof(rgadsvOtherTelephones)/sizeof(ADSVALUE);

    DWORD dwReturn;
 
    // Set the new attribute values.
    hr = pDirObject->SetObjectAttributes(attrInfo, 
        sizeof(attrInfo)/sizeof(ADS_ATTR_INFO), 
        &dwReturn);

    pDirObject->Release();
}
```



 

 




