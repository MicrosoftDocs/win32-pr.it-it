---
title: Metodi di proprietà IADsO (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsO ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: d4bc1d29-98de-462d-b59c-2bc2641c25a0
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsO ADSI
topic_type:
- apiref
api_name:
- IADsO Property Methods
- IADsO.Description
- IADsO.get_Description
- IADsO.put_Description
- IADsO.FaxNumber
- IADsO.get_FaxNumber
- IADsO.put_FaxNumber
- IADsO.LocalityName
- IADsO.get_LocalityName
- IADsO.put_LocalityName
- IADsO.PostalAddress
- IADsO.get_PostalAddress
- IADsO.put_PostalAddress
- IADsO.TelephoneNumber
- IADsO.get_TelephoneNumber
- IADsO.put_TelephoneNumber
- IADsO.SeeAlso
- IADsO.get_SeeAlso
- IADsO.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09840cf62d6883eb4f5ca326998b697a34698c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742687"
---
# <a name="iadso-property-methods"></a>Metodi di proprietà IADsO

I metodi di proprietà dell'interfaccia [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Descrizione**
</dt> <dd> <dl>

Descrizione dell'organizzazione.

<dt>

Tipo di accesso: lettura/scrittura
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

**NumeroFax**
</dt> <dd> <dl>

Il numero di fax dell'organizzazione.

<dt>

Tipo di accesso: lettura/scrittura
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

Nome della posizione in cui si trova l'organizzazione.

<dt>

Tipo di accesso: lettura/scrittura
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

Indirizzo postale dell'organizzazione.

<dt>

Tipo di accesso: lettura/scrittura
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

Matrice di nomi di ADsPath di altri oggetti ADSI che possono essere rilevanti per questo oggetto.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
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

**TelephoneNumber**
</dt> <dd> <dl>

Il numero di telefono dell'organizzazione.

<dt>

Tipo di accesso: lettura/scrittura
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

Nell'esempio di codice seguente viene visualizzata la descrizione di una determinata organizzazione. Si presuppone che il servizio directory sottostante supporti il raggruppamento di oggetti directory in base all'organizzazione.


```VB
Dim dom As IADsContainer
Dim dso As IADsOpenDSObject
Dim szUsername As String
Dim szPassword As String
On Error GoTo Cleanup

' Insert code to securely retrieve the user name and password
 
Set dso = GetObject("LDAP:")
Set dom = dso.OpenDSObject("LDAP://adsrv1/dc=Fabrikam, dc=Com", _
                           szUsername, szPassword,1)
dom.Filter = Array("organization")
For Each o In dom
    MsgBox "Fax number of " & o.Name & " : " & o.Description
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set dom = Nothing
    Set dso = Nothing
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsO è definito come A1CD2DC6-Effe-11CF-8ABC-00C04FD8D503<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)
</dt> <dt>

[Metodi di proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

 





