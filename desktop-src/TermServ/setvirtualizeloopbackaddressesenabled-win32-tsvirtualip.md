---
title: Metodo SetVirtualizeLoopbackAddressesEnabled della classe Win32_TSVirtualIP
description: Imposta il valore della proprietà VirtualizeLoopbackAddressesEnabled.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetVirtualizeLoopbackAddressesEnabled
- Metodo SetVirtualizeLoopbackAddressesEnabled Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo SetVirtualizeLoopbackAddressesEnabled
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301207"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a>Metodo SetVirtualizeLoopbackAddressesEnabled della \_ classe TSVirtualIP Win32

Imposta il valore della proprietà **VirtualizeLoopbackAddressesEnabled** .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VirtualizeLoopbackAddressesEnabled* \[ in\]
</dt> <dd>

Specifica se abilitare la virtualizzazione degli indirizzi di loopback. Può corrispondere a uno dei valori seguenti.

<dt>

0
</dt> <dd>

Non abilitare la virtualizzazione degli indirizzi di loopback.

</dd> <dt>

1
</dt> <dd>

Abilitare la virtualizzazione degli indirizzi di loopback.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





