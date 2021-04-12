---
description: Contiene il CLSID di un gestore qualità per la sessione multimediale.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: Attributo MF_SESSION_QUALITY_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346656"
---
# <a name="mf_session_quality_manager-attribute"></a>\_Attributo MF Session \_ Quality \_ Manager

Contiene il CLSID di un gestore qualità per la sessione multimediale.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

È possibile usare questo attributo per fornire un gestore di qualità personalizzato per la sessione multimediale.

Impostare questo attributo utilizzando il parametro *pConfiguration* della funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Se questo attributo è impostato, la sessione multimediale chiama **CoCreateInstance** con il CLSID specificato per creare il gestore qualità. L'oggetto creato da questo CLSID deve esporre l'interfaccia [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .

Se questo attributo non è impostato, la sessione multimediale crea il gestore qualità predefinito fornito in Media Foundation.

Se si vuole eseguire la sessione multimediale senza alcun gestore qualità, impostare questo attributo su **GUID \_ null**.

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
</dt> </dl>

 

 




