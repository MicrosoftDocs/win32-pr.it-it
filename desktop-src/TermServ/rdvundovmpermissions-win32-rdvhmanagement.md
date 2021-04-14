---
title: Metodo RdvUndoVMPermissions della classe Win32_RdvhManagement
description: Ripristina le autorizzazioni impostate da RdvSetupVMPermissions nella macchina virtuale specificata.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RdvUndoVMPermissions
- Metodo RdvUndoVMPermissions Servizi Desktop remoto, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Servizi Desktop remoto, metodo RdvUndoVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478868"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Metodo RdvUndoVMPermissions della \_ classe RdvhManagement Win32

Ripristina le autorizzazioni impostate da [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) nella macchina virtuale specificata.

## <a name="syntax"></a>Sintassi


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VmName* \[ in\]
</dt> <dd>

Nome della macchina virtuale su cui annullare le autorizzazioni.

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

 

 





