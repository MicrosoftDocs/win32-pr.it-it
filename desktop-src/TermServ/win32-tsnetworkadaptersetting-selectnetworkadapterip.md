---
title: Metodo SelectNetworkAdapterIP della Win32_TSNetworkAdapterSetting classe
description: Seleziona una scheda di rete in base all'indirizzo IP della scheda.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Metodo SelectNetworkAdapterIP Servizi Desktop remoto
- Metodo SelectNetworkAdapterIP Servizi Desktop remoto , Win32_TSNetworkAdapterSetting classe
- Win32_TSNetworkAdapterSetting classe Servizi Desktop remoto , metodo SelectNetworkAdapterIP
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a88c4820e4537d9c0fb1833b67eb2660a7fb5618189023dfe2217f222efa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008371"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Metodo SelectNetworkAdapterIP della classe \_ Win32 TSNetworkAdapterSetting

Seleziona una scheda di rete in base all'indirizzo IP della scheda.

## <a name="syntax"></a>Sintassi


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkAdapterIP* \[ Pollici\]
</dt> <dd>

Indirizzo IP della scheda di rete da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se l'indirizzo IP specificato è valido e restituisce un codice di errore WMI se l'indirizzo IP non è valido o non esiste. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

## <a name="remarks"></a>Commenti

È possibile recuperare l'indirizzo IP di una scheda di rete enumerando le proprietà della [**classe \_ TSNetworkAdapterListSetting Win32.**](win32-tsnetworkadapterlistsetting.md)

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

