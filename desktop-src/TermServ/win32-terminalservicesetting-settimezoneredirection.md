---
title: Metodo SetTimeZoneRedirection della classe Win32_TerminalServiceSetting
description: Il metodo SetTimeZoneRedirection imposta la proprietà TimeZoneRedirection, che consente al computer client di reindirizzare le impostazioni del fuso orario Servizi Desktop remoto sessione.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Metodo SetTimeZoneRedirection Servizi Desktop remoto
- Metodo SetTimeZoneRedirection Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto metodo SetTimeZoneRedirection
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
ms.openlocfilehash: 802cd4741f4ea30f378492075f69dfa21dfce54688fbc7ff9e72b957689d7c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755642"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetTimeZoneRedirection della classe TerminalServiceSetting Win32 \_

Il **metodo SetTimeZoneRedirection** imposta la **proprietà TimeZoneRedirection,** che consente al computer client di reindirizzare le impostazioni del fuso orario Servizi Desktop remoto sessione.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TimeZoneRedirection* \[ Pollici\]
</dt> <dd>

Nuovo valore per la **proprietà TimeZoneRedirection.**

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Disabilita la **proprietà TimeZoneRedirection.** Non viene eseguito alcun reindirizzamento del fuso orario.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Abilita la **proprietà TimeZoneRedirection.** Il fuso orario del client viene reindirizzato al fuso orario della sessione.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il fuso orario per la sessione Servizi Desktop remoto è uguale al fuso orario per il server host sessione Desktop remoto (Host sessione Desktop remoto). I computer client non possono reindirizzare le informazioni sul fuso orario.

Se il reindirizzamento del fuso orario è disabilitato, le nuove sessioni ereditano il fuso orario del server. Quando una sessione si riconnette, la sessione mantiene il fuso orario che aveva prima della disconnessione.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

