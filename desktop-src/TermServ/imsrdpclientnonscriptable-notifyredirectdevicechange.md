---
title: Metodo IMsRdpClientNonScriptable NotifyRedirectDeviceChange
description: Notifica al modulo di reindirizzamento del dispositivo del Desktop remoto controllo ActiveX che si è verificata una modifica del dispositivo nel sistema. Questo metodo passa \_ le notifiche di WM DEVICECHANGE al controllo.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964883"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>Metodo IMsRdpClientNonScriptable:: NotifyRedirectDeviceChange

Notifica al modulo di reindirizzamento del dispositivo del Desktop remoto controllo ActiveX che si è verificata una modifica del dispositivo nel sistema. Questo metodo passa le notifiche di [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) al controllo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Specifica l'evento del dispositivo. Questo parametro può avere uno dei valori seguenti.

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**\_CONFIGCHANGECANCELED DBT**


</dt> <dd>

Una richiesta di modifica della configurazione corrente (dock o Undock) è stata annullata.

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**\_CONFIGCHANGED DBT**


</dt> <dd>

La configurazione corrente è cambiata a causa di un ancoraggio o di Undock.

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**\_CUSTOMEVENT DBT**


</dt> <dd>

Si è verificato un evento personalizzato.

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**\_DEVICEARRIVAL DBT**


</dt> <dd>

Un dispositivo è stato inserito ed è ora disponibile.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**\_DEVICEQUERYREMOVE DBT**


</dt> <dd>

Viene richiesta l'autorizzazione per rimuovere un dispositivo. Qualsiasi applicazione può negare questa richiesta e annullare la rimozione.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**\_DEVICEQUERYREMOVEFAILED DBT**


</dt> <dd>

Una richiesta di rimozione di un dispositivo è stata annullata.

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**\_DEVICEREMOVECOMPLETE DBT**


</dt> <dd>

Un dispositivo è stato rimosso.

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**\_DEVICEREMOVEPENDING DBT**


</dt> <dd>

Un dispositivo sta per essere rimosso. Non è possibile negare la rimozione.

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**\_DEVICETYPESPECIFIC DBT**


</dt> <dd>

Si è verificato un evento specifico del dispositivo.

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**\_DEVNODE DBT \_ modificato**


</dt> <dd>

Un dispositivo è stato aggiunto o rimosso dal sistema.

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**\_QUERYCHANGECONFIG DBT**


</dt> <dd>

Viene richiesta l'autorizzazione per modificare la configurazione corrente (dock o Undock).

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**\_USERDEFINED DBT**


</dt> <dd>

Il significato di questo messaggio è definito dall'utente.

</dd> </dl> </dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una struttura che contiene dati specifici dell'evento. Il formato dipende dal valore del parametro *wParam* . Per ulteriori informazioni, vedere la documentazione relativa a ogni evento. Per altre informazioni, vedere [tipi di eventi del dispositivo](/windows/desktop/DevIO/device-event-types).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Un'applicazione contenitore che consente l'aggiunta o la rimozione dinamica dei dispositivi deve elaborare il messaggio [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) nella finestra di primo livello e trasmettere il messaggio al controllo usando il metodo **NotifyRedirectDeviceChange** . Un esempio di una modifica dinamica del dispositivo si verifica quando viene aggiunta o rimossa un'unità disco reindirizzata mentre il sistema è in esecuzione.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                     |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                               |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable è definito come 2f079c4c-87B2-4afd-97AB-20cdb43038ae<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

