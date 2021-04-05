---
title: Metodo RemoveLSFromSpecifiedLicenseServerList della classe Win32_TerminalServiceSetting
description: Rimuove il server licenze specificato dall'elenco dei server licenze specificati.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveLSFromSpecifiedLicenseServerList
- Metodo RemoveLSFromSpecifiedLicenseServerList Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo RemoveLSFromSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901c2676748e819290855df2de51e5d7936dc793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873813"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Metodo RemoveLSFromSpecifiedLicenseServerList della \_ classe TerminalServiceSetting Win32

Rimuove il server licenze specificato dall'elenco dei server licenze specificati.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LicenseServerName* \[ in\]
</dt> <dd>

Nome del server licenze da rimuovere.

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
</dt> <dt>

[**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





