---
title: Metodo RemoveLSFromSpecifiedLicenseServerList Win32_TerminalServiceSetting classe
description: Rimuove il server licenze specificato dall'elenco dei server licenze specificati.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- Metodo RemoveLSFromSpecifiedLicenseServerList Servizi Desktop remoto
- Metodo RemoveLSFromSpecifiedLicenseServerList Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto metodo RemoveLSFromSpecifiedLicenseServerList
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
ms.openlocfilehash: 492b955b8aced6972ec80f499af5ca4b043141159ad2c8fd359225302d8f63b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605190"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Metodo RemoveLSFromSpecifiedLicenseServerList della classe TerminalServiceSetting Win32 \_

Rimuove il server licenze specificato dall'elenco dei server licenze specificati.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LicenseServerName* \[ Pollici\]
</dt> <dd>

Nome del server licenze da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

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
</dt> <dt>

[**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





