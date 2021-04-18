---
description: Usato per controllare la raccolta di metriche per un elemento o elementi gestiti.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Metodo ControlMetrics della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314356"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>Metodo ControlMetrics della classe MSVM \_ MetricService

Usato per controllare la raccolta di metriche per un elemento o elementi gestiti.

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

*Oggetto* \[ in\]
</dt> <dd>

Istanza di [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che identifica gli elementi gestiti per i quali verranno raccolte le metriche. Se questo parametro è **null**, verranno raccolte le metriche per tutti gli elementi gestiti associati al parametro *Definition* .

</dd> <dt>

*Definizione* \[ di in\]
</dt> <dd>

Istanza di [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) che specifica le metriche che verranno raccolte. Se questo parametro è **null**, vengono raccolte le metriche per tutte le definizioni associate all'elemento gestito identificato dal parametro *Subject*

</dd> <dt>

*MetricCollectionEnabled* \[ in\]
</dt> <dd>

Specifica l'operazione da eseguire sulla raccolta di metriche. Deve essere uno dei valori seguenti.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Abilita** (2)


</dt> <dd>

Abilitare la raccolta di metriche.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** (3)


</dt> <dd>

Disabilitare la raccolta di metriche.

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (4)


</dt> <dd>

Reimposta i valori delle metriche.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)


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

## <a name="remarks"></a>Commenti

Questo metodo avrà esito negativo nelle istanze seguenti:

-   I parametri *Subject* e *Definition* sono entrambi **null**.
-   I parametri *Subject* e *Definition* sono entrambi non **null** e non è disponibile un'istanza di [**MSVM \_ MetricDefForME**](msvm-metricdefforme.md) che associ le due istanze.
-   Il parametro della *definizione* è un riferimento a un'istanza di [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) che non è associata a [**MSVM \_ MetricService**](msvm-metricservice.md) tramite [**MSVM \_ ServiceAffectsElement**](msvm-serviceaffectselement.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_MetricService MSVM**](msvm-metricservice.md)
</dt> </dl>

 

