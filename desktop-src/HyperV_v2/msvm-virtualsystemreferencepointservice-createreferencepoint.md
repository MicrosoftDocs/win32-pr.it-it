---
description: Crea un punto di riferimento di un sistema virtuale.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Metodo CreateReferencePoint della classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320630"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Metodo CreateReferencePoint della classe MSVM \_ VirtualSystemReferencePointService

Crea un punto di riferimento di un sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedSystem* \[ in\]
</dt> <dd>

Un [**\_ ComputerSystem MSVM**](msvm-computersystem.md) che fa riferimento al sistema virtuale interessato.

</dd> <dt>

*ReferencePointSettings* \[ in\]
</dt> <dd>

Contiene le impostazioni dei parametri.

</dd> <dt>

*ReferencePointType* \[ in\]
</dt> <dd>

Tipo di punto di riferimento richiesto:

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basato su log** (0)


</dt> <dd>

In base al rilevamento del log della replica Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basato su RCT** (1)


</dt> <dd>

Basato su Rilevamento modifiche resiliente di dischi virtuali.

</dd> </dl> </dd> <dt>

*ResultingReferencePoint* \[ in uscita\]
</dt> <dd>

Punto di riferimento del sistema virtuale risultante

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo. In questo caso, l'istanza della classe [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) che rappresenta il nuovo punto di riferimento del sistema virtuale viene presentata tramite l'associazione [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) con il valore della proprietà **affected** che fa riferimento alla nuova istanza della classe **MSVM \_ VirtualSystemReferencePoint** che rappresenta il punto di riferimento del sistema virtuale e il valore di **ElementEffects** impostato su 5 (Create).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0; in caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Tipo non valido** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualSystemReferencePointService MSVM**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




