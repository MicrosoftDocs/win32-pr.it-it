---
description: Inserisce un interrupt non mascherabile nella macchina virtuale.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: 'Metodo Msvm_ComputerSystem:: InjectNonMaskableInterrupt'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5798079a8866d9fb67356adff43c0ac1e993e6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306044"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a>\_Metodo MSVM ComputerSystem:: InjectNonMaskableInterrupt

Inserisce un interrupt non mascherabile nella macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) per tenere traccia dello stato dell'inserimento di interrupt. Questo riferimento può essere **null** se l'attività è stata completata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Accesso negato** (32769)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\\\Virtualizzazione radice \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ComputerSystem MSVM**](msvm-computersystem.md)
</dt> </dl>

 

