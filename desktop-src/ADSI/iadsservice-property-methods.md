---
title: Metodi di proprietà IADsService (IADs. h)
description: Leggere e scrivere le proprietà descritte in questo argomento.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsService ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301478"
---
# <a name="iadsservice-property-methods"></a>Metodi di proprietà IADsService

I metodi di proprietà dell'interfaccia [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) leggono e scrivono le proprietà descritte in questo argomento. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Dipendenze**
</dt> <dd> <dl>

Matrice di nomi **BSTR** dei servizi o dei gruppi di carico che devono essere caricati per il caricamento del servizio. La sintassi per la voce è "Service:" seguita dal nome del servizio o "Group:" seguito dal nome del gruppo di caricamento.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

**DisplayName**
</dt> <dd> <dl>

Nome descrittivo del servizio.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

**ErrorControl**
</dt> <dd> <dl>

Azione da eseguire se il servizio non riesce all'avvio. Di seguito sono riportati i valori validi per questa proprietà.

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\_errore del servizio ADS \_ \_ Ignora * * * *


</dt> <dd>

Il programma di avvio registra l'errore, ma continua l'operazione di avvio.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>errore del servizio ADS- \_ \_ \_ normale * * * *


</dt> <dd>

Il programma di avvio registra l'errore e visualizza una finestra di messaggio, ma continua l'operazione di avvio.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_errore grave del servizio ADS \_ \_ * * * *


</dt> <dd>

Il programma di avvio registra l'errore. Se viene avviata la configurazione Last-know-valido, l'operazione di avvio continua. In caso contrario, il sistema viene riavviato con l'ultima configurazione ben nota.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_errore critico del servizio ADS \_ \_ * * * *


</dt> <dd>

Il programma di avvio registra l'errore, se possibile. Se è in corso l'avvio della configurazione Last-know-valido, l'operazione di avvio non riesce. In caso contrario, il sistema viene riavviato con l'ultima configurazione corretta.

</dd> </dl> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

**HostComputer**
</dt> <dd> <dl>

Stringa ADsPath dell'host del servizio.

<dt>

Tipo di accesso: lettura/scrittura
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

**LoadOrderGroup**
</dt> <dd> <dl>

Nome del gruppo di ordini di carico di cui questo servizio è membro.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

**Percorso**
</dt> <dd> <dl>

Percorso e nome file dell'eseguibile del servizio.

<dt>

Tipo di accesso: lettura/scrittura
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


</dt> </dl> </dd> <dt>

**ServiceAccountName**
</dt> <dd> <dl>

Nome dell'account utilizzato dal servizio per l'autenticazione all'avvio.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

**ServiceAccountPath**
</dt> <dd> <dl>

Percorso dell'account specificato dalla proprietà **ServiceAccountPath** .

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

**ServiceType**
</dt> <dd> <dl>

Descrizione del modo in cui un servizio presenta se stesso nel computer host. Questa proprietà può essere zero o una combinazione di uno o più dei valori seguenti.

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

DRIVER del kernel del servizio ADS * * * * \_ \_ \_ (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

\_Driver del \_ file System del servizio ADS * * * * \_ \_ (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

\_Processo del servizio ADS * * * * \_ \_ (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

Processo di condivisione del servizio ADS * * * * \_ \_ \_ (0x00000020)


</dt> <dd></dd> </dl> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

**Tipo di avvio**
</dt> <dd> <dl>

Determina come avviare il servizio. Di seguito sono riportati i valori validi per questa proprietà.

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>avvio \_ avvio del servizio ADS \_ \_ * * * *


</dt> <dd>

Il servizio è un driver di dispositivo avviato dal caricatore di sistema. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_avvio del sistema del servizio ADS \_ \_ * * * *


</dt> <dd>

Il servizio è un driver di dispositivo avviato dalla funzione **IoInitSystem** . Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_avvio automatico del servizio ADS \_ \_ * * * *


</dt> <dd>

Il servizio verrà avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\_ \_ avvio richiesta servizio ADS \_ * * * *


</dt> <dd>

Il servizio verrà avviato da Gestione controllo servizi quando un processo chiama la funzione [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_servizio ADS \_ disabilitato * * * *


</dt> <dd>

Impossibile avviare il servizio. Tenta di avviare il risultato del servizio nel servizio errori codice di errore **\_ \_ disabilitato**.

</dd> </dl> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

**StartupParameters**
</dt> <dd> <dl>

Parametri passati al servizio all'avvio.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

**Versione**
</dt> <dd> <dl>

Versione del servizio.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come elencare tutti i servizi di sistema disponibili in esecuzione nel computer host, "computer", insieme al percorso per trovare i file eseguibili dei servizi.


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsService è definito come 68AF66E0-31CA-11CF-A98A-00AA006BC149<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[Metodi di proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

