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
ms.openlocfilehash: fdcf4680ff10bdc8135fae4ec3bb9f81d53c26092e7196e73965ee4f4d87991f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014479"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Metodo CreateReferencePoint della classe Msvm \_ VirtualSystemReferencePointService

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

*AffectedSystem* \[ Pollici\]
</dt> <dd>

ComputerSystem [**Msvm \_ che**](msvm-computersystem.md) fa riferimento al sistema virtuale interessato.

</dd> <dt>

*ReferencePointSettings* \[ Pollici\]
</dt> <dd>

Contiene le impostazioni dei parametri.

</dd> <dt>

*ReferencePointType* \[ Pollici\]
</dt> <dd>

Tipo di punto di riferimento richiesto:

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basato su** log (0)


</dt> <dd>

In base al rilevamento dei log della replica Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basato su RCT** (1)


</dt> <dd>

In base alla Rilevamento modifiche resiliente dei dischi virtuali.

</dd> </dl> </dd> <dt>

*ResultingReferencePoint* \[ in, out\]
</dt> <dd>

Punto di riferimento del sistema virtuale risultante

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione è a esecuzione lunga, facoltativamente può essere restituito un processo. In questo caso, l'istanza della classe [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) che rappresenta il nuovo punto di riferimento del sistema virtuale viene presentata tramite l'associazione [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) al valore della proprietà **AffectedElement** che fa riferimento alla nuova istanza della classe **Msvm \_ VirtualSystemReferencePoint** che rappresenta il punto di riferimento del sistema virtuale e il valore di **ElementEffects** impostato su 5 (Create).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0; In caso contrario, restituisce un errore.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Tipo non valido** (6)
</dt> <dt>

**DmTF Reserved** (..)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




