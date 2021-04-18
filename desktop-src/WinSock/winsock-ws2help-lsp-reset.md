---
description: Evento di modifica del catalogo Winsock per un'operazione di reimpostazione del catalogo Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: Evento WINSOCK_WS2HELP_LSP_RESET
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315750"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>\_Evento di \_ reimpostazione di Winsock ws2help LSP \_

> [!Note]  
> I provider di servizi sovrapposti sono deprecati. A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

L'evento di **\_ \_ \_ reimpostazione di Winsock ws2help LSP** è un evento di modifica del catalogo Winsock per un'operazione di reimpostazione del catalogo Winsock.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Catalogo* 
</dt> <dd>

Il catalogo Winsock (32 bit o 64 bit) che viene reimpostato. Si tratta di un valore intero che può essere 32 o 64.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'evento di **\_ \_ \_ reimpostazione di Winsock ws2help LSP** viene tracciato per un'operazione LSP (Layered Service Provider) Winsock quando viene reimpostato il catalogo Winsock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo della traccia Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Traccia Winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Dettagli della traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
