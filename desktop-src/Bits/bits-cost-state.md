---
title: BITS_COST_STATE (Bits5 \_ 0.h)
description: L'enumerazione \_ BITS COST \_ STATE definisce i valori costanti che specificano lo stato di costo BITS.
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
ms.openlocfilehash: ecbe54966a54310af71a4c96a3d3c2423f524f9b8a8067b10350fba05675a54b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701981"
---
# <a name="bits_cost_state"></a>STATO DEI COSTI \_ DEI \_ BIT

Definisce costanti che specificano lo stato di costo BITS.

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**STATO DEI COSTI DEI BIT \_ \_ SENZA \_ RESTRIZIONI**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**UTILIZZO LIMITATO \_ DELLO STATO DEI COSTI \_ \_ \_ \_ BITS SCONOSCIUTO**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**STATO DEI COSTI DEI BIT \_ AL DI SOTTO DEL LIMITE \_ \_ \_ MASSIMO**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**STATO DEI COSTI DEI BIT \_ \_ VICINO AL \_ \_ LIMITE**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**ADDEBITO \_ \_ OVERCAP DELLO STATO \_ DEI COSTI IN \_ BIT**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**BITS \_ COST \_ STATE \_ OVERCAP \_ THROTTLED**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**BITS \_ COST \_ STATE \_ USAGE \_ BASED**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**OPZIONE BITS COST IGNORE CONGESTION (IGNORA \_ \_ \_ \_ CONGESTIONE)**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**STATO COSTO \_ BITS \_ \_ RISERVATO**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Riservato.


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**TRASFERIMENTO DELLO \_ STATO \_ DEI COSTI \_ BITS NON IN \_ \_ ROAMING**
</dt> <dd> <dl> <dt>

(BITS \_ OPZIONE COST IGNORE CONGESTION BITS COST STATE USAGE BASED \_ \_ \_ \| \_ \_ \_ \_ \| BITS \_ COST STATE COST \_ STATE \_ OVERCAP \_ THROTTLED BITS COST STATE \| \_ \_ \_ OVERCAP CHARGED \_ \| BITS COST STATE NEAR \_ CAP \_ \_ \_ \| BITS COST STATE BELOW \_ \_ CAP \_ \_ \| BITS COST STATE \_ \_ \_ CAPPED USAGE UNKNOWN \_ \_ \| BITS COST STATE \_ \_ \_ UNRESTRICTED) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**TRASFERIMENTO DELLO \_ STATO \_ DEI COSTI \_ \_ BITS SENZA \_ SUPPLEMENTO**
</dt> <dd> <dl> <dt>

(BITS \_ OPZIONE COST IGNORE CONGESTION BITS COST STATE USAGE BASED \_ \_ \_ \| \_ \_ \_ \_ \| BITS \_ COST STATE \_ \_ OVERCAP \_ THROTTLED \| BITS COST STATE NEAR \_ CAP \_ \_ \_ \| BITS COST STATE BELOW CAP BITS COST STATE \_ \_ \_ \_ \| \_ \_ \_ CAPPED \_ USAGE UNKNOWN \_ \| BITS COST STATE \_ \_ \_ UNRESTRICTED)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ STANDARD**
</dt> <dd> <dl> <dt>

(BITS \_ OPZIONE COST IGNORE CONGESTION BITS COST STATE USAGE BASED \_ \_ \_ \| \_ \_ \_ \_ \| BITS COST STATE \_ \_ \_ OVERCAP \_ THROTTLED \| BITS COST STATE \_ BELOW CAP \_ \_ \_ \| BITS COST STATE \_ \_ \_ CAPPED USAGE UNKNOWN \_ \_ \| BITS COST STATE \_ \_ \_ UNRESTRICTED) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**TRASFERIMENTO SENZA \_ RESTRIZIONI DELLO STATO DEI COSTI \_ \_ \_ BITS**
</dt> <dd> <dl> <dt>

(BITS \_ OPZIONE \_ COST IGNORE CONGESTION \_ \_ \| BITS COST STATE \_ \_ \_ OVERCAP \_ THROTTLED \| BITS COST STATE \_ \_ \_ UNRESTRICTED)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**TRASFERIMENTO DELLO \_ STATO DEI \_ COSTI \_ \_ BITS SEMPRE**
</dt> <dd> <dl> <dt>

(BITS \_ OPZIONE COST IGNORE CONGESTION BITS COST STATE ROAMING BITS COST STATE COST STATE USAGE BASED BITS COST STATE COST STATE \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ OVERCAP \_ THROTTLED BITS COST STATE OVERCAP CHARGED \| \_ \_ \_ \_ \| BITS \_ COST STATE NEAR \_ CAP \_ \_ \| BITS COST STATE BELOW \_ \_ CAP \_ \_ \| BITS COST STATE \_ \_ \_ CAPPED USAGE UNKNOWN \_ \_ \| BITS COST STATE \_ \_ \_ UNRESTRICTED)
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Bits5 \_ 0.h (include Bits.h)</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Bits5 \_ 0.idl</dt> </dl>                |



 

 





