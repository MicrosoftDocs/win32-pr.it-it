---
description: Mostra le metriche in base alla classe.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Metodo ShowMetricsByClass della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 40865847b1deef877c70c1c99349c12915a464b394a38b5b804ea9139d5d0cf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147510"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Metodo ShowMetricsByClass della classe Msvm \_ MetricService

Mostra le metriche in base alla classe.

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

Al termine del metodo, può contenere riferimenti a istanze di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per [**CIM \_ ManagedElement**](cim-managedelement.md) identificate dal *parametro Subject.*

</dd> <dt>

*MetricNames* \[ Cambio\]
</dt> <dd>

Al termine del metodo, ogni indice di matrice contiene il valore della proprietà **Name** per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice di matrice corrispondente del *parametro DefinitionList.*

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

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Operazione riuscita** ()
</dt> <dt>

**Non supportato** ()
</dt> <dt>

**Operazione non** riuscita ()
</dt> <dt>

**Metodo riservato** ()
</dt> <dt>

**Specifico del fornitore** ()
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

 

 




