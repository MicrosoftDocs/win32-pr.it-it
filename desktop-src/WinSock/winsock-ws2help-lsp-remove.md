---
description: Evento di modifica del catalogo Winsock per un'operazione di rimozione di un provider di servizi a livelli (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: WINSOCK_WS2HELP_LSP_REMOVE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: b0ac13a5404dcbbfe5fb5f5d8c2a5f17d43edeb72ba135abfc7e85ad9e5227a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321593"
---
# <a name="winsock_ws2help_lsp_remove-event"></a>EVENTO REMOVE DI WINSOCK \_ WS2HELP \_ LSP \_

> [!Note]  
> I provider di servizi su più livelli sono deprecati. A partire da Windows 8 e Windows Server 2012, usare [Windows Filtering Platform.](../fwp/windows-filtering-platform-start-page.md)

 

**L'evento REMOVE di WINSOCK \_ WS2HELP \_ LSP \_** è un evento di modifica del catalogo Winsock per un'operazione di rimozione di un provider di servizi a livelli (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome LSP* 
</dt> <dd>

Nome dell'LSP ottenuto dal membro **szProtocol** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP da rimuovere.

</dd> <dt>

*Catalogo* 
</dt> <dd>

Catalogo Di Winsock (a 32 bit o a 64 bit) in cui viene rimosso il provider di servizi di rete. Si tratta di un valore intero che è 32 o 64.

</dd> <dt>

*Programma di installazione* 
</dt> <dd>

Nome del modulo dell'applicazione che effettua la chiamata di rimozione dell'LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valore GUID del provider di trasporto Winsock da cui viene rimosso l'LSP.

</dd> <dt>

*Categoria* 
</dt> <dd>

Membro **dwCatalogEntryId** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP da rimuovere.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'evento REMOVE di WINSOCK \_ WS2HELP \_ LSP \_** viene tracciato per un'operazione di rimozione LSP quando viene rimossa una voce di protocollo dal catalogo Winsock.

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

 

 
