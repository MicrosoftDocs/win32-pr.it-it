---
title: Metodo RdvSetupVMPermissions della classe Win32_RdvhManagement
description: Imposta le autorizzazioni per una macchina virtuale per l'utente corrente.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- Metodo RdvSetupVMPermissions Servizi Desktop remoto
- Metodo RdvSetupVMPermissions Servizi Desktop remoto , Win32_RdvhManagement classe
- Win32_RdvhManagement classe Servizi Desktop remoto , metodo RdvSetupVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6628e3ac1660c1f0c505e3d5349dd481c7c48b09a77aaedeac1352ecbaf4562
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988811"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Metodo RdvSetupVMPermissions della classe \_ RdvhManagement Win32

Imposta le autorizzazioni per una macchina virtuale per l'utente corrente.

## <a name="syntax"></a>Sintassi


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VmName* \[ Pollici\]
</dt> <dd>

Nome della macchina virtuale su cui impostare le autorizzazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





