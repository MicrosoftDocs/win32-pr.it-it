---
description: Evento di modifica del catalogo Winsock per un'operazione di reimpostazione del catalogo Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET evento
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
ms.openlocfilehash: 3c9a638d962db908b24387d7baeb2f34d4e09ece561fdd1796a8a44930a5dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051289"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>EVENTO RESET DI WINSOCK \_ WS2HELP \_ LSP \_

> [!Note]  
> I provider di servizi su più livelli sono deprecati. A partire da Windows 8 e Windows Server 2012, usare [Windows Filtering Platform.](../fwp/windows-filtering-platform-start-page.md)

 

**L'evento RESET di WINSOCK \_ WS2HELP \_ LSP \_** è un evento di modifica del catalogo Winsock per un'operazione di reimpostazione del catalogo Winsock.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Catalogo* 
</dt> <dd>

Catalogo Winsock (a 32 bit o a 64 bit) da reimpostare. Si tratta di un valore intero che è 32 o 64.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'evento \_ WINSOCK WS2HELP \_ LSP \_ RESET** viene tracciato per un'operazione LSP (Layered Service Provider) Winsock quando il catalogo Winsock viene reimpostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo della traccia winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Traccia winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia di Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Dettagli traccia modifiche catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
