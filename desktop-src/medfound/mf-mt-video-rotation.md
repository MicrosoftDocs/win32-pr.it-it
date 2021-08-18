---
description: Specifica la rotazione di un fotogramma video in senso antiorario.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: MF_MT_VIDEO_ROTATION attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf3d909b29757a02d46cc842b30f04bfb0463d6f734eecb74bfb957fa206fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876701"
---
# <a name="mf_mt_video_rotation-attribute"></a>Attributo \_ MF MT \_ VIDEO \_ ROTATION

Specifica la rotazione di un fotogramma video in senso antiorario.

## <a name="data-type"></a>Tipo di dati

**MFVideoRotationFormat archiviato** come **UINT32**

## <a name="remarks"></a>Commenti

Il video di un dispositivo portatile, ad esempio un telefono cellulare, viene spesso ruotato di 90, 180 o 270 gradi. Se la fotocamera archivia l'orientamento come metadati nel file video, l'immagine può essere regolata al momento della riproduzione.

Se questo attributo è impostato su **MFVideoRotationFormat \_ 90,** significa che il contenuto è stato ruotato di 90 gradi in senso antiorario. Se il contenuto è stato ruotato di 90 gradi in senso orario, il valore dell'attributo sarà **MFVideoRotationFormat \_ 270.**

I valori supportati per questo attributo vengono enumerati in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tipi di supporti](media-types.md)
</dt> </dl>

 

 




