---
description: Mostra le metriche per classe.
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
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311785"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Metodo ShowMetricsByClass della classe MSVM \_ MetricService

Mostra le metriche per classe.

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

*Oggetto* \[ in\]
</dt> <dd>

Identifica una classe CIM per la quale il metodo restituisce riferimenti a istanze [**di \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definiscono le metriche che sono disponibili per l'acquisizione per tutte le istanze della classe.

</dd> <dt>

*Definizione* \[ di in\]
</dt> <dd>

Identifica un'istanza di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md). Il metodo restituisce riferimenti a istanze di [**CIM \_ Managed**](cim-managedelement.md) per le quali è possibile raccogliere le metriche definite dall'istanza di **CIM \_ BaseMetricDefinition** .

</dd> <dt>

*Definizione* \[ out\]
</dt> <dd>

Al completamento del metodo, può contenere riferimenti a istanze di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per l'oggetto [**\_ gestito CIM**](cim-managedelement.md) identificato dal parametro *Subject* .

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

Al completamento del metodo, ogni indice di matrice contiene il valore della proprietà **Name** per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice della matrice corrispondente del parametro *Definition* .

</dd> <dt>

*MetricCollectionEnabled* \[ out\]
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

**Fornitore riservato** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Operazione riuscita** ()
</dt> <dt>

**Non supportato** ()
</dt> <dt>

**Non riuscito** ()
</dt> <dt>

**Metodo riservato** ()
</dt> <dt>

**Specifico del fornitore** ()
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

 

 




