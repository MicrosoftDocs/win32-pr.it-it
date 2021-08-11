---
title: Metodi delle proprietà IADsOU (Iads.h)
description: I metodi di proprietà dell'interfaccia IADsOU ottengono o impostano le proprietà elencate nella tabella seguente. Per altre informazioni, vedere Metodi delle proprietà di interfaccia.
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsOU ADSI
topic_type:
- apiref
api_name:
- IADsOU Property Methods
- IADsOU.BusinessCategory
- IADsOU.get_BusinessCategory
- IADsOU.put_BusinessCategory
- IADsOU.Description
- IADsOU.get_Description
- IADsOU.put_Description
- IADsOU.FaxNumber
- IADsOU.get_FaxNumber
- IADsOU.put_FaxNumber
- IADsOU.LocalityName
- IADsOU.get_LocalityName
- IADsOU.put_LocalityName
- IADsOU.PostalAddress
- IADsOU.get_PostalAddress
- IADsOU.put_PostalAddress
- IADsOU.TelephoneNumber
- IADsOU.get_TelephoneNumber
- IADsOU.put_TelephoneNumber
- IADsOU.SeeAlso
- IADsOU.get_SeeAlso
- IADsOU.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019fb93575bc8b8b419797c7efdf41c15a6375172a834f48626befd3526b3b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179531"
---
# <a name="iadsou-property-methods"></a>Metodi delle proprietà IADsOU

I metodi di proprietà [**dell'interfaccia IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) ottengono o impostano le proprietà elencate nella tabella seguente. Per altre informazioni, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**BusinessCategory**
</dt> <dd> <dl>

Stringa che contiene la funzione o le funzioni aziendali generali eseguite dall'unità organizzativa, ad esempio "Accounting".

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BusinessCategory(
  [out] BSTR* pbstrBusinessCategory
);
HRESULT put_BusinessCategory(
  [in] BSTR bstrBusinessCategory
);
```


</dt> </dl> </dd> <dt>

**Descrizione**
</dt> <dd> <dl>

Stringa che contiene una descrizione testuale dell'unità organizzativa.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

**Numero fax**
</dt> <dd> <dl>

Stringa che contiene il numero facsimile dell'unità organizzativa.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] BSTR* pbstrFaxNumber
);
HRESULT put_FaxNumber(
  [in] BSTR bstrFaxNumber
);
```


</dt> </dl> </dd> <dt>

**LocalityName**
</dt> <dd> <dl>

Stringa che contiene il nome dell'area geografica dell'unità organizzativa.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

**PostalAddress**
</dt> <dd> <dl>

Stringa che contiene l'indirizzo postale dell'unità organizzativa.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

**SeeAlso**
</dt> <dd> <dl>

Matrice di stringhe che contiene i nomi distinti di altri oggetti directory che possono essere rilevanti per questo oggetto.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

**Numero di telefono**
</dt> <dd> <dl>

Stringa contenente il numero di telefono dell'unità organizzativa.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* pbstrTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente vengono visualizzate **le proprietà BusinessCategory** e **Description** di tutte le unità organizzative in un contenitore. Si presuppone che il servizio directory sottostante supporti il raggruppamento di oggetti directory per unità organizzativa.


```VB
Dim dom As IADsContainer
Dim ou As IADsOU

' Bind to the container.
Set dom = GetObject("LDAP://server1/domain1")

' Filter out all objects that are not of class "organizationalUnit".
dom.filter = Array("organizationalUnit")

' Enumerate the organizational units in the container and display  
' the BusinessCategory and Description properties of each OU.
For Each ou In dom
    MsgBox ou.BusinessCategory & ": " & ou.Description
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsOU è definito come A2F733B8-EFFE-11CF-8ABC-00C04FD8D503<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[Metodi delle proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

 





