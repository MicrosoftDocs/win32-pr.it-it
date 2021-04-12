---
description: Disabilita l'uso dei plug-in della fotocamera di post-elaborazione da parte del lettore di origine.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: Attributo MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233620"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a>\_Attributo MF Source \_ Reader \_ Disable \_ fotocamera \_ plugins

Disabilita l'uso dei plug-in della fotocamera di post-elaborazione da parte del [lettore di origine](source-reader.md).

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Questo attributo si applica quando il lettore di origine viene usato con un'origine di acquisizione video. Se questo attributo è **true**, impedisce al lettore di origine di caricare tutti i plug-in di post-elaborazione che potrebbero essere forniti dalla fotocamera. In caso contrario, per impostazione predefinita il lettore di origine li caricherà.

Il valore predefinito di questo attributo è **false**. Impostare l'attributo quando si crea il lettore di origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




