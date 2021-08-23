---
description: Evento di modifica del catalogo Winsock per un'operazione di disabilitazione del provider di servizi a più livelli (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 578479710856e149760202699be13d4b30b50709f6ea9b389e055793a8b0ca94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733131"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>Evento DISABLE di WINSOCK \_ WS2HELP \_ LSP \_

> [!Note]  
> I provider di servizi a più livelli sono deprecati. A partire da Windows 8 e Windows Server 2012, usare [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).

 

**L'evento DISABLE di WINSOCK \_ WS2HELP \_ LSP \_** è un evento di modifica del catalogo Winsock per un'operazione di disabilitazione del provider di servizi a più livelli (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome LSP* 
</dt> <dd>

Nome dell'LSP ottenuto dal membro **szProtocol** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP disabilitato.

</dd> <dt>

*Catalogo* 
</dt> <dd>

Catalogo Winsock (a 32 o 64 bit) in cui l'LSP viene disabilitato. Si tratta di un valore intero che è 32 o 64.

</dd> <dt>

*Programma di installazione* 
</dt> <dd>

Nome file del modulo dell'applicazione che effettua la chiamata di disabilitazione LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valore GUID del provider di trasporto Winsock disabilitato dal provider di servizi di configurazione locale.

</dd> <dt>

*Categoria* 
</dt> <dd>

Membro **dwCatalogEntryId** della [**struttura WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP disabilitato.

</dd> </dl>

Questo evento non ha parametri.

## <a name="remarks"></a>Commenti

**L'evento DISABLE di WINSOCK \_ WS2HELP \_ LSP \_** viene tracciato per un'operazione di disabilitazione LSP quando una voce di protocollo è disabilitata nel catalogo Winsock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo della traccia Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Traccia winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia di Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Dettagli di traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
