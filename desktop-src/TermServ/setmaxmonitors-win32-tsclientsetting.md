---
title: Metodo SetMaxMonitors della classe Win32_TSClientSetting
description: Imposta la proprietà MaxMonitors.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetMaxMonitors
- Metodo SetMaxMonitors Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, metodo SetMaxMonitors
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301857"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a>Metodo SetMaxMonitors della \_ classe TSClientSetting Win32

Imposta la proprietà **MaxMonitors** .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MaxMonitors* \[ in\]
</dt> <dd>

Specifica il nuovo numero massimo di monitoraggi supportati dal server. Il valore minimo è 1 e il valore massimo è 10.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.

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

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

 





