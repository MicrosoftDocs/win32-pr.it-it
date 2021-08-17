---
description: Specifica la voce corrente nella casella di descrizione dell'esempio per un tipo di supporto MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660f74c1f9335556b514607cc2100f7ef59a00fba84f6cfe90412b91e1ff500a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877035"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>Attributo MF \_ MT \_ MPEG4 \_ CURRENT SAMPLE \_ \_ ENTRY

Specifica la voce corrente nella casella di descrizione dell'esempio per un tipo di supporto MPEG-4.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

In un file MP4 o 3GP la casella di descrizione dell'esempio descrive la codifica usata per un flusso nel file. La casella della descrizione di esempio può contenere più voci. Questo attributo specifica la voce da usare. Il valore è un indice in base zero nell'elenco.

Attualmente, l'unico valore supportato è 0. L'attributo è stato definito per un'estendibilità futura.

L'origine file MPEG-4 imposta sempre il valore su 0. I sink di file MP4 e 3GP ignorano il valore di questo attributo, se presente.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[DESCRIZIONE \_ DELL'ESEMPIO \_ MPEG4 MF MT \_ \_](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




