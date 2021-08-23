---
description: Specifica l'impostazione predefinita per il bit originale nel flusso audio MPEG-1. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Proprietà AVEncMPAOriginalBitstream (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d39b34339e25d08b138fd1c55a64e8a84d6cf4b4db302cbab1e5f50b8ccebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689741"
---
# <a name="avencmpaoriginalbitstream-property"></a>AVEncMPAOriginalBitstream - proprietà

Specifica l'impostazione predefinita per il bit originale nel flusso audio MPEG-1. Questa proprietà si applica ai codificatori audio MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncMPAOriginalBitstream**

## <a name="property-value"></a>Valore proprietà

Questa proprietà può avere i valori seguenti.



| Valore          | Descrizione          |
|----------------|----------------------|
| VARIANT \_ FALSE | Il bit originale è disattivato. |
| VARIANT \_ TRUE  | Il bit originale è on.  |



 

## <a name="remarks"></a>Commenti

Il codificatore potrebbe eseguire l'override di questa impostazione, in base al contenuto del flusso di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server desktop apps UWP apps (App desktop UWP di Windows 2000 \[ \| Server)\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




