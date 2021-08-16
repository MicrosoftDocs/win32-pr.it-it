---
description: Usato per controllare la raccolta di metriche per uno o più elementi gestiti.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Metodo ControlMetrics della Msvm_MetricService classe
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
ms.openlocfilehash: 051a08f261432c817bc0e56cab323c56cd11935c1541c40357b6b151a14f4074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645847"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>Metodo ControlMetrics della classe Msvm \_ MetricService

Usato per controllare la raccolta di metriche per uno o più elementi gestiti.

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

Istanza [**CiM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che identifica gli elementi gestiti per i quali verranno raccolte le metriche. Se questo parametro è **Null,** verranno raccolte le  metriche per tutti gli elementi gestiti associati al parametro Definition.

</dd> <dt>

*Definizione* \[ Pollici\]
</dt> <dd>

Istanza [**di \_ BaseMetricDefinition msvm**](msvm-basemetricdefinition.md) che specifica quali metriche verranno raccolte. Se questo parametro è **Null,** verranno raccolte le metriche per  tutte le definizioni associate all'elemento gestito identificato dal parametro Subject

</dd> <dt>

*MetricCollectionEnabled* \[ Pollici\]
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

Disabilitare la raccolta delle metriche.

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimpostazione** (4)


</dt> <dd>

Reimpostare i valori delle metriche.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

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

## <a name="remarks"></a>Commenti

Questo metodo avrà esito negativo nelle istanze seguenti:

-   I *parametri Subject* e *Definition* sono **entrambi Null.**
-   I *parametri Subject* e *Definition* sono entrambi diversi da **Null** e non esiste un'istanza di [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md) che associa le due istanze.
-   Il *parametro Definition* è un riferimento a un'istanza di [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) non associata a [**Msvm \_ MetricService**](msvm-metricservice.md) tramite [**Msvm \_ ServiceAffectsElement.**](msvm-serviceaffectselement.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

