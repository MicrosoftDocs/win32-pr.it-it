---
description: Fornisce un'interfaccia di callback per l'applicazione per ricevere un oggetto Enabler contenuto dalla sessione del percorso multimediale protetto (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: Attributo MF_SESSION_CONTENT_PROTECTION_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315012"
---
# <a name="mf_session_content_protection_manager-attribute"></a>\_Attributo MF Session \_ Content \_ Protection \_ Manager

Fornisce un'interfaccia di callback per l'applicazione per ricevere un oggetto Enabler contenuto dalla sessione del percorso multimediale protetto (PMP).

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFContentProtectionManager* *](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) dell'applicazione.

Impostare questo attributo nella sessione PMP utilizzando il parametro *pConfiguration* della funzione [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: Unknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Attributi della sessione multimediale](media-session-attributes.md)
</dt> <dt>

[Come riprodurre file multimediali protetti](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




