---
description: "Segnala quanto segue: le metriche disponibili per essere raccolte per un elemento gestito, gli elementi gestiti per i quali è disponibile una metrica definita da un'istanza di CIM \\_ BaseMetricDefinition e se è in corso la raccolta di una determinata metrica per un elemento gestito."
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: Metodo ShowMetrics della classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131747"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a>Metodo ShowMetrics della classe CIM \_ MetricService

Segnala quanto segue: le metriche disponibili per essere raccolte per un elemento gestito, gli elementi gestiti per i quali è disponibile una metrica definita da un'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) e se è in corso la raccolta di una determinata metrica per un elemento gestito.

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

Identifica un'istanza di [**CIM \_ Managed**](cim-managedelement.md) per la quale il metodo restituisce riferimenti a istanze di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definiscono le metriche acquisite per **CIM \_ managementelement**.

</dd> <dt>

*Definizione* \[ di in\]
</dt> <dd>

Identifica un'istanza di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md). Il metodo restituisce riferimenti a istanze di [**CIM \_ Managed**](cim-managedelement.md) per le quali è possibile raccogliere le metriche definite dall'istanza di **CIM \_ BaseMetricDefinition** .

</dd> <dt>

*ManagedElements* \[ out\]
</dt> <dd>

In presenza di esito positivo, può contenere riferimenti a oggetti [**CIM \_ gestitielement**](cim-managedelement.md) per i quali la metrica identificata dal parametro della *definizione* è disponibile per la raccolta.

</dd> <dt>

*Definizione* \[ out\]
</dt> <dd>

In caso di esito positivo, può contenere riferimenti a istanze di oggetti [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per l'oggetto [**\_ gestito CIM**](cim-managedelement.md) identificato dal parametro *Subject* .

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

In caso di esito positivo, ogni indice di matrice deve contenere il valore della proprietà **Name** per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice della matrice corrispondente del parametro *Definition* .

</dd> <dt>

*MetricCollectionEnabled* \[ out\]
</dt> <dd>

Indica se viene raccolta una metrica per un elemento gestito.

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

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

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

[**\_METRICSERVICE CIM**](cim-metricservice.md)
</dt> </dl>

 

 




