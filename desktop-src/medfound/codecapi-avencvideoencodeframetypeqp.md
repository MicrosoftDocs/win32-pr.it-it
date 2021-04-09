---
description: Specifica i tipi di frame (I, P o B) a cui viene applicato il parametro di quantizzazione (QP).
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: Proprietà CODECAPI_AVEncVideoEncodeFrameTypeQP (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127975"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a>Proprietà AVEncVideoEncodeFrameTypeQP di codecapi \_

Specifica i tipi di frame (I, P o B) a cui viene applicato il parametro di quantizzazione (QP).

## <a name="data-type"></a>Tipo di dati

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoEncodeFrameTypeQP**

## <a name="remarks"></a>Commenti

Per i codificatori che supportano l'impostazione di un parametro di quantizzazione (QP) per diversi tipi di frame (I, P, B), devono esporre questa API oltre a [CODEcapite \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md). Se un codificatore supporta solo un singolo QP per tutti i tipi di frame, dovrà supportare solo codecapite \_ AVEncVideoEncodeQP.

Si tratta di una proprietà di codifica dinamica che indica che è possibile impostare un nuovo valore in qualsiasi momento durante la sessione di codifica.

**Codificatori H. 264/AVC:**

Il codificatore deve supportare [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Un set di campi a 4 16 bit viene usato per specificare il frame query al secondo nella codifica Fixed-QP. I campi sono:

-   **Bits 0-15:** QP usato per I frame I, intervallo valido \[ 0, 51 \] .
-   **Bits 16-31:** QP usato per i frame P, intervallo valido \[ 0, 51 \] .
-   **Bits 32-47:** QP utilizzato per i frame B, intervallo valido \[ 0, 51\]
-   **Bits 48-63:** riservato

Quando questo codecapi è supportato, I codificatori supporteranno le impostazioni di QP per il tipo di frame I, P e B.

Il valore predefinito deve essere 0x0000001a001a001a. QP uguale a 26 per I, P e B.

Quando [CODEcapites \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) seleziona un livello temporale specifico, il [**valore**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) di codecapites \_ AVEncVideoEncodeFrameTypeQP imposta QP per i frame I, P e B su tale livello temporale. Per impostazione predefinita, imposta la query QP per I frame I, P e B sul livello temporale di base livello temporale 0.

[CODEcapi \_ ](codecapi-avencvideomaxqp.md)Per definire e limitare l'intervallo di QP per query al secondo di tutti i tipi di immagine, i, P e B, è necessario usare AVEncVideoMaxQP e [codecapit \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                   |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

