---
title: Metodo RdvMigrateVmToDifferentHost della classe Win32_RdvhManagement
description: Avvia una migrazione in tempo reale di una macchina virtuale in un host specificato.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RdvMigrateVmToDifferentHost
- Metodo RdvMigrateVmToDifferentHost Servizi Desktop remoto, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Servizi Desktop remoto, metodo RdvMigrateVmToDifferentHost
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3def1be6332397fb3830ffe8c90f324afc9f1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741495"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a>Metodo RdvMigrateVmToDifferentHost della \_ classe RdvhManagement Win32

Avvia una migrazione in tempo reale di una macchina virtuale in un host specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VmName* \[ in\]
</dt> <dd>

Nome della macchina virtuale da migrare.

</dd> <dt>

*DestinationHost* \[ in\]
</dt> <dd>

nome dell'host di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RdvhManagement Win32**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





