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
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308369"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>Metodo GetError della classe CIM \_ ConcreteJob

Recupera un errore a causa di un processo non riuscito. Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna istanza di [**\_ errore CIM**](cim-error.md) . Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, viene restituita un'istanza di **\_ errore CIM** .

## <a name="syntax"></a>Sintassi


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errore* \[ out\]
</dt> <dd>

Restituisce un'istanza di [**\_ errore CIM**](cim-error.md) se il **OperationalStatus** del processo non è "OK"; in caso contrario, restituisce **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Errore non specificato** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Non riuscito** (4)
</dt> <dt>

**Parametro non valido** (5)
</dt> <dt>

**Accesso negato** (6)
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

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> </dl>

 

 




