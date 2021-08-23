---
description: Consente al lettore di origine Media Foundation trasformazioni di destinazione (MFT) ottimizzate per la transcodificare.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc5362c93138ef301ac65ace799ad64d59ac9110af349822e0efa98d410686e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605018"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>MF \_ SOURCE READER ENABLE \_ \_ \_ TRANSCODE ONLY \_ \_ TRANSFORMS attribute

Consente al [lettore di](source-reader.md) origine Media Foundation trasformazioni di destinazione (MFT) ottimizzate per la transcodificare.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come booleano.

## <a name="remarks"></a>Commenti

Alcuni MFT, in particolare i decodificatori, sono ottimizzati per la transcodificare anziché per la riproduzione. Per impostazione predefinita, il lettore di origine non carica tali trasformazioni. Impostare questo attributo su **TRUE se** si vuole usare la transcodificare MFT con il lettore di origine.

Un'applicazione potrebbe impostare questo attributo se non elabora i dati in tempo reale (per la transcodizzazione o scenari simili). In caso contrario, per la riproduzione in tempo reale, usare il comportamento predefinito.

Internamente, questo attributo fa sì che il lettore di origine includa il flag **MFT \_ ENUM \_ FLAG \_ TRANSCODE \_ ONLY** quando chiama [**MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> </dl>

 

 




