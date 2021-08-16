---
title: Metodo SetFallbackPrintDriverType della classe Win32_TerminalServiceSetting
description: Il metodo SetFallbackPrintDriverType imposta la proprietà FallbackPrintDriverType per la classe.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Metodo SetFallbackPrintDriverType Servizi Desktop remoto
- Metodo SetFallbackPrintDriverType Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto metodo SetFallbackPrintDriverType
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39033a34c75ea94f365ae690b1ac6fe4cd61663e9cd6db19f2cd2c232bd8c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137864"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetFallbackPrintDriverType della classe TerminalServiceSetting Win32 \_

Il **metodo SetFallbackPrintDriverType** imposta la **proprietà FallbackPrintDriverType** per la classe.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FallbackPrintDriverType* \[ Pollici\]
</dt> <dd>

Imposta la **proprietà FallbackPrintDriverType** che consente o nega nuove Servizi Desktop remoto connessioni.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Nessun driver di fallback.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

È meglio indovinare.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

È meglio indovinare. Se non viene trovata alcuna corrispondenza, eseguire il fallback Hewlett-Packard Printer Control Language (PCL).

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

È meglio indovinare. Se non viene trovata alcuna corrispondenza, eseguire il fallback a Postscript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

È meglio indovinare. Se non viene trovata alcuna corrispondenza, visualizzare i driver PS e PCL.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce Success in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere . Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

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

 

