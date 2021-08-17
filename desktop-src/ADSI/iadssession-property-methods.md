---
title: Metodi della proprietà IADsSession (Iads.h)
description: I metodi di proprietà dell'interfaccia IADsSession ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni e una discussione generale sui metodi di proprietà, vedere Metodi delle proprietà di interfaccia.
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsSession ADSI
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227c855be1704754be6e2b610f492eff26c8ceb966e3294c6672a8fbeb6dac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690736"
---
# <a name="iadssession-property-methods"></a>Metodi della proprietà IADsSession

I metodi di proprietà [**dell'interfaccia IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni e una discussione generale sui metodi di proprietà, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**Computer**
</dt> <dd> <dl>

Nome della workstation client.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

**Percorso computer**
</dt> <dd> <dl>

ADsPath dell'oggetto computer per la workstation client.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

**ConnectTime**
</dt> <dd> <dl>

Tempo trascorso, in secondi, dall'avvio della sessione.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

**IdleTime**
</dt> <dd> <dl>

Tempo di inattività, in secondi, della sessione.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

**Utente**
</dt> <dd> <dl>

Nome dell'utente della sessione.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

**UserPath**
</dt> <dd> <dl>

ADsPath dell'oggetto utente per l'utente di questa sessione.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come esaminare le sessioni per un servizio file.


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



Nell'esempio di codice seguente viene enumerata una raccolta di sessioni.


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsSession è definito come 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsFileServiceOperations::Sessions**](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 





