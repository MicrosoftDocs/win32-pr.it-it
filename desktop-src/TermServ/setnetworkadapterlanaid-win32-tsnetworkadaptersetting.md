---
title: Metodo SetNetworkAdapterLanaID della Win32_TSNetworkAdapterSetting classe
description: Specifica il numero LANA (Local Area Network Adapter) della scheda di rete da impostare.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Metodo SetNetworkAdapterLanaID Servizi Desktop remoto
- Metodo SetNetworkAdapterLanaID Servizi Desktop remoto , Win32_TSNetworkAdapterSetting classe
- Win32_TSNetworkAdapterSetting classe Servizi Desktop remoto, metodo SetNetworkAdapterLanaID
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5ffe976da794714f01e711913c01216d6b9bfad30c8c337da1fbd4c796e5f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008961"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>Metodo SetNetworkAdapterLanaID della classe \_ Win32 TSNetworkAdapterSetting

Il **metodo SetNetworkAdapterLanaID** specifica il numero LANA (Local Area Network Adapter) della scheda di rete da impostare. Se l'ID LANA specificato non è valido o non esiste, viene restituito un errore. L'elenco disponibile di ID LANA viene ottenuto enumerando la proprietà **DeviceIDList** nella [**classe \_ Win32 TSNetworkAdapterSetting.**](win32-tsnetworkadaptersetting.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkAdapterLanaID* \[ Pollici\]
</dt> <dd>

Numero LANA della scheda di rete da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto di questi valori,](terminal-services-wmi-provider-error-codes.md) fare riferimento Servizi Desktop remoto di errore del provider WMI.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

