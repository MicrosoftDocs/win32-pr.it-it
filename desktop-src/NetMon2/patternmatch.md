---
description: La struttura PATTERNMATCH definisce gli elementi del criterio utilizzati per valutare un frame.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Struttura PATTERNMATCH (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967774"
---
# <a name="patternmatch-structure"></a>Struttura PATTERNMATCH

La struttura **PATTERNMATCH** definisce gli elementi del criterio utilizzati per valutare un frame.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a>Members

<dl> <dt>

**Flag**
</dt> <dd>

Flag di corrispondenza criterio:



| Valore                                                                                                                                                                                                                                                                                           | Significato                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <dt>**Modello \_ Flag di corrispondenza \_ \_ non**</dt> <dt>0x00000001</dt> </dl>                                   | Se impostato, questo flag mantiene i frame che non dispongono del modello specificato nella posizione corretta.<br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <dt>**Modello \_ \_Porta flag di corrispondenza \_ \_ specificata**</dt> <dt>0x00000008</dt> </dl> | Cerca un valore del numero di porta.<br/>                                                             |



 

</dd> <dt>

**OffsetBasis**
</dt> <dd>

Tipi di offset, che possono essere uno dei seguenti:



| Valore                                                                                                                                                                                                                                                       | Significato                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <dt>**OFFSET \_ \_ di base rispetto \_ al \_ frame**</dt> </dl>                                         | Imposta un offset, in byte, relativo all'inizio del frame.<br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <dt>**OFFSET \_ \_ di base \_ rispetto \_ al \_ protocollo effettivo**</dt> </dl> | Imposta un offset, in byte, relativo all'inizio del protocollo di riferimento.<br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <dt>**OFFSET \_ \_ di base rispetto \_ a \_ IPX**</dt> </dl>                                               | Imposta un offset, in byte, solo rispetto a IPX.<br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <dt>**OFFSET \_ \_ di base rispetto \_ all' \_ IP**</dt> </dl>                                                  | Imposta un offset, in byte, solo rispetto a IP.<br/>                              |



 

</dd> <dt>

**Porta**
</dt> <dd>

Valore della porta, se specificato.

</dd> <dt>

**Offset**
</dt> <dd>

Offset, in byte, relativo a **OffsetBasis**.

</dd> <dt>

**Length**
</dt> <dd>

Lunghezza del criterio corrispondente.

</dd> <dt>

**PatternToMatch**
</dt> <dd>

Criterio di corrispondenza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata per costruire un filtro di acquisizione. Per ulteriori informazioni sull'implementazione di questa struttura, vedere [Capture filters](capture-filters.md).

Un filtro di acquisizione può contenere fino a quattro strutture **PATTERNMATCH** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




