---
title: Metodo SetPrimaryLicenseServer della classe Win32_TerminalServiceSetting
description: Imposta il server licenze specificato come prima voce nell'elenco dei server licenze specificati.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetPrimaryLicenseServer
- Metodo SetPrimaryLicenseServer Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetPrimaryLicenseServer
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
ms.openlocfilehash: 61d73212230d1ca69e0a0809c48b8f2985920045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873481"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetPrimaryLicenseServer della \_ classe TerminalServiceSetting Win32

Imposta il server licenze specificato come prima voce nell'elenco dei server licenze specificati.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LicenseServerName* \[ in\]
</dt> <dd>

Nome del server licenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





