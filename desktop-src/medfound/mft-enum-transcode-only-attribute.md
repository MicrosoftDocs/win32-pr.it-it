---
description: Specifica se un decodificatore è ottimizzato per la transcoding anziché per la riproduzione.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0951d4f370849678eb88ecbd9751c417a7e50d2bd709ad1f2c5b6cf96f5f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973080"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a>Attributo \_ MFT ENUM \_ TRANSCODE \_ ONLY \_ ATTRIBUTE

Specifica se un decodificatore è ottimizzato per la transcoding anziché per la riproduzione.

Attualmente, questo attributo si applica solo ai decodificatori basati su hardware che usano il mini driver AVStream. L'attributo viene archiviato nel Registro di sistema sotto le informazioni sulle funzionalità del decodificatore. Per altre informazioni, vedere la documentazione di [**IGetCapabilitiesKey.**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey)

Le applicazioni in genere non usano questo attributo.

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

Se questa voce del Registro di sistema è presente e uguale a 1, la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ignora il decodificatore a meno che il chiamante non ha specificato il flag **MFT \_ ENUM \_ FLAG \_ TRANSCODE \_ ONLY** in **MFTEnumEx**.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
