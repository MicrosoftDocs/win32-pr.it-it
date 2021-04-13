---
description: Specifica se un decodificatore è ottimizzato per la transcodifica anziché per la riproduzione.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: Attributo MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401690"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a>\_ \_ \_ Attributo attributo solo transcodifica dell'enumerazione MFT \_

Specifica se un decodificatore è ottimizzato per la transcodifica anziché per la riproduzione.

Attualmente, questo attributo si applica solo ai decodificatori basati su hardware che usano il mini driver AVStream. L'attributo viene archiviato nel registro di sistema nelle informazioni sulle funzionalità del decodificatore. Per ulteriori informazioni, vedere la documentazione relativa a [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).

Le applicazioni in genere non utilizzano questo attributo.

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

Se questa voce del registro di sistema è presente e uguale a 1, la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ignora il decodificatore, a meno che il chiamante non abbia specificato il flag di **\_ enumerazione MFT \_ flag \_ transcode \_ only** in **MFTEnumEx**.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
