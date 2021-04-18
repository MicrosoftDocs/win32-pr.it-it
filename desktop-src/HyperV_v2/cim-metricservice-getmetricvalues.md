---
description: Fornisce la possibilità di restituire un elenco filtrato di \_ istanze di BASEMETRICVALUE CIM.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Metodo GetMetricValues della classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3c84ae9f5128edecfd3dd4cb591f811fdbd86010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312922"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a>Metodo GetMetricValues della classe CIM \_ MetricService

Fornisce la possibilità di restituire un elenco filtrato di istanze di [**\_ BaseMetricValue CIM**](cim-basemetricvalue.md) .

## <a name="syntax"></a>Sintassi


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Definizione* \[ di in\]
</dt> <dd>

Identifica un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) per cui verranno restituite le metriche.

</dd> <dt>

*Intervallo* \[ in\]
</dt> <dd>

Identifica la modalità di selezione delle istanze. L'algoritmo per l'ordinamento delle istanze di valore è specifico della definizione metrica.

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**Minimo** (2)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Massimo** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Specifico del fornitore** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Numero* \[ di in\]
</dt> <dd>

Identifica il numero massimo di istanze che devono essere restituite dal metodo.

</dd> <dt>

*Valori* \[ di out\]
</dt> <dd>

Al completamento del metodo, contiene riferimenti a istanze di [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md), filtrate in base ai valori dei parametri di input.

</dd> </dl>

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

 

 




