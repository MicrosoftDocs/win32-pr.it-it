---
description: Avviare un processo per eliminare un pool di risorse.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Metodo DeleteResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a5fb895eb76a503d6199bf1057a9f9eaff0c72e4af59460c63551a7c581ff0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648090"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Metodo DeleteResourcePool della classe \_ CIM ResourcePoolConfigurationService

Avviare un processo per eliminare un pool di risorse. Nessuna allocazione può essere in sospeso o l'eliminazione avrà esito negativo con "In uso". Se il pool di risorse è un pool di risorse radice, tutte le risorse host vengono restituite al sistema sottostante.

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pool* \[ Pollici\]
</dt> <dd>

Pool [**di risorse CIM \_**](cim-resourcepool.md) che fa riferimento al pool da eliminare.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Processo [**concreto CIM \_**](cim-concretejob.md) che fa riferimento al processo (può essere **Null** se il processo è stato completato).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.

<dl> <dt>

**Processo completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Sconosciuto** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Operazione non** riuscita (4)
</dt> <dt>

**Parametro non** valido (5)
</dt> <dt>

**In uso** (6)
</dt> <dt>

**ResourceType non corretto per il pool** (7)
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

[**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




