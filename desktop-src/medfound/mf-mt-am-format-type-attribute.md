---
description: Contiene un GUID del formato DirectShow per un tipo di supporto.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Attributo MF_MT_AM_FORMAT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344571"
---
# <a name="mf_mt_am_format_type-attribute"></a>\_ \_ \_ Attributo tipo di formato MF mt \_

Contiene un GUID del formato DirectShow per un tipo di supporto.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato quando un tipo di supporto DirectShow viene convertito in un tipo di supporto Media Foundation. L'attributo indica il tipo di formato DirectShow originale. Il valore corrisponde al membro formatType della struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Per un formato audio, l' [**attributo \_ \_ \_ dati utente MF mt**](mf-mt-user-data-attribute.md) può contenere il blocco di formato originale, se il tipo di formato DirectShow non è stato riconosciuto.

Non impostare questo attributo su un tipo di supporto a meno che non si converta una struttura del formato DirectShow.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Conversioni di tipi di supporto](media-type-conversions.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> <dt>

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MFCreateMediaTypeFromRepresentation**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
