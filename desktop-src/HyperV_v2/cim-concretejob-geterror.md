---
description: Recupera un errore a causa di un processo non riuscito.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Metodo GetError della classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0b43d433bf9d2a3967efcc4a2e927d3bf687ebfa5ac67d7c7e34c48c34832c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813267"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>Metodo GetError della classe CIM \_ ConcreteJob

Recupera un errore a causa di un processo non riuscito. Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna [**istanza di Errore CIM. \_**](cim-error.md) Tuttavia, se il processo ha avuto esito negativo a causa di un problema interno o perché il processo è stato terminato da un client, viene restituita **un'istanza \_ di errore CIM.**

## <a name="syntax"></a>Sintassi


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errore* \[ Cambio\]
</dt> <dd>

Restituisce [**un'istanza CIM \_ Error**](cim-error.md) se **OperationalStatus** nel processo non è "OK". In caso contrario, restituisce **null.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Errore non specificato** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Operazione non** riuscita (4)
</dt> <dt>

**Parametro non valido** (5)
</dt> <dt>

**Accesso negato** (6)
</dt> <dt>

**DMTF riservato** (..)
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

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> </dl>

 

 




