---
description: Consente al lettore di origine di utilizzare le trasformazioni di Media Foundation (MFTs) ottimizzate per la transcodifica.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: Attributo MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525992"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>MF \_ source \_ Reader \_ Abilita l' \_ attributo TRANScode \_ only \_ Transformations

Consente al [lettore di origine](source-reader.md) di utilizzare le trasformazioni di Media Foundation (MFTS) ottimizzate per la transcodifica.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Alcuni MFTs, in particolare i decodificatori, sono ottimizzati per la transcodifica anziché per la riproduzione. Per impostazione predefinita, il lettore di origine non caricherà tali trasformazioni. Impostare questo attributo su **true** se si desidera utilizzare la transcodifica di MFTS con il lettore di origine.

Un'applicazione potrebbe impostare questo attributo se non elabora i dati in tempo reale (per la transcodifica o scenari simili). In caso contrario, per la riproduzione in tempo reale, utilizzare il comportamento predefinito.

Internamente, questo attributo fa in modo che il lettore di origine includa il flag del **\_ flag enum di enumerazione MFT \_ \_ \_ solo** quando chiama [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

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

[Lettore di origine](source-reader.md)
</dt> </dl>

 

 




