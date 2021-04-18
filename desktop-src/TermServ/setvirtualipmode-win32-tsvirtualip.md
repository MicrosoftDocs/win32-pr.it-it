---
title: Metodo SetVirtualIPMode della classe Win32_TSVirtualIP
description: Imposta il valore della proprietà VirtualIPMode.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetVirtualIPMode
- Metodo SetVirtualIPMode Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo SetVirtualIPMode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301964"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a>Metodo SetVirtualIPMode della \_ classe TSVirtualIP Win32

Imposta il valore della proprietà **VirtualIPMode** .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VirtualIPMode* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Specifica la modalità di virtualizzazione IP utilizzata nel server. Può corrispondere a uno dei valori seguenti.

<dt>

0
</dt> <dd>

La modalità di virtualizzazione IP è per sessione.

</dd> <dt>

1
</dt> <dd>

La modalità di virtualizzazione IP è per utente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

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

 

 





