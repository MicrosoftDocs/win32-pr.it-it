---
description: Mostra la metrica specificata.
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
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885150"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>Metodo ShowMetrics della classe MSVM \_ MetricService

Mostra la metrica specificata.

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

*Oggetto* \[ in\]
</dt> <dd>

Il parametro Subject identifica un'istanza di [**CIM \_ Managed**](cim-managedelement.md) per la quale il metodo restituisce riferimenti a istanze di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definiscono le metriche acquisite per **CIM \_ managementelement**.

</dd> <dt>

*Definizione* \[ di in\]
</dt> <dd>

Il parametro Definition identifica un'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md). Il metodo restituisce riferimenti a istanze di [**CIM \_ Managed**](cim-managedelement.md) per le quali è possibile raccogliere le metriche definite dall'istanza di **CIM \_ BaseMetricDefinition** .

</dd> <dt>

*ManagedElements* \[ out\]
</dt> <dd>

Al completamento del metodo, il parametro *ManagedElements* \[ \] può contenere riferimenti a [**CIM \_ Managed**](cim-managedelement.md) per il quale la metrica identificata dal parametro *Definition* è disponibile per la raccolta.

</dd> <dt>

*Definizione* \[ out\]
</dt> <dd>

Al completamento del metodo, il parametro *definitionName* può contenere riferimenti a istanze di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per l'oggetto [**\_ gestito CIM**](cim-managedelement.md) identificato dal parametro *Subject* .

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

Al completamento del metodo, ogni indice della matrice del parametro *MetricNames* deve contenere il valore della proprietà Name per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice della matrice corrispondente del parametro *Definition* .

</dd> <dt>

*MetricCollectionEnabled* \[ out\]
</dt> <dd>

Il parametro *MetricCollectionEnabled* indica se viene raccolta una metrica per un elemento gestito.

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

**Fornitore riservato** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Metodo riservato** (..)
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

[**\_MetricService MSVM**](msvm-metricservice.md)
</dt> </dl>

 

 




