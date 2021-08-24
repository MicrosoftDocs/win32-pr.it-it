---
description: Consente di restituire un elenco filtrato di istanze \_ baseMetricValue CIM.
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
ms.openlocfilehash: d010128bdef9bec4ce7df5fb3b1021a80a6ac99bdfbaf797958a76b27a812479
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695001"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a>Metodo GetMetricValues della classe \_ CIM MetricService

Consente di restituire un elenco filtrato di [**istanze \_ baseMetricValue CIM.**](cim-basemetricvalue.md)

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

*Definizione* \[ Pollici\]
</dt> <dd>

Identifica un [**oggetto CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) per il quale verranno restituite le metriche.

</dd> <dt>

*Intervallo* \[ Pollici\]
</dt> <dd>

Identifica la modalità di selezione delle istanze. L'algoritmo per l'ordinamento delle istanze di valore è specifico della definizione delle metriche.

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

**Specifico del** fornitore (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Conteggio* \[ Pollici\]
</dt> <dd>

Identifica il numero massimo di istanze restituite dal metodo .

</dd> <dt>

*Valori* \[ Cambio\]
</dt> <dd>

Al termine del metodo, contiene riferimenti a istanze di [**CIM \_ BaseMetricValue,**](cim-basemetricvalue.md)filtrate in base ai valori dei parametri di input.

</dd> </dl>

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

 

 




