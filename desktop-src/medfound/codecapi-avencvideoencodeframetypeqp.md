---
description: Specifica i tipi di frame (I, P o B) a cui viene applicato il parametro di quantizzazione (QP).
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: CODECAPI_AVEncVideoEncodeFrameTypeQP proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ebd4a25f3779ce1c721eb3cb1188b487be4d313ae5dbeb02dd41e494f4c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743856"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a>CODECAPI \_ AVEncVideoEncodeFrameTypeQP - proprietà

Specifica i tipi di frame (I, P o B) a cui viene applicato il parametro di quantizzazione (QP).

## <a name="data-type"></a>Tipo di dati

**ULONGULONG** (INTERFACCIA UTENTE \_ VT8)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**

## <a name="remarks"></a>Commenti

Per i codificatori che supportano l'impostazione di un parametro di quantizzazione (QP) per tipi di fotogrammi diversi (I, P, B), devono esporre questa API oltre a [CODECAPI \_ AVEncVideoEncodeQP.](codecapi-avencvideoencodeqp.md) Se un codificatore supporta un solo QP per tutti i tipi di frame, deve supportare solo CODECAPI \_ AVEncVideoEncodeQP.

Si tratta di una proprietà di codifica dinamica che indica che è possibile impostare un nuovo valore in qualsiasi momento durante la sessione di codifica.

**Codificatori H.264/AVC:**

Il codificatore deve [**supportare GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Un set di quattro campi a 16 bit viene usato per specificare i QP dei frame nella codifica QP fissa. I campi sono:

-   **Bit da 0 a 15:** QP usato per i fotogrammi I, intervallo \[ valido 0, 51 \] .
-   **Bit 16-31:** QP usato per i fotogrammi P, intervallo \[ valido 0, 51 \] .
-   **Bit 32-47:** QP usato per i fotogrammi B, intervallo \[ valido 0, 51\]
-   **Bit 48-63:** riservato

Quando questo CodecAPI è supportato, i codificatori devono supportare l'impostazione QP nel tipo di frame I, P e B.

Il valore predefinito deve essere 0x0000001a001a001a. QP uguale a 26 per I, P e B.

Quando [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) seleziona un livello temporale specifico, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) di CODECAPI AVEncVideoEncodeFrameTypeQP imposta QP per i fotogrammi I, P e B su tale livello \_ temporale. Per impostazione predefinita, imposta QP per i fotogrammi I, P e B sul livello temporale 0 del livello temporale di base.

[CODECAPI \_ AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) e [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) devono essere usati per definire e limitare l'intervallo di domande e risposte per qp di tutti i tipi di immagine, I, P e B.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                   |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

