---
description: Contiene il CLSID di un caricatore della topologia per la sessione multimediale.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: Attributo MF_SESSION_TOPOLOADER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318056"
---
# <a name="mf_session_topoloader-attribute"></a>\_Attributo TOPOLOADER della sessione MF \_

Contiene il CLSID di un caricatore della topologia per la sessione multimediale.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

È possibile usare questo attributo per fornire un caricatore di topologia personalizzato per la sessione multimediale.

Impostare questo attributo utilizzando il parametro *pConfiguration* della funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o la funzione [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Se questo attributo è impostato, la sessione multimediale chiama **CoCreateInstance** con il CLSID specificato quando crea il caricatore della topologia. L'oggetto creato da questo CLSID deve esporre l'interfaccia [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .

Se questo attributo non è impostato, la sessione multimediale crea il caricatore della topologia predefinito fornito in Media Foundation.

Un caricatore di topologia deve supportare gli Apartment A thread multipli. È necessario registrare il caricatore della topologia come ThreadingModel = "both". Inoltre, se si usa il caricatore della topologia all'interno del percorso multimediale protetto (PMP), il caricatore della topologia deve essere un componente attendibile. Per altre informazioni, vedere [percorso multimediale protetto](protected-media-path.md).

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

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Attributi della sessione multimediale](media-session-attributes.md)
</dt> <dt>

[Caricatori topologia personalizzati](custom-topology-loaders.md)
</dt> </dl>

 

 




