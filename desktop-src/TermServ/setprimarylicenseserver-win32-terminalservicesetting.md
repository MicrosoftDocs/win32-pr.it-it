---
title: Metodo SetPrimaryLicenseServer della classe Win32_TerminalServiceSetting
description: Imposta il server licenze specificato come prima voce nell'elenco dei server licenze specificati.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- Metodo SetPrimaryLicenseServer Servizi Desktop remoto
- Metodo SetPrimaryLicenseServer Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto, metodo SetPrimaryLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42eee8bbcab6494459ddde5c339f3836cab414ad3c2f5204399bac09e362c3ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008921"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetPrimaryLicenseServer della classe TerminalServiceSetting Win32 \_

Imposta il server licenze specificato come prima voce nell'elenco dei server licenze specificati.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LicenseServerName* \[ Pollici\]
</dt> <dd>

Nome del server licenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





