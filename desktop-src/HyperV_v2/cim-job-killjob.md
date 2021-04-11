---
description: Metodo che consente di terminare il processo e tutti i processi sottostanti e di rimuovere tutte le associazioni in sospeso. Questo metodo è deprecato; in alternativa, usare RequestChangeState.
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
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967314"
---
# <a name="killjob-method-of-the-cim_job-class"></a>Metodo KillJob della classe di \_ processi CIM

Metodo che consente di terminare il processo e tutti i processi sottostanti e di rimuovere tutte le associazioni "penzoloni". Questo metodo è deprecato; in alternativa, usare **RequestChangeState** . **KillJob** è stato deprecato perché non vi è alcuna distinzione tra un arresto ordinato e un kill immediato. [**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() fornisce le opzioni ' terminate ' è Kill ' per consentire questa distinzione.

## <a name="syntax"></a>Sintassi


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DeleteOnKill* \[ in\]
</dt> <dd>

Indica se il processo deve essere eliminato automaticamente al termine della terminazione. Questo parametro ha la precedenza sulla proprietà **DeleteOnCompletion** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Sconosciuto** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Non riuscito** (4)
</dt> <dt>

**Accesso negato** (6)
</dt> <dt>

**Non trovato** (7)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Processo CIM**](cim-job.md)
</dt> </dl>

 

 




