---
description: Contiene la decodifica timestamp (DTS) per l'esempio.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Attributo MFSampleExtension_DecodeTimestamp (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309097"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>\_Attributo DecodeTimestamp di MFSampleExtension

Contiene la decodifica timestamp (DTS) per l'esempio.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Il valore dell'attributo è il DTS in unità 100-nanosecondi. DTS è definito in alcuni standard di codifica, incluso MPEG. Il DTS specifica quando l'immagine codificata deve essere decodificata. Se il video codificato contiene i frame B, DTS può differire dall'ora di presentazione, perché le immagini B appaiono fuori dall'ordine temporale nel bitstream.

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

[Attributi di esempio](sample-attributes.md)
</dt> </dl>

 

 




