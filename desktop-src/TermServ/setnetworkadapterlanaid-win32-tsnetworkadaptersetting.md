---
title: Metodo SetNetworkAdapterLanaID della classe Win32_TSNetworkAdapterSetting
description: Specifica il numero di scheda di rete locale (LANA) della scheda di rete da impostare.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetNetworkAdapterLanaID
- Metodo SetNetworkAdapterLanaID Servizi Desktop remoto, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Servizi Desktop remoto, metodo SetNetworkAdapterLanaID
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
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743495"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>Metodo SetNetworkAdapterLanaID della \_ classe TSNetworkAdapterSetting Win32

Il metodo **SetNetworkAdapterLanaID** specifica il numero di scheda di rete locale (lana) della scheda di rete da impostare. Se l'ID di LANA specificato non è valido o non esiste, viene restituito un errore. L'elenco di ID di LANA disponibile viene ottenuto enumerando la proprietà **DeviceIDList** nella classe [**\_ TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md) .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkAdapterLanaID* \[ in\]
</dt> <dd>

Numero di LANA della scheda di rete da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

