---
title: Metodi della proprietà IADsGroup (Iads.h)
description: Metodi di proprietà dell'interfaccia IADsGroup.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsGroup ADSI
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
ms.openlocfilehash: f15a55765a10afef10087e7b28d04304ab0cc2668915a6e6ffa71fc770eb54a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082405"
---
# <a name="iadsgroup-property-methods"></a>Metodi della proprietà IADsGroup

I metodi di proprietà [**dell'interfaccia IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) leggono e scrivono le proprietà seguenti. Per altre informazioni, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**Descrizione**
</dt> <dd> <dl>

Indica la descrizione testuale dell'appartenenza al gruppo.

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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Uso di IADsGroup per recuperare le descrizioni dei gruppi predefiniti

Negli esempi seguenti viene illustrato come recuperare informazioni sui gruppi Windows oggetti in base al nome. In un ambiente multilingue, i gruppi predefiniti sono talvolta noti con nomi localizzati diversi, il che significa che non possono essere recuperati direttamente usando identificatori di stringa, ad esempio "WinNT://Microsoft/Administrators". In tal caso, l'utente può eseguire l'associazione all'oggetto SID noto per il gruppo, recuperare il nome del gruppo localizzato e fornire tale nome al metodo GetObject. Per altre informazioni, vedere [SID noti.](/windows/desktop/SecAuthZ/well-known-sids)

## <a name="examples"></a>Esempio

Nell'esempio Visual Basic seguente viene illustrato come eseguire l'associazione a un oggetto gruppo e visualizzare la descrizione del gruppo.


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



Nell'esempio C++ seguente viene illustrato come eseguire l'associazione a un oggetto gruppo e visualizzare la descrizione del gruppo.


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
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsGroup è definito come 27636B00-410F-11CF-B1FF-02608C9E7553<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAD**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Metodi delle proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

