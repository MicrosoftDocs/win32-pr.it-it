---
title: Metodo SetVirtualizeLoopbackAddressesEnabled della Win32_TSVirtualIP classe
description: Imposta il valore della proprietà VirtualizeLoopbackAddressesEnabled.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Metodo SetVirtualizeLoopbackAddressesEnabled Servizi Desktop remoto
- Metodo SetVirtualizeLoopbackAddressesEnabled Servizi Desktop remoto , Win32_TSVirtualIP classe
- Win32_TSVirtualIP classe Servizi Desktop remoto, metodo SetVirtualizeLoopbackAddressesEnabled
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
ms.openlocfilehash: 5168ddd271dcf013a7595be1e1bdf32cde91e8f9f3ce8cfebc3b9f39af1fa109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000490"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a>Metodo SetVirtualizeLoopbackAddressesEnabled della classe \_ Win32 TSVirtualIP

Imposta il **valore della proprietà VirtualizeLoopbackAddressesEnabled.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VirtualizeLoopbackAddressesEnabled* \[ Pollici\]
</dt> <dd>

Specifica se abilitare la virtualizzazione degli indirizzi di loopback. Può essere uno dei valori seguenti.

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

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





