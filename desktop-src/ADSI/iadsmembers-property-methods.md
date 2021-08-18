---
title: Metodi della proprietà IADsMembers (Iads.h)
description: I metodi dell'interfaccia IADsMembers leggono e scrivono le proprietà descritte in questo argomento. Per altre informazioni, vedere Metodi delle proprietà dell'interfaccia.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsMembers ADSI
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
ms.openlocfilehash: 384aa8a8f04afe8abbaa9627a0080b7a4ce219d4b58482d3eddc20bb33825c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023459"
---
# <a name="iadsmembers-property-methods"></a>Metodi della proprietà IADsMembers

I metodi [**dell'interfaccia IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) leggono e scrivono le proprietà descritte in questo argomento. Per altre informazioni, vedere [Metodi delle proprietà dell'interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Count**
</dt> <dd> <dl>

Indica il numero di elementi nel contenitore. Se il filtro è impostato, count restituisce solo il numero di elementi che rientrano nella descrizione del filtro.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati scripting: **LONG**
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

Indica il filtro. La sintassi delle voci nella matrice di filtri è la stessa del filtro usato [**nell'interfaccia IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer)

<dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Tipo di dati scripting: **VARIANT**
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

I provider di sistema ADSI non supportano il metodo della proprietà **IADsMembers::get \_ Count.**

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come usare i metodi delle proprietà di questa interfaccia.


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



Nell'esempio di codice seguente viene utilizzato il metodo **IADsMembers::p ut \_ Filter** per preparare un'enumerazione della raccolta di membri di un gruppo.


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
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IADsMembers IID è definito come \_ 451A0030-72EC-11CF-B03B-00AA006E0975<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**IADsMembers::get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[Metodi delle proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

 





