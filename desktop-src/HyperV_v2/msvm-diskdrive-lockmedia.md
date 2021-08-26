---
description: Blocca o sblocca il supporto.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Metodo LockMedia della classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d6a3b35b418427a4af8f86dfb162cff7009539d93eab3d87f0c96423a5e951e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130581"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a>Metodo LockMedia della classe Msvm \_ DiskDrive

Blocca o sblocca il supporto.

## <a name="syntax"></a>Sintassi


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Blocco* \[ Pollici\]
</dt> <dd>

**true** per bloccare il supporto; **false** per rilasciare il supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ DiskDrive**](msvm-diskdrive.md)
</dt> </dl>

 

 




