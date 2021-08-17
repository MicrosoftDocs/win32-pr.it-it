---
description: Crea un punto di riferimento di una raccolta di sistemi virtuali.
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Metodo CreateReferencePoint della classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e1745a02b643f035dd46d82e1686a8f5075157a7f749a701865028f3a7db162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117994802"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Metodo CreateReferencePoint della classe Msvm \_ CollectionReferencePointService

Crea un punto di riferimento di una raccolta di sistemi virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Raccolta* \[ Pollici\]
</dt> <dd>

Riferimento alla raccolta di sistemi virtuali interessata.

</dd> <dt>

*ReferencePointSettings* \[ Pollici\]
</dt> <dd>

Impostazioni dei parametri.

</dd> <dt>

*ReferencePointType* \[ Pollici\]
</dt> <dd>

Indica il tipo del punto di riferimento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basato su** log (1)


</dt> <dd>

Rilevamento dei log della replica Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basato su RCT** (2)


</dt> <dd>

In base alla Rilevamento modifiche resiliente dei dischi virtuali.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del** fornitore (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingReferencePointCollection* \[ in, out\]
</dt> <dd>

Punto di riferimento risultante di una raccolta di sistemi virtuali.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione è a esecuzione lunga, facoltativamente può essere restituito un processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, restituisce 0 (nessun errore) o 4096 (processo avviato); In caso contrario, restituisce un errore.

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

[**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




