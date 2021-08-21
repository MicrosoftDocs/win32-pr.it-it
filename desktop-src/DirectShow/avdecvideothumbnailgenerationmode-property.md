---
description: Abilita o disabilita la modalità di generazione delle anteprime in un decodificatore video.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Proprietà AVDecVideoThumbnailGenerationMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb10b4996a88c8d2e62180edcbfaba8f71b6738d7dc7e3019a0b8ee4b44462d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159992"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>AVDecVideoThumbnailGenerationMode - proprietà

Abilita o disabilita la modalità di generazione delle anteprime in un decodificatore video.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>Commenti

Se il valore è **VARIANT \_ TRUE,** il decodificatore usa un'impostazione ottimizzata per generare rapidamente immagini di anteprima. Ad esempio, potrebbe ignorare i frame B o P. In caso contrario, se il valore è **VARIANT \_ FALSE,** il decodificatore usa le normali impostazioni di decodifica.

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

 

 




