---
description: "Segnala quanto segue: le metriche disponibili per la raccolta per tutte le istanze di una classe CIM, le classi CIM per le quali è possibile raccogliere una metrica definita da un'istanza di CIM BaseMetricDefinition e se una metrica specifica è attualmente raccolta per un elemento \\_ gestito."
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Metodo ShowMetricsByClass della classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c70d81f153471e841803dde195f09886137f29b390298c2c7d09ce69ad1648e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694951"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a>Metodo ShowMetricsByClass della classe \_ CIM MetricService

Segnala quanto segue: le metriche disponibili per la raccolta per tutte le istanze di una classe CIM, le classi CIM per le quali è possibile raccogliere una metrica definita da un'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) e se una metrica specifica è attualmente raccolta per un elemento gestito.

## <a name="syntax"></a>Sintassi


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Oggetto* \[ Pollici\]
</dt> <dd>

Identifica una classe CIM per cui il metodo restituisce riferimenti a istanze di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per l'acquisizione per tutte le istanze della classe.

</dd> <dt>

*Definizione* \[ Pollici\]
</dt> <dd>

Identifica un'istanza di [**CIM \_ BaseMetricDefinition.**](cim-basemetricdefinition.md) Il metodo restituisce riferimenti a istanze [**di CIM \_ ManagedElement**](cim-managedelement.md) per le quali le metriche definite dall'istanza di **CIM \_ BaseMetricDefinition** sono disponibili per la raccolta.

</dd> <dt>

*DefinitionList* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, può contenere riferimenti a istanze [**di oggetti CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per [**CIM \_ ManagedElement**](cim-managedelement.md) identificato dal *parametro Subject.*

</dd> <dt>

*MetricNames* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, ogni indice di matrice deve contenere il valore della proprietà **Name** per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice di matrice corrispondente del *parametro DefinitionList.*

</dd> <dt>

*MetricCollectionEnabled* \[ Cambio\]
</dt> <dd>

Indica se viene raccolta una metrica per tutte le istanze di una classe di elementi gestiti.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (3)


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

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.

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

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




