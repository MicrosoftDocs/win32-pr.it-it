---
title: Metodo SetTimeZoneRedirection della classe Win32_TerminalServiceSetting
description: Il metodo SetTimeZoneRedirection imposta la proprietà TimeZoneRedirection, che consente al computer client di reindirizzare le impostazioni del fuso orario al Servizi Desktop remoto sessione.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetTimeZoneRedirection
- Metodo SetTimeZoneRedirection Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetTimeZoneRedirection
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301510"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetTimeZoneRedirection della \_ classe TerminalServiceSetting Win32

Il metodo **SetTimeZoneRedirection** imposta la proprietà **TimeZoneRedirection** , che consente al computer client di reindirizzare le impostazioni del fuso orario al Servizi Desktop remoto sessione.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TimeZoneRedirection* \[ in\]
</dt> <dd>

Nuovo valore per la proprietà **TimeZoneRedirection** .

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Disabilita la proprietà **TimeZoneRedirection** . Non si verifica alcun reindirizzamento del fuso orario.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Abilita la proprietà **TimeZoneRedirection** . Il fuso orario del client viene reindirizzato al fuso orario della sessione.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il fuso orario per la sessione di Servizi Desktop remoto corrisponde al fuso orario del server di host sessione Desktop remoto (host sessione Desktop remoto). I computer client non possono reindirizzare le informazioni sul fuso orario.

Se il reindirizzamento del fuso orario è disabilitato, le nuove sessioni ereditano il fuso orario del server. Quando una sessione viene riconnessa, la sessione mantiene il fuso orario precedente alla disconnessione.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

