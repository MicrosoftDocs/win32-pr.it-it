---
description: La tabella seguente contiene i codici di errore specifici di Microsoft DirectX Media Objects (DMOs). Questi codici di errore sono definiti nel file di intestazione Mediaerr. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: Codici di errore DMO (Mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332865"
---
# <a name="dmo-error-codes"></a>Codici di errore DMO

La tabella seguente contiene i codici di errore specifici di Microsoft DirectX Media Objects (DMOs). Questi codici di errore sono definiti nel file di intestazione Mediaerr. h.



| Costante/valore                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt> </dl> | Indice del flusso non valido.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ E \_ INVALIDTYPE**</dt> <dt>0x80040202</dt> </dl>                      | Tipo di supporto non valido.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ \_Tipo E \_ non \_ impostato**</dt> <dt>0x80040203</dt> </dl>                 | Il tipo di supporto non è stato impostato. Uno o più flussi richiedono un tipo di supporto prima di poter eseguire questa operazione.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt> </dl>                   | Non è possibile accettare i dati nel flusso. Potrebbe essere necessario elaborare altri dati di output; vedere [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ \_Tipo E \_ non \_ accettato**</dt> <dt>0x80040205</dt> </dl>  | Il tipo di supporto non è stato accettato.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ E \_ nessun \_ altro \_ elemento**</dt> <dt>0x80040206</dt> </dl>              | Indice del tipo di supporto non compreso nell'intervallo.<br/>                                                                                                                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mediaerr. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DMO](dmo-constants.md)
</dt> </dl>

 

 




