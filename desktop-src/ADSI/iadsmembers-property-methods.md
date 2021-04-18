---
title: Metodi di proprietà IADsMembers (IADs. h)
description: I metodi dell'interfaccia IADsMembers leggono e scrivono le proprietà descritte in questo argomento. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsMembers ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302140"
---
# <a name="iadsmembers-property-methods"></a>Metodi di proprietà IADsMembers

I metodi dell'interfaccia [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) leggono e scrivono le proprietà descritte in questo argomento. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Count**
</dt> <dd> <dl>

Indica il numero di elementi nel contenitore. Se il filtro è impostato, Count restituisce solo il numero di elementi che soddisfano la descrizione del filtro.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

Indica il filtro. La sintassi delle voci nella matrice di filtri è identica a quella del filtro usato nell'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

I provider di sistema ADSI non supportano il metodo della proprietà **IADsMembers:: Get \_ count** .

## <a name="examples"></a>Esempio

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare i metodi di proprietà di questa interfaccia.


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



Nell'esempio di codice seguente viene usato il metodo **IADsMembers::p UT \_ Filter** per preparare un'enumerazione della raccolta di membri di un gruppo.


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsMembers è definito come 451A0030-72EC-11CF-B03B-00AA006E0975<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**IADsMembers:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[Metodi di proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

 





