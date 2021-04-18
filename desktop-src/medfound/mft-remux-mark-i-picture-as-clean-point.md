---
description: Specifica se il video H. 264 remux MFT dovrebbe contrassegnare le immagini come punto di pulitura per una migliore capacità di ricerca. Questo può causare danneggiamenti nelle ricerche in file MP4 finali non conformi.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: Attributo MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310210"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a>\_ \_ Immagine di REMUX di MFT contrassegnata \_ \_ \_ come \_ \_ attributo punto di pulizia

Specifica se il video H. 264 remux MFT dovrebbe contrassegnare le immagini come punto di pulitura per una migliore capacità di ricerca. Questo può causare danneggiamenti nelle ricerche in file MP4 finali non conformi.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

L'immagine del punto di pulizia deve essere compressa IDR immagini per definizione.

Questa operazione non è consigliata per la registrazione o la remuxing di file MP4, a meno che tale esercizio non produca alcuni file pseudo-MP4 intermedi per la modifica dei video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




