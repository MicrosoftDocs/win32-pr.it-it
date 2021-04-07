---
title: Metodo SelectNetworkAdapter della classe Win32_TSVirtualIP
description: Imposta l'indirizzo MAC della scheda di rete da utilizzare per la virtualizzazione IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SelectNetworkAdapter
- Metodo SelectNetworkAdapter Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo SelectNetworkAdapter
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
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964138"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a>Metodo SelectNetworkAdapter della \_ classe TSVirtualIP Win32

Imposta l'indirizzo MAC della scheda di rete da utilizzare per la virtualizzazione IP.

## <a name="syntax"></a>Sintassi


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NetworkAdapterMacAddress* \[ in\]
</dt> <dd>

Tipo: **stringa**

Specifica l'indirizzo MAC della scheda di rete.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

Se l'indirizzo MAC non è valido o non esiste o se la modalità di virtualizzazione IP è per sessione, viene restituito un errore.

Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





