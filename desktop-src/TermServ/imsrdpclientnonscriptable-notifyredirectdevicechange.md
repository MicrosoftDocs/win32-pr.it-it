---
title: Metodo IMsRdpClientNonScriptable NotifyRedirectDeviceChange
description: Notifica al modulo di reindirizzamento del dispositivo il controllo Desktop remoto ActiveX che si è verificata una modifica del dispositivo nel sistema. Questo metodo passa le \_ notifiche DEVICECHANGE WM al controllo.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto
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
ms.openlocfilehash: 37986a218f672f5ace6d81b6496b958547e70a95f8ddea91bf6a130eb05b1ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130078"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>Metodo IMsRdpClientNonScriptable::NotifyRedirectDeviceChange

Notifica al modulo di reindirizzamento del dispositivo il controllo Desktop remoto ActiveX che si è verificata una modifica del dispositivo nel sistema. Questo metodo passa [**le \_ notifiche DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange) al controllo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Specifica l'evento del dispositivo. Questo parametro può avere uno dei valori seguenti.

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**


</dt> <dd>

Una richiesta di modifica della configurazione corrente (ancora o disanco) è stata annullata.

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ CONFIGCHANGED**


</dt> <dd>

La configurazione corrente è stata modificata a causa di un'ancoraggio o uno sganciamento.

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**


</dt> <dd>

Si è verificato un evento personalizzato.

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRIVAL**


</dt> <dd>

Un dispositivo è stato inserito ed è ora disponibile.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**


</dt> <dd>

È richiesta l'autorizzazione per rimuovere un dispositivo. Qualsiasi applicazione può rifiutare questa richiesta e annullare la rimozione.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**


</dt> <dd>

Una richiesta di rimozione di un dispositivo è stata annullata.

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**


</dt> <dd>

Un dispositivo è stato rimosso.

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**


</dt> <dd>

Un dispositivo sta per essere rimosso. La rimozione non può essere negata.

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**


</dt> <dd>

Si è verificato un evento specifico del dispositivo.

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ MODIFICATO**


</dt> <dd>

Un dispositivo è stato aggiunto o rimosso dal sistema.

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**


</dt> <dd>

È richiesta l'autorizzazione per modificare la configurazione corrente (ancora o disanco).

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ DEFINITO DALL'UTENTE**


</dt> <dd>

Il significato di questo messaggio è definito dall'utente.

</dd> </dl> </dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura che contiene dati specifici dell'evento. Il formato dipende dal valore del *parametro wParam.* Per altre informazioni, vedere la documentazione per ogni evento. Per altre informazioni, vedere [Tipi di eventi del dispositivo.](/windows/desktop/DevIO/device-event-types)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Un'applicazione contenitore che consente l'aggiunta o la rimozione dinamica dei dispositivi deve elaborare il messaggio [**\_ DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange) nella finestra di primo livello e inoltrare il messaggio al controllo usando il **metodo NotifyRedirectDeviceChange.** Un esempio di modifica dinamica del dispositivo è quando un'unità disco reindirizzata viene aggiunta o rimossa mentre il sistema è in esecuzione.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                     |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                               |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable è definito come 2f079c4c-87b2-4afd-97ab-20cdb43038ae<br/> |



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

 

