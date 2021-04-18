---
description: Flag del profilo che definiscono le impostazioni del flusso per la topologia transcodifica. I flag sono definiti nell'enumerazione dei \_ flag del profilo MF transcode \_ Adjust \_ \_ .
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: Attributo MF_TRANSCODE_ADJUST_PROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308430"
---
# <a name="mf_transcode_adjust_profile-attribute"></a>\_Attributo MF transcode \_ Adjust \_ profile

Flag del profilo che definiscono le impostazioni del flusso per la topologia transcodifica. I flag sono definiti nell'enumerazione [**dei \_ \_ \_ \_ flag del profilo MF transcode Adjust**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) .

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Un'applicazione può impostare questo attributo a livello di contenitore sul profilo transcodifica. Se questo attributo è impostato, la funzione [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) modifica gli attributi del flusso durante la compilazione della topologia, a seconda del flag specificato. Se, ad esempio, l'applicazione specifica il flag **\_ predefinito MF transcode \_ Adjust \_ profile \_** , per creare il profilo vengono usate le impostazioni di flusso specificate dall'applicazione.

Per il flusso video, la frequenza dei fotogrammi viene aggiornata in base all'origine del supporto. Se l'applicazione non specifica la modalità interlacciata, il profilo viene aggiornato in modo da usare i frame progressivi per impostazione predefinita.

Se l'applicazione specifica il flag **MF \_ transcode \_ Adjust \_ \_ use \_ source \_ Attributes** , gli attributi di flusso mancanti vengono copiati dall'origine del supporto di input nelle impostazioni del flusso nel profilo transcodifica.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API transcodifica](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




