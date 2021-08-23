---
description: 'Metodo LockMedia della classe Msvm_DVDDrive : blocca o rilascia il supporto.'
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Metodo LockMedia della classe Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e86ef975d872f0fd86922f25f9752fda7508a037e293db85245ef6b1384a1570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525321"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a>Metodo LockMedia della classe MSvm \_ DVDDrive

Blocca o rilascia il supporto.

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

[**Unità \_ DVD Msvm**](msvm-dvddrive.md)
</dt> </dl>

 

 




