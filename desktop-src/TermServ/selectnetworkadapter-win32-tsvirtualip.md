---
title: Metodo SelectNetworkAdapter della Win32_TSVirtualIP classe
description: Imposta l'indirizzo MAC della scheda di rete da usare per la virtualizzazione IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Metodo SelectNetworkAdapter Servizi Desktop remoto
- Metodo SelectNetworkAdapter Servizi Desktop remoto , Win32_TSVirtualIP classe
- Win32_TSVirtualIP classe Servizi Desktop remoto , metodo SelectNetworkAdapter
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d27df38f8314720c4ed16d675cdbd06424611d2ccd127a45069586875c82d77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865521"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a>Metodo SelectNetworkAdapter della classe \_ Win32 TSVirtualIP

Imposta l'indirizzo MAC della scheda di rete da usare per la virtualizzazione IP.

## <a name="syntax"></a>Sintassi


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkAdapterMacAddress* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Specifica l'indirizzo MAC della scheda di rete.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto di questi valori,](terminal-services-wmi-provider-error-codes.md) fare riferimento Servizi Desktop remoto di errore del provider WMI.

Se l'indirizzo MAC non è valido o non esiste oppure se la modalità di virtualizzazione IP è per sessione, viene restituito un errore.

Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

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

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





