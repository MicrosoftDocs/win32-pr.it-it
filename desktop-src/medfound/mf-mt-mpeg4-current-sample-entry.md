---
description: Specifica la voce corrente nella casella Descrizione esempio per un tipo di supporto MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: Attributo MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315031"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>\_ \_ \_ \_ Attributo voce di esempio corrente MF mt MPEG4 \_

Specifica la voce corrente nella casella Descrizione esempio per un tipo di supporto MPEG-4.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

In un file MP4 o 3GP, nella casella Descrizione esempio viene descritta la codifica utilizzata per un flusso nel file. La casella Descrizione esempio può contenere più voci. Questo attributo specifica quale voce usare. Il valore è un indice in base zero nell'elenco.

Attualmente, l'unico valore supportato è 0. L'attributo è stato definito per l'estendibilità futura.

L'origine file MPEG-4 imposta sempre il valore su 0. I sink di file MP4 e 3GP ignorano il valore di questo attributo, se presente.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[\_Descrizione dell'esempio MF mt \_ MPEG4 \_ \_](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




