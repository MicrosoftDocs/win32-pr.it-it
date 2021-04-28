---
description: 'Metodo ControlMetricsByClass della CIM_MetricService: abilita e disabilita la raccolta di metriche.'
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: Metodo ControlMetricsByClass della CIM_MetricService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fda8407d49ed3eec7ff86abc94ced6b63d2d77c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109709"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a>Metodo ControlMetricsByClass della classe \_ CIM MetricService

Abilita e disabilita la raccolta di metriche. **ControlMetricsByClass** viene usato per controllare la raccolta di ogni tipo di metrica per tutte le istanze di una classe o la raccolta di una metrica specifica per tutte le istanze di una classe.

## <a name="syntax"></a>Sintassi


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Oggetto* \[ Pollici\]
</dt> <dd>

Identifica la [**classe CIM \_ ManagedElement**](cim-managedelement.md) per cui verranno controllate le metriche.

</dd> <dt>

*Definizione* \[ Pollici\]
</dt> <dd>

Identifica una [**\_ baseMetricDefinition CIM**](cim-basemetricdefinition.md) per cui verranno controllate le metriche.

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

**Reimposta** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DmTF riservato** (..)


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
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




