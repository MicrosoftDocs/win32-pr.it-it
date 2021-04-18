---
description: Specifica il numero di fotogrammi dopo il frame corrente che il codec valuterà prima di codificare il frame corrente.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: Proprietà MFPKEY_LOOKAHEAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310627"
---
# <a name="mfpkey_lookahead-property"></a>\_Proprietà lookahead di MFPKEY

Specifica il numero di fotogrammi dopo il frame corrente che il codec valuterà prima di codificare il frame corrente.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCLookAhead

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Quando il codec USA lookahead, può codificare il video in modo più efficiente.

L'oggetto writer di Windows Media Format SDK prevede che il codec Codifichi immediatamente ogni campione. Di conseguenza, questa funzionalità non funziona correttamente nel software che utilizza l'oggetto writer (incluso Windows Media Encoder e Windows Media Player). Tutte le estensioni di unità dati associate ai frame video verranno collegate al frame di output errato. Il numero di frame in base ai quali le estensioni dell'unità dati vengono posizionate in modo non corrispondente è uguale al numero di frame di lookahead utilizzati.

I valori lookahead validi sono compresi tra 0 e 16 frame. Il valore consigliato è 16.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




