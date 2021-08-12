---
description: La tabella seguente contiene codici di errore specifici di Microsoft DirectX Media Objects (DMO). Questi codici di errore sono definiti nel file di intestazione Mediaerr.h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: DMO Codici di errore (Mediaerr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa8f45b8f9f61185adbcd79a354df8ab3e41471067b66179193b825a5e40651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653295"
---
# <a name="dmo-error-codes"></a>DMO Codici di errore

La tabella seguente contiene codici di errore specifici di Microsoft DirectX Media Objects (DMO). Questi codici di errore sono definiti nel file di intestazione Mediaerr.h.



| Costante/valore                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt> </dl> | Indice del flusso non valido.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ E \_ INVALIDTYPE**</dt> <dt>0x80040202</dt> </dl>                      | Tipo di supporto non valido.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ E \_ TYPE \_ NOT \_ SET**</dt> <dt>0x80040203</dt> </dl>                 | Tipo di supporto non impostato. Uno o più flussi richiedono un tipo di supporto prima di poter eseguire questa operazione.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt> </dl>                   | I dati non possono essere accettati in questo flusso. Potrebbe essere necessario elaborare più dati di output. vedere [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ E \_ TIPO \_ NON \_ ACCETTATO**</dt> <dt>0X80040205</dt> </dl>  | Tipo di supporto non accettato.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ E \_ NO MORE ITEMS \_ \_ 0x80040206**</dt> <dt></dt> </dl>              | L'indice di tipo media non è compreso nell'intervallo.<br/>                                                                                                                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mediaerr.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DMO Costanti](dmo-constants.md)
</dt> </dl>

 

 




