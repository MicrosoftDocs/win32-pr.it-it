---
description: 'Metodo ControlMetrics della classe CIM_MetricService: abilita e disabilita la raccolta di metriche.'
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Metodo ControlMetrics della CIM_MetricService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 19e732e50f8c367463e7f528a520a736117999b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090869"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a>Metodo ControlMetrics della classe \_ CIM MetricService

Abilita e disabilita la raccolta di metriche. **ControlMetrics** viene usato per controllare la raccolta di ogni tipo di metrica per un Elemento gestito [**CIM, \_**](cim-managedelement.md)la raccolta di un determinato tipo di metrica per tutti gli elementi gestiti o la raccolta di una metrica specifica per un elemento gestito specifico.

## <a name="syntax"></a>Sintassi


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Oggetto* \[ Pollici\]
</dt> <dd>

[**ManagedElement \_ CIM**](cim-managedelement.md) che identifica gli elementi gestiti per i quali verranno controllate le metriche.

</dd> <dt>

*Definizione* \[ Pollici\]
</dt> <dd>

Identifica un [**oggetto \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) per il quale verranno controllate le metriche.

</dd> <dt>

*MetricCollectionEnabled* \[ Pollici\]
</dt> <dd>

Indica l'operazione desiderata da eseguire sulle metriche.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Abilita** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Disabilita** (3)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Reimpostazione** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

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
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




