---
title: Metodi della proprietà IADsServiceOperations (Iads.h)
description: I metodi di proprietà dell'interfaccia IADsServiceOperations leggono e scrivono le proprietà descritte nell'elenco seguente. Per altre informazioni sui metodi di proprietà, vedere Metodi delle proprietà di interfaccia.
ms.assetid: ebddfc42-1d2f-495b-b57c-f57419b54ff8
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsServiceOperations ADSI
topic_type:
- apiref
api_name:
- IADsServiceOperations Property Methods
- IADsServiceOperations.Status
- IADsServiceOperations.get_Status
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f60b8fe1280e257ccd33f505b2b696a0d1a16228ebfaf8b0cabf7f1319964a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427607"
---
# <a name="iadsserviceoperations-property-methods"></a>Metodi della proprietà IADsServiceOperations

I metodi di proprietà [**dell'interfaccia IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) leggono e scrivono le proprietà descritte nell'elenco seguente. Per altre informazioni sui metodi di proprietà, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**Status**
</dt> <dd> <dl>

Stato del servizio.

Di seguito sono riportati i valori possibili.

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

**Servizi di dominio Active Directory \_ SERVICE \_ STOPPED** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

**Servizi di dominio Active Directory \_ AVVIO \_ SERVIZIO \_ IN SOSPESO** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

**Servizi di dominio Active Directory \_ SERVICE \_ STOP \_ PENDING** (0x00000003)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

**Servizi di dominio Active Directory \_ SERVIZIO \_ IN** ESECUZIONE (0x00000004)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

**Servizi di dominio Active Directory \_ SERVICE \_ CONTINUE \_ PENDING** (0X00000005)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

**Servizi di dominio Active Directory \_ SERVICE \_ PAUSE \_ PENDING** (0x00000006)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

**Servizi di dominio Active Directory \_ SERVICE \_ PAUSED** (0x00000007)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

**Servizi di dominio Active Directory \_ ERRORE \_ DEL SERVIZIO** (0x00000008)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

**Servizi di dominio Active Directory \_ PROCESSO \_ \_ PERSONALIZZATO DEL** SERVIZIO (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

**Servizi di dominio Active Directory \_ PROCESSO \_ DI \_ CONDIVISIONE DEL** SERVIZIO (0x00000020)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

**Servizi di dominio Active Directory \_ DRIVER \_ DEL \_ KERNEL DEL** SERVIZIO (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

**Servizi di dominio Active Directory \_ DRIVER \_ DEL FILE \_ SYSTEM \_** DEL SERVIZIO (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

**Servizi di dominio Active Directory \_ AVVIO \_ DEL \_ SERVIZIO** (AVVIO DEL \_ \_ SERVIZIO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

**Servizi di dominio Active Directory \_ AVVIO \_ DEL SISTEMA DEL \_ SERVIZIO** (AVVIO \_ DEL SISTEMA DEL \_ SERVIZIO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

**Servizi di dominio Active Directory \_ AVVIO \_ AUTOMATICO \_ DEL SERVIZIO** (AVVIO AUTOMATICO DEL \_ \_ SERVIZIO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

**Servizi di dominio Active Directory \_ AVVIO \_ DELLA RICHIESTA DI \_ SERVIZIO** (AVVIO \_ DELLA RICHIESTA DI \_ SERVIZIO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

**Servizi di dominio Active Directory \_ SERVIZIO \_ DISABILITATO** (SERVIZIO \_ DISABILITATO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

**Servizi di dominio Active Directory \_ SERVICE \_ ERROR \_ IGNORE** (0)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

**Servizi di dominio Active Directory \_ ERRORE \_ DI \_ SERVIZIO NORMALE** (1)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

**Servizi di dominio Active Directory \_ ERRORE \_ DEL \_ SERVIZIO GRAVE** (2)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

**Servizi di dominio Active Directory \_ ERRORE \_ DEL \_ SERVIZIO CRITICO** (3)


</dt> <dd></dd> </dl> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come verificare lo stato di un servizio Microsoft Fax in esecuzione Windows 2000.


```VB
Dim cp As IADsComputer
Dim sr As IADsService
Dim so As IADsServiceOperations
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set sr = cp.GetObject("Service", "Fax")
Set so = sr

Select Case so.Status
    Case ADS_SERVICE_STOPPED
        MsgBox "Microsoft Fax Service has stopped."
    Case ADS_SERVICE_RUNNING
        MsgBox "Microsoft Fax Service is running."
    Case ADS_SERVICE_PAUSED
        MsgBox "Microsoft Fax Service has paused."
    Case ADS_SERVICE_ERROR
        MsgBox "Microsoft Fax Service has errors."
End Select

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
    Set sr = Nothing
    Set so = Nothing
```



Nell'esempio di codice seguente viene verificato lo stato di un servizio Microsoft Fax in esecuzione Windows 2000.


```C++
IADsContainer *pCont = NULL;
IADsServiceOperations *pSrvOp = NULL;
LPWSTR adsPath = L"WinNT://myMachine,computer";
IDispatch *pDisp = NULL;
long status = 0;

HRESULT hr = S_OK;

hr = ADsGetObject(adsPath,IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->GetObject(CComBSTR("Service"), CComBSTR("Fax"), &pDisp);
if(FAILED(hr)) {goto Cleanup;}

hr = pDisp->QueryInterface(IID_IADsServiceOperations,(void**)&pSrvOp);
if(FAILED(hr)) {goto Cleanup;}

hr = pSrvOp->get_Status(&status);
switch (status) 
{
    case ADS_SERVICE_STOPPED:
        printf("The service has stopped.\n");
        break;
    case ADS_SERVICE_RUNNING:
        printf("The service is running.\n");
        break;
    case ADS_SERVICE_PAUSED:
        printf("The service has paused.\n");
        break;
    case ADS_SERVICE_ERROR:
        printf("The service has errors.\n");
        break;
}

Cleanup:
    if(pDisp) pDisp->Release();
    if(pCont) pCont->Release();
    if(pSrvOp) pSrvOp->Release();
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IADsServiceOperations è definito come 5D7B33F0-31CA-11CF-A98A-00AA006BC149<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





