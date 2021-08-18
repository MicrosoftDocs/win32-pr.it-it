---
title: Metodo SetMaxXResolution della classe Win32_TSClientSetting
description: Imposta la proprietà MaxXResolution.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- Metodo SetMaxXResolution Servizi Desktop remoto
- Metodo SetMaxXResolution Servizi Desktop remoto , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Servizi Desktop remoto metodo SetMaxXResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759a674e2b283d18caf1cc4d1b2f3e3ecae786dc76f9acc222f47dd8daf385de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000511"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a>Metodo SetMaxXResolution della classe \_ Win32 TSClientSetting

Imposta la **proprietà MaxXResolution.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MaxXResolution* \[ Pollici\]
</dt> <dd>

Nuova risoluzione X massima supportata dal server. Il valore minimo è 200 e il valore massimo è 4096.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





