---
title: Metodo SetMaxYResolution della classe Win32_TSClientSetting
description: Imposta la proprietà MaxYResolution.
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- Metodo SetMaxYResolution Servizi Desktop remoto
- Metodo SetMaxYResolution Servizi Desktop remoto , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Servizi Desktop remoto , metodo SetMaxYResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd980857e727943e3af101518bcfcb9ce4212f822aadf95bcb5829d9b11b693
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987891"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a>Metodo SetMaxYResolution della classe \_ Win32 TSClientSetting

Imposta la **proprietà MaxYResolution.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MaxYResolution* \[ Pollici\]
</dt> <dd>

Nuova risoluzione Y massima supportata dal server. Il valore minimo è 200 e il valore massimo è 2048.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





