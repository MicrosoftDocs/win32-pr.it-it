---
description: Specifica il numero di fotogrammi dopo il frame corrente che il codec valuterà prima di codificare il frame corrente.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: MFPKEY_LOOKAHEAD proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa5b11abbacc19a4a66dda785d628b1f5d67f636a0f02c7392402ad64a7c3926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113331"
---
# <a name="mfpkey_lookahead-property"></a>Proprietà LOOKAHEAD MFPKEY \_

Specifica il numero di fotogrammi dopo il frame corrente che il codec valuterà prima di codificare il frame corrente.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCLookAhead

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Quando il codec usa lookahead, può codificare il video in modo più efficiente.

L'oggetto writer di Windows Media Format SDK prevede che il codec codifica immediatamente ogni esempio. Di conseguenza, questa funzionalità non funziona correttamente nel software che usa l'oggetto writer (inclusi Windows Media Encoder e Windows Media Player). Tutte le estensioni di unità dati associate ai fotogrammi video verranno collegate al frame di output errato. Il numero di frame in base ai quali le estensioni delle unità dati vengono spostate in modo erto è uguale al numero di frame di lookahead usati.

I valori lookahead validi sono da 0 a 16 fotogrammi. Il valore consigliato è 16.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




