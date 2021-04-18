---
title: Metodi di proprietà IADsGroup (IADs. h)
description: Metodi di proprietà dell'interfaccia IADsGroup.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsGroup ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302142"
---
# <a name="iadsgroup-property-methods"></a>Metodi di proprietà IADsGroup

I metodi di proprietà dell'interfaccia [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) leggono e scrivono le proprietà seguenti. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Descrizione**
</dt> <dd> <dl>

Indica la descrizione testuale dell'appartenenza al gruppo.

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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Uso di IADsGroup per recuperare le descrizioni dei gruppi predefiniti

Negli esempi seguenti viene illustrato come recuperare informazioni sugli oggetti gruppo di Windows in base al nome. In un ambiente multilingue, i gruppi predefiniti sono a volte noti da nomi localizzati diversi, il che significa che non possono essere recuperati direttamente usando identificatori di stringa, ad esempio "WinNT://Microsoft/Administrators". In tal caso, l'utente può eseguire l'associazione all'oggetto SID noto per il gruppo, recuperare il nome del gruppo localizzato e fornire tale nome al metodo GetObject. Per ulteriori informazioni, vedere [SID noti](/windows/desktop/SecAuthZ/well-known-sids).

## <a name="examples"></a>Esempio

Nell'esempio di Visual Basic seguente viene illustrato come eseguire l'associazione a un oggetto gruppo e visualizzare la descrizione del gruppo.


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



Nell'esempio C++ riportato di seguito viene illustrato come eseguire l'associazione a un oggetto gruppo e visualizzare la descrizione del gruppo.


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsGroup è definito come 27636B00-410f-11CF-B1FF-02608C9E7553<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Metodi di proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

