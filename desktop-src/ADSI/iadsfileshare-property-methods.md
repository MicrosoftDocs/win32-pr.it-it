---
title: Metodi della proprietà IADsFileShare (Iads.h)
description: I metodi di proprietà dell'interfaccia IADsFileshare ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi delle proprietà di interfaccia.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsFileShare ADSI
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6daec9905990d0f5cc5826b82b5361e0fc0653fafb0c617633a34b87c7a0e995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691419"
---
# <a name="iadsfileshare-property-methods"></a>Metodi della proprietà IADsFileShare

I metodi di proprietà [**dell'interfaccia IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**CurrentUserCount**
</dt> <dd> <dl>

Numero di utenti connessi alla condivisione.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

**Descrizione**
</dt> <dd> <dl>

Descrizione della condivisione file.

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

**Computer host**
</dt> <dd> <dl>

Riferimento ADsPath al computer host.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

**MaxUserCount**
</dt> <dd> <dl>

Numero massimo di utenti autorizzati ad accedere alla condivisione contemporaneamente.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

**Percorso**
</dt> <dd> <dl>

Percorso file system percorso della directory condivisa.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Esempio

Per accedere alle proprietà delle condivisioni file in un computer, è prima necessario eseguire il binding a "LanmanServer" nel computer. Nell'esempio di codice seguente viene illustrato come configurare la descrizione e il numero massimo di utenti consentiti per tutte le condivisioni file pubbliche nel computer, denominato "myMachine", nel dominio predefinito.


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



Nell'esempio di codice seguente viene illustrato come impostare la directory C: \\ MyFolder esistente come condivisione file pubblica.


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



L'esempio di codice seguente rende la directory C: \\ MyFolder esistente una condivisione file pubblica.


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsFileShare è definito come EB6DCAF0-4B83-11CF-A995-00AA006BC149<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**IADsFileShare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[Metodi delle proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

 





