---
description: Metodo per compilare il processo e tutti i processi sottostanti e per rimuovere eventuali associazioni inesammate. Questo metodo è deprecato. In alternativa, usare RequestChangeState.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Metodo KillJob della classe CIM_Job
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 681d6a878f90f29708812fce2c39f27024ed588deb5f3b8066cc4833487fd91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900331"
---
# <a name="killjob-method-of-the-cim_job-class"></a>Metodo KillJob della classe Job \_ CIM

Metodo per compilare il processo e tutti i processi sottostanti e per rimuovere eventuali associazioni "inesammati". Questo metodo è deprecato. In **alternativa, usare RequestChangeState.** **KillJob** è deprecato perché non è stata fatta alcuna distinzione tra un arresto ordinato e un arresto immediato. [**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() fornisce le opzioni 'Terminate' e 'Kill' per consentire questa distinzione.

## <a name="syntax"></a>Sintassi


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DeleteOnKill* \[ Pollici\]
</dt> <dd>

Indica se il processo deve essere eliminato automaticamente al termine. Questo parametro ha la precedenza **sulla proprietà DeleteOnCompletion.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Sconosciuto** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Operazione non** riuscita (4)
</dt> <dt>

**Accesso negato** (6)
</dt> <dt>

**Non trovato** (7)
</dt> <dt>

**DmTF Reserved** (..)
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

[**Processo \_ CIM**](cim-job.md)
</dt> </dl>

 

 




