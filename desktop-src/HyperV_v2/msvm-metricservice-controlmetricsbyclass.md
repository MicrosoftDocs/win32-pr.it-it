---
description: Controlla le metriche per classe.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Metodo ControlMetricsByClass della Msvm_MetricService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d522a2c66cf8b7127520fc3ec66b809c4e825cb759de116b3a3e820eb0ae676c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046531"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Metodo ControlMetricsByClass della classe Msvm \_ MetricService

Controlla le metriche per classe.

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

Identifica la classe CIM per cui verranno controllate le metriche.

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

Questo metodo restituisce uno dei valori seguenti:

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

 

 




