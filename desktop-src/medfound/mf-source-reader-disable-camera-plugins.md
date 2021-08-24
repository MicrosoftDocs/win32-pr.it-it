---
description: Disabilita l'uso dei plug-in della fotocamera di post-elaborazione da parte del lettore di origine.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66ae9c69d13b6af3e368b57a3f864f031d0cc7e63716d2267ae5d3869d102b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600291"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a>Attributo MF \_ SOURCE READER DISABLE CAMERA \_ \_ \_ \_ PLUGINS

Disabilita l'uso dei plug-in della fotocamera di post-elaborazione da parte del [lettore di origine.](source-reader.md)

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica quando il lettore di origine viene usato con un'origine di acquisizione video. Se questo attributo è **TRUE,** impedisce al lettore di origine di caricare i plug-in di post-elaborazione che la fotocamera potrebbe fornire. In caso contrario, per impostazione predefinita il lettore di origine li carica.

Il valore predefinito di questo attributo è **FALSE.** Impostare l'attributo quando si crea il lettore di origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




