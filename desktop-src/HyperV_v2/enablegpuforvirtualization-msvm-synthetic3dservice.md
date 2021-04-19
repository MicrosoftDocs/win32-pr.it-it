---
description: Abilita una GPU fisica per la virtualizzazione.
ms.assetid: 700cb46b-97f1-40cf-88d2-64242f4bd2c6
title: Metodo EnableGPUForVirtualization della classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.EnableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cf21424e9af8398cd435dce409bccde03543a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315502"
---
# <a name="enablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a>Metodo EnableGPUForVirtualization della classe MSVM \_ Synthetic3DService

Abilita una GPU fisica per la virtualizzazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PhysicalGPU* \[ in\]
</dt> <dd>

Riferimento a un'istanza della classe [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) che rappresenta la GPU fisica da abilitare.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Synthetic3DService MSVM**](msvm-synthetic3dservice.md)
</dt> </dl>

 

