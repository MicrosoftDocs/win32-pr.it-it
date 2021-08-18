---
title: Metodo RdvMigrateVmToDifferentHost della Win32_RdvhManagement classe
description: Avvia una migrazione in tempo reale di una macchina virtuale a un host specificato.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- Metodo RdvMigrateVmToDifferentHost Servizi Desktop remoto
- Metodo RdvMigrateVmToDifferentHost Servizi Desktop remoto , Win32_RdvhManagement classe
- Win32_RdvhManagement classe Servizi Desktop remoto, metodo RdvMigrateVmToDifferentHost
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
ms.openlocfilehash: 7a84171bc6db6a39cff5a2d55ca7e453bf9b963636ea765480fe87b16fd8da92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756243"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a>Metodo RdvMigrateVmToDifferentHost della classe \_ Win32 RdvhManagement

Avvia una migrazione in tempo reale di una macchina virtuale a un host specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VmName* \[ Pollici\]
</dt> <dd>

Nome della macchina virtuale di cui eseguire la migrazione.

</dd> <dt>

*Host di destinazione* \[ Pollici\]
</dt> <dd>

Nome dell'host di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto di questi valori,](terminal-services-wmi-provider-error-codes.md) fare riferimento Servizi Desktop remoto di errore del provider WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





