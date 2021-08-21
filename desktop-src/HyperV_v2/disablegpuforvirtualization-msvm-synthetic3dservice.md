---
description: Disabilita una GPU fisica per la virtualizzazione.
ms.assetid: 280a3c25-7b8f-4113-bf35-171d15f4aea7
title: Metodo DisableGPUForVirtualization della classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.DisableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f156ee160f9ae158c36b1c7a237f746d6577906cc5e254a183308d5bec122a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150037"
---
# <a name="disablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a>Metodo DisableGPUForVirtualization della classe Msvm \_ Synthetic3DService

Disabilita una GPU fisica per la virtualizzazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 DisableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PhysicalGPU* \[ Pollici\]
</dt> <dd>

Riferimento a un'istanza della [**classe \_ Msvm Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) che rappresenta la GPU fisica da disabilitato.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ Synthetic3DService**](msvm-synthetic3dservice.md)
</dt> </dl>

 

