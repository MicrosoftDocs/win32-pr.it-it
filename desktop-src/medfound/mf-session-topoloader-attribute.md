---
description: Contiene il CLSID di un caricatore di topologia per la sessione multimediale.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: MF_SESSION_TOPOLOADER attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9568193bbdbd46485015b6e5975db26fca2b552b23b7c227576e4e6544d69af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955131"
---
# <a name="mf_session_topoloader-attribute"></a>Attributo MF \_ SESSION \_ TOPOLOADER

Contiene il CLSID di un caricatore di topologia per la sessione multimediale.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

È possibile usare questo attributo per fornire un caricatore di topologia personalizzato per la sessione multimediale.

Impostare questo attributo usando il *parametro pConfiguration* della [**funzione MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**della funzione MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)

Se questo attributo è impostato, la sessione multimediale chiama **CoCreateInstance** con il CLSID specificato quando crea il caricatore della topologia. L'oggetto creato da questo CLSID deve esporre [**l'interfaccia IMFTopoLoader.**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)

Se questo attributo non è impostato, la sessione multimediale crea il caricatore di topologia predefinito fornito in Media Foundation.

Un caricatore di topologia deve supportare apartment multithreading. È necessario registrare il caricatore della topologia come ThreadingModel="Both". Inoltre, se si usa il caricatore della topologia all'interno del percorso del supporto protetto (PMP), il caricatore della topologia deve essere un componente attendibile. Per altre informazioni, vedere [Percorso del supporto protetto.](protected-media-path.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Attributi della sessione multimediale](media-session-attributes.md)
</dt> <dt>

[Caricatori di topologia personalizzati](custom-topology-loaders.md)
</dt> </dl>

 

 




