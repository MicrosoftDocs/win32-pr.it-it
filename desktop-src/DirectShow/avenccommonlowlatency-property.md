---
description: Specifica se il flusso di output deve essere strutturato in modo che il flusso codificato abbia una bassa latenza di decodifica.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Proprietà AVEncCommonLowLatency (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b53c4b0122e595c930828f400600fc22b5a03977a781adab0e3a2f42b1048ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690231"
---
# <a name="avenccommonlowlatency-property"></a>AVEncCommonLowLatency - proprietà

Specifica se il flusso di output deve essere strutturato in modo che il flusso codificato abbia una bassa latenza di decodifica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonLowLatency**

## <a name="remarks"></a>Commenti

La latenza di decodifica è definita come la quantità di dati che il decodificatore deve buffer. Ad esempio, l'impostazione di questa proprietà su **VARIANT \_ TRUE** in un codificatore video MPEG limita i tipi di strutture GOP che il codificatore può usare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows app desktop di Windows 2000 Server \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




