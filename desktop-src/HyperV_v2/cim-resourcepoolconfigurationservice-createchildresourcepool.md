---
description: Avviare un processo per creare un pool secondario da un pool padre usando le impostazioni di allocazione specificate.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Metodo CreateChildResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 48a43baeefcbc56707fa6327930d9c18eaa57a2442b81fbc5f5cff17633b2148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648153"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Metodo CreateChildResourcePool della classe \_ CIM ResourcePoolConfigurationService

Avviare un processo per creare un pool secondario da un pool padre usando le impostazioni di allocazione specificate.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ElementName* \[ Pollici\]
</dt> <dd>

Nome pertinente dell'utente finale per il pool da creare. Se **NULL,** è possibile usare un nome predefinito fornito dal sistema. Il valore verrà archiviato nella proprietà **ElementName** per l'elemento creato.

</dd> <dt>

*Impostazioni* \[ Pollici\]
</dt> <dd>

Stringa contenente una rappresentazione di [**un'istanza \_ CIM SettingData**](cim-settingdata.md) usata per specificare le impostazioni per il pool figlio.

</dd> <dt>

*ParentPool* \[ Pollici\]
</dt> <dd>

Pool [**di risorse CIM \_**](cim-resourcepool.md) da cui creare il nuovo pool.

</dd> <dt>

*Pool* \[ Cambio\]
</dt> <dd>

Pool [**di risorse CIM \_ che**](cim-resourcepool.md) fa riferimento al pool risultante.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Riferimento al processo (può essere Null se il processo è stato completato).

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

**Parametro non valido** (5)
</dt> <dt>

**In uso** (6)
</dt> <dt>

**ResourceType non corretto per il pool** (7)
</dt> <dt>

**Risorse insufficienti** (8)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Dimensioni non supportate** (4097)
</dt> <dt>

**Metodo riservato** (4098..32767)
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

 

 




