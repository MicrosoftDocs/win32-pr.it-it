---
description: Visualizza le metriche specificate.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Metodo ShowMetrics della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 052f708f07a8e1074eeaa6c8089ccd410bb63af478072545d5db92af7933fc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521471"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>Metodo ShowMetrics della classe Msvm \_ MetricService

Visualizza le metriche specificate.

## <a name="syntax"></a>Sintassi


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Oggetto* \[ Pollici\]
</dt> <dd>

Il parametro Subject identifica un'istanza di [**CIM \_ ManagedElement**](cim-managedelement.md) per cui il metodo restituisce riferimenti a istanze di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche acquisite per **CIM \_ ManagedElement.**

</dd> <dt>

*Definizione* \[ Pollici\]
</dt> <dd>

Il parametro Definition identifica un'istanza di [**CIM \_ BaseMetricDefinition.**](cim-basemetricdefinition.md) Il metodo restituisce riferimenti a istanze [**di CIM \_ ManagedElement**](cim-managedelement.md) per le quali le metriche definite dall'istanza di **CIM \_ BaseMetricDefinition** sono disponibili per la raccolta.

</dd> <dt>

*ManagedElements* \[ Cambio\]
</dt> <dd>

Al termine del metodo, il *parametro ManagedElements* può contenere riferimenti a \[ \] [**CIM \_ ManagedElement**](cim-managedelement.md) per cui la metrica identificata dal parametro *Definition* è disponibile per la raccolta.

</dd> <dt>

*DefinitionList* \[ Cambio\]
</dt> <dd>

Al termine del metodo, il *parametro DefinitionList* può contenere riferimenti a istanze di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per [**CIM \_ ManagedElement**](cim-managedelement.md) identificate dal *parametro Subject.*

</dd> <dt>

*MetricNames* \[ Cambio\]
</dt> <dd>

Al termine del metodo, ogni indice di matrice del parametro *MetricNames* deve contenere il valore della proprietà Name per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice di matrice corrispondente del *parametro DefinitionList.*

</dd> <dt>

*MetricCollectionEnabled* \[ Cambio\]
</dt> <dd>

Il *parametro MetricCollectionEnabled* indica se viene raccolta una metrica per un elemento gestito.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Abilita** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Disabilita** (3)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Riservato** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Metodo riservato** (..)
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

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




