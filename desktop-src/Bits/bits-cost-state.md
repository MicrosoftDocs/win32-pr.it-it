---
title: BITS_COST_STATE (Bits5 \_ 0. h)
description: L' \_ enumerazione di stato dei costi bits \_ definisce i valori costanti che specificano lo stato del costo BITS.
ms.assetid: A8C36D4E-98B3-45C4-9ECD-9B5280133176
topic_type:
- apiref
api_name:
- BITS_COST_STATE_UNRESTRICTED
- BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
- BITS_COST_STATE_BELOW_CAP
- BITS_COST_STATE_NEAR_CAP
- BITS_COST_STATE_OVERCAP_CHARGED
- BITS_COST_STATE_OVERCAP_THROTTLED
- BITS_COST_STATE_USAGE_BASED
- BITS_COST_OPTION_IGNORE_CONGESTION
- BITS_COST_STATE_RESERVED
- BITS_COST_STATE_TRANSFER_NOT_ROAMING
- BITS_COST_STATE_TRANSFER_NO_SURCHARGE
- BITS_COST_STATE_TRANSFER_STANDARD
- BITS_COST_STATE_TRANSFER_UNRESTRICTED
- BITS_COST_STATE_TRANSFER_ALWAYS
api_location:
- Bits5_0.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/20/2019
ms.openlocfilehash: 88fb0b949fb06a6e1eb6e14cdf55c8d54d9ab33c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964338"
---
# <a name="bits_cost_state"></a>\_stato costo \_ BITS

Definisce le costanti che specificano lo stato del costo BITS.

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**\_stato costo \_ bits \_ senza restrizioni**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**\_ \_ \_ utilizzo limitato stato costo bits \_ \_ sconosciuto**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**\_stato costo \_ bits \_ sotto \_ Cap**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**\_stato di costo bits \_ \_ vicino al \_ limite**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**\_ \_ cappuccio stato costo \_ bits \_ addebitato**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**\_cappuccio stato di costo bits \_ \_ \_ limitato**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**\_ \_ \_ basato sull'utilizzo dello stato di costo bits \_**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**\_opzione costo bits- \_ \_ Ignora \_ congestione**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**\_stato costo \_ bits \_ riservato**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Riservato.


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**\_ \_ trasferimento stato costo BITS non in \_ \_ \_ roaming**
</dt> <dd> <dl> <dt>

(BITS \_ opzione di costo ignora lo stato di costo dei bit per la gestione dello stato dei costi di bit cappuccio limitazione delle richieste in base allo stato del costo di bit costo cappuccio costo bits per lo stato di costo dei bit di \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ riduzione \_ utilizzo \_ \| \_ \_ \_ limitato 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**\_ \_ trasferimento stato costo \_ bits \_ senza \_ supplemento**
</dt> <dd> <dl> <dt>

(BITS \_ opzione di costo ignora lo stato di costo bit per l' \_ \_ \_ \| \_ \_ utilizzo dello stato \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ di costo bits cappuccio per lo stato di costo limitato in base al costo dei bit limite per lo stato dei costi di bit limitato utilizzo ridotto stato costo bit sconosciuto
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**\_standard di \_ trasferimento dello stato dei costi \_ bits \_**
</dt> <dd> <dl> <dt>

(BITS \_ opzione di costo ignora lo stato dei costi di costo bits per l'utilizzo dello stato di costo bits cappuccio in stato di costo bit limitato stato di costo bit di \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ riduzione \_ utilizzo \_ \| \_ \_ \_ limite stato costo bit sconosciuto 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**\_ \_ trasferimento stato costo \_ bits \_ senza restrizioni**
</dt> <dd> <dl> <dt>

(BITS \_ opzione di costo ignora lo stato dei costi per i \_ \_ bit di \_ congestione \| \_ \_ \_ cappuccio limitazione dello \_ \| \_ \_ stato \_ dei costi BITS.
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**\_ \_ trasferimento stato costo \_ bits \_ sempre**
</dt> <dd> <dl> <dt>

(BITS \_ opzione di costo ignora lo stato dei costi bits di congestione dei costi bits per lo stato dei costi bits cappuccio in base allo stato di costo bits costo di bit di costo cappuccio in stato di costo dei bit di costo \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ inferiore \_ \| \_ \_ \_ \_ utilizzo \_ \| \_ \_ \_ limitato stato costi bit sconosciuto
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Bits5 \_ 0. h (include BITS. h)</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Bits5 \_ 0. idl</dt> </dl>                |



 

 





