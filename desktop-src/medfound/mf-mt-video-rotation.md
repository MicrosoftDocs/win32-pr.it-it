---
description: Specifica la rotazione di un frame video in senso antiorario.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: Attributo MF_MT_VIDEO_ROTATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885581"
---
# <a name="mf_mt_video_rotation-attribute"></a>\_ \_ Attributo rotazione video MF mt \_

Specifica la rotazione di un frame video in senso antiorario.

## <a name="data-type"></a>Tipo di dati

**MFVideoRotationFormat** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Il video da un dispositivo palmare, ad esempio un telefono cellulare, viene spesso ruotato di 90, 180 o 270 gradi. Se la fotocamera archivia l'orientamento come metadati nel file video, l'immagine può essere regolata al momento della riproduzione.

Se questo attributo è impostato su **MFVideoRotationFormat \_ 90**, significa che il contenuto è stato ruotato di 90 gradi in senso antiorario. Se il contenuto è stato ruotato di 90 gradi in senso orario, il valore dell'attributo sarà **MFVideoRotationFormat \_ 270**.

I valori supportati per questo attributo sono enumerati in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 




