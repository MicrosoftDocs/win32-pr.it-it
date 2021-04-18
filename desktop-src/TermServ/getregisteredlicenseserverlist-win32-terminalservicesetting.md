---
title: Metodo GetRegisteredLicenseServerList della classe Win32_TerminalServiceSetting
description: Ottiene l'elenco dei server licenze registrati.
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetRegisteredLicenseServerList
- Metodo GetRegisteredLicenseServerList Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo GetRegisteredLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302472"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Metodo GetRegisteredLicenseServerList della \_ classe TerminalServiceSetting Win32

Ottiene l'elenco dei server licenze registrati.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RegisteredLSList* \[ out\]
</dt> <dd>

Matrice di stringhe che riceve l'elenco dei server licenze registrati. Se non è presente alcun server licenze registrato, questa matrice sarà vuota.

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

 

 





