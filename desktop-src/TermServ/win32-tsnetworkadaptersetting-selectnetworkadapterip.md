---
title: Metodo SelectNetworkAdapterIP della classe Win32_TSNetworkAdapterSetting
description: Seleziona una scheda di rete in base all'indirizzo IP della scheda.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SelectNetworkAdapterIP
- Metodo SelectNetworkAdapterIP Servizi Desktop remoto, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Servizi Desktop remoto, metodo SelectNetworkAdapterIP
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
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301441"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Metodo SelectNetworkAdapterIP della \_ classe TSNetworkAdapterSetting Win32

Seleziona una scheda di rete in base all'indirizzo IP della scheda.

## <a name="syntax"></a>Sintassi


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkAdapterIP* \[ in\]
</dt> <dd>

Indirizzo IP della scheda di rete da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se l'indirizzo IP specificato è valido e restituisce un codice di errore WMI se l'indirizzo IP non è valido o non esiste. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Commenti

È possibile recuperare l'indirizzo IP di una scheda di rete enumerando le proprietà della classe [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) .

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

 

