---
description: Specifica che l'origine del supporto verrà creata in un processo remoto.
ms.assetid: 3a2f9ff5-1780-40f3-b36b-3a7cccb47d05
title: Attributo MF_SESSION_REMOTE_SOURCE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27b26a71e8bea53ab687eaf6126a1803e71ba16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232529"
---
# <a name="mf_session_remote_source_mode-attribute"></a>\_ \_ \_ Attributo modalità origine remota della sessione MF \_

Specifica che l'origine del supporto verrà creata in un processo remoto.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

È possibile impostare questo attributo sulla sessione del percorso multimediale protetto (PMP) utilizzando il parametro *pConfiguration* della funzione [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Attributi della sessione multimediale](media-session-attributes.md)
</dt> <dt>

[Sessione multimediale PMP](pmp-media-session.md)
</dt> </dl>

 

 




