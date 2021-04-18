---
title: Metodo SetAllowDwm della classe Win32_TSClientSetting
description: Imposta la proprietà AllowDwm.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetAllowDwm
- Metodo SetAllowDwm Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, metodo SetAllowDwm
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39441ba3244f206b057ba47c3cb6f765b5e80604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301518"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a>Metodo SetAllowDwm della \_ classe TSClientSetting Win32

Imposta la proprietà **AllowDwm** .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AllowDwm* \[ in\]
</dt> <dd>

Nuovo valore della proprietà **AllowDwm** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

 





