---
description: Consente a due istanze della sessione multimediale di condividere lo stesso processo di percorso multimediale protetto (PMP).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Attributo MF_SESSION_SERVER_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131958"
---
# <a name="mf_session_server_context-attribute"></a>\_Attributo di \_ contesto del server di sessione MF \_

Consente a due istanze della sessione multimediale di condividere lo stesso processo di percorso multimediale protetto (PMP).

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="remarks"></a>Commenti

Usare questo attributo se si vuole creare la sessione multimediale PMP in un processo PMP esistente. Il valore dell'attributo è un puntatore all'interfaccia [_ *IMFPMPServer* *](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .

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
</dt> </dl>

 

 




