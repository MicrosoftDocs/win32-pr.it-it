---
title: Metodi di proprietà IADsPropertyEntry (IADs. h)
description: Fornire l'accesso alle seguenti proprietà.
ms.assetid: 73b0f6d4-55db-46cf-a781-e10bc4fcf2db
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPropertyEntry ADSI
topic_type:
- apiref
api_name:
- IADsPropertyEntry Property Methods
- IADsPropertyEntry.Name
- IADsPropertyEntry.get_Name
- IADsPropertyEntry.put_Name
- IADsPropertyEntry.ADsType
- IADsPropertyEntry.get_ADsType
- IADsPropertyEntry.put_ADsType
- IADsPropertyEntry.ControlCode
- IADsPropertyEntry.get_ControlCode
- IADsPropertyEntry.put_ControlCode
- IADsPropertyEntry.Values
- IADsPropertyEntry.get_Values
- IADsPropertyEntry.put_Values
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e82344b2b659395bb14c0500fde3214530e000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874521"
---
# <a name="iadspropertyentry-property-methods"></a>Metodi di proprietà IADsPropertyEntry

I metodi di proprietà dell'interfaccia [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) forniscono accesso alle proprietà seguenti. Per ulteriori informazioni sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**ADsType**
</dt> <dd> <dl>

Tipo di dati della proprietà **Name** . I valori del tipo di dati sono definiti nell'enumerazione [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) .

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* plADsType
);
HRESULT put_ADsType(
  [in] LONG lADsType
);
```


</dt> </dl> </dd> <dt>

**ControlCode**
</dt> <dd> <dl>

Costante che specifica l'operazione da eseguire sulla proprietà denominata. Il valore viene definito nell'enumerazione [**\_ enum dell' \_ operazione \_ della proprietà ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ControlCode(
  [out] LONG* pControlCode
);
HRESULT put_ControlCode(
  [in] LONG lnControlCode
);
```


</dt> </dl> </dd> <dt>

**Nome**
</dt> <dd> <dl>

Nome della voce della proprietà. Questo nome deve corrispondere al nome di un attributo, come definito nello schema.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
HRESULT put_Name(
  [in] BSTR bstrName
);
```


</dt> </dl> </dd> <dt>

**Valori**
</dt> <dd> <dl>

Matrice **Variant** . Ogni elemento in questa matrice rappresenta un valore della proprietà denominata. Tali valori di proprietà sono rappresentati da oggetti ADSI che implementano le interfacce [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) e [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) . Pertanto, la matrice **Variant** include una matrice di puntatori all'interfaccia [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sugli oggetti ADSI che implementano le interfacce **IADsPropertyValue** e **IADsPropertyValue2** .

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Values(
  [out] VARIANT* pvValues
);
HRESULT put_Values(
  [in] VARIANT vValues
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

Ogni metodo di proprietà supporta i valori restituiti **HRESULT** standard, incluso S \_ OK. Per ulteriori informazioni sugli altri valori restituiti, vedere [codici di errore ADSI](adsi-error-codes.md).

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come recuperare una proprietà denominata dalla cache e come creare una nuova voce di proprietà.


```VB
 
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup

'------------------------------------------------------------
'----- Getting IADsPropertyEntry ----------------------------
'------------------------------------------------------------
 
' Create the property list object.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a named property entry object.
Set propEntry = propList.GetPropertyItem("dc", ADSTYPE_CASE_IGNORE_STRING)

' Insert code to do something with propEntry
Set propEntry = Nothing
 
'------------------------------------------------------------
'---- Setting IADsPropertyEntry -----------------------------
'------------------------------------------------------------
 
' Create a property value object.
Set propVal = New PropertyValue
 
'---- Property Value -----
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'---- Create a new Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' ---- Put the newly created property entry to the cache ----
propList.PutPropertyItem (propEntry)
 
' Commit the entry to the directory store.
propList.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



Nell'esempio di codice seguente viene illustrato come ottenere una proprietà denominata da una cache.


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADs *pObj = NULL;
VARIANT var;
long valType = ADSTYPE_CASE_IGNORE_STRING;
 
VariantInit(&var);
 
// Bind to directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);
if(FAILED(hr)){return;}
 
// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
pObj->GetInfo();
pObj->Release();
 
// Get a property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), valType, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}
hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Get the name and the type of the property entry.
BSTR nm = NULL;
hr = pEntry->get_Name(&nm);
printf("Property name = %S\n",nm);
VariantClear(&var);
long at;
hr = pEntry->get_ADsType(&at);
printf("Property type = %d\n",a);

Cleanup:
    if(nm)
        SysFreeString(nm);

    if(pList)
        pList->Release();

    if(pEntry)
        pEntry->Release();

    if(pObj)
        pObj->Release();

    VariantClear(&var);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPropertyEntry è definito come 05792C8E-941F-11D0-8529-00C04FD8D503<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ enum operazione proprietà \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)
</dt> <dt>

[Codici di errore ADSI](adsi-error-codes.md)
</dt> <dt>

[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

