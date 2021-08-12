---
description: Contiene il timestamp di decodifica (DTS) per l'esempio.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: MFSampleExtension_DecodeTimestamp attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d72ea69f487efe24148fa8ce60ad05eb7a124673f02a78e70c67f604a51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241482"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>Attributo \_ DecodeTimestamp MFSampleExtension

Contiene il timestamp di decodifica (DTS) per l'esempio.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Il valore dell'attributo è DTS in unità da 100 nanosecondi. Il DTS è definito in alcuni standard di codifica, incluso MPEG. DTS specifica quando deve essere decodificata l'immagine codificata. Se il video codificato contiene fotogrammi B, il DTS può differire dall'ora di presentazione, perché le immagini B vengono visualizzate in ordine temporale nel flusso di bit.

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

[Attributi di esempio](sample-attributes.md)
</dt> </dl>

 

 




