---
title: Modifica degli attributi con l'interfaccia IDirectoryObject
description: Oltre a IADs put e IADs PutEx, è possibile usare il metodo IDirectoryObject SetObjectAttributes per modificare i valori degli attributi. Per usare questo metodo, è necessario compilare una struttura di \_ info attr Ads \_ per ogni attributo da modificare.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Modifica degli attributi con l'interfaccia IDirectoryObject ADSI
- IDirectoryObject ADSI, utilizzo di per modificare gli attributi
- ADSI ADSI, esempio di codice C/C++, uso di IDirectoryObject per modificare gli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715826d0fc835f3d9ecae914fcc51603883af5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116680"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>Modifica degli attributi con l'interfaccia IDirectoryObject

Oltre a [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex), è possibile usare il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) per modificare i valori degli attributi. Per usare questo metodo, è necessario compilare una struttura [**di \_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) per ogni attributo da modificare.

Il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) consente di modificare gli attributi a valore singolo e multivalore. Questa funzione fornisce controlli operativi simili, ad esempio Clear, Append, DELETE e Update, a quelli disponibili nel metodo [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Le costanti di controllo includono:

-   [**Clear degli annunci \_ attr \_**](adsi-attribute-modification-types.md)
-   [**\_aggiornamento attr \_ ADS**](adsi-attribute-modification-types.md)
-   [**\_accodamento degli annunci attr \_**](adsi-attribute-modification-types.md)
-   [**eliminazione degli annunci \_ attr \_**](adsi-attribute-modification-types.md)

Se si specifica ADS, l' [**\_ \_ aggiornamento attr**](adsi-attribute-modification-types.md) attiverà un'operazione lato server che può richiedere un utilizzo intensivo delle risorse. Un esempio è costituito dall'avvio dell'operazione di aggiornamento di un lungo elenco di appartenenza al gruppo. In generale, evitare di usare questa operazione, a meno che la modifica non includa un numero ridotto di attributi nella directory. Per modificare un lungo elenco di appartenenze a gruppi, l'approccio più efficiente consiste nel leggere l'elenco dalla directory sottostante, apportare modifiche e archiviare nuovamente l'elenco aggiornato nella directory.

> [!Note]  
> Analogamente a [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex) con [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), le modifiche degli attributi vengono completamente sottoposte a commit o scartate in Active Directory. Se una o più delle modifiche non sono consentite e pertanto non è possibile eseguirle, nessuna delle modifiche collettive apportate agli attributi viene sottoposta a commit nella directory.

 

## <a name="example"></a>Esempio

Nell'esempio di codice seguente viene illustrato come modificare gli attributi singoli e multivalore con il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .


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



 

 




