---
description: Abilita o Disabilita la modalità di generazione di anteprime in un decodificatore video.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Proprietà AVDecVideoThumbnailGenerationMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965825"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>Proprietà AVDecVideoThumbnailGenerationMode

Abilita o Disabilita la modalità di generazione di anteprime in un decodificatore video.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>Commenti

Se il valore è **Variant \_ true**, il decodificatore usa un'impostazione ottimizzata per generare rapidamente immagini di anteprima. (Ad esempio, potrebbe ignorare i frame B o P). In caso contrario, se il valore è **Variant \_ false**, il decodificatore utilizza le impostazioni di decodifica normali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




