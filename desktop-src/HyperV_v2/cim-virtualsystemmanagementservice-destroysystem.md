---
description: Elimina un sistema virtuale.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Metodo DestroySystem della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fa7bf479e1e861e8425376fa0ebb610cd0b728cc9f02ba80acc9c1faa284fc16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980551"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Metodo DestroySystem della classe \_ CIM VirtualSystemManagementService

Elimina un sistema virtuale.

Il sistema virtuale a cui si fa riferimento viene eliminato, inclusi gli eventuali elementi con ambito. Le risorse virtuali vengono restituite ai pool di risorse, il che può implicare la distruzione di tali risorse (dipendente dall'implementazione). Se il sistema virtuale è attivo quando l'operazione viene richiamata, viene prima disattivata e quindi distrutta. Se sono stati creati snapshot dal sistema virtuale, anche questi vengono distrutti.

## <a name="syntax"></a>Sintassi


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedSystem* \[ Pollici\]
</dt> <dd>

Riferimento a un'istanza della [**classe CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il sistema di computer virtuali da eliminare.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione è a esecuzione lunga, facoltativamente può essere restituito [**un processo CIM \_ ConcreteJob**](cim-concretejob.md) che rappresenta il processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non** valido (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
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

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




