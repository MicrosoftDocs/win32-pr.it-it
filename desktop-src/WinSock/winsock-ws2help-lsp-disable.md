---
description: Evento di modifica del catalogo Winsock per un'operazione di disabilitazione di un provider di servizi a più livelli (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: Evento WINSOCK_WS2HELP_LSP_DISABLE
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
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315752"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>\_Evento di \_ disabilitazione LSP ws2help di Winsock \_

> [!Note]  
> I provider di servizi sovrapposti sono deprecati. A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

L'evento di **\_ \_ \_ disabilitazione LSP ws2help di Winsock** è un evento di modifica del catalogo Winsock per un'operazione di disabilitazione di un provider di servizi a più livelli.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome LSP* 
</dt> <dd>

Nome dello LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP disabilitato.

</dd> <dt>

*Catalogo* 
</dt> <dd>

Il catalogo Winsock (32 bit o 64 bit) in cui lo LSP viene disabilitato. Si tratta di un valore intero che può essere 32 o 64.

</dd> <dt>

*Programma di installazione* 
</dt> <dd>

Il nome file del modulo dell'applicazione che effettua la chiamata di disabilitazione di LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valore GUID del provider di trasporto Winsock che verrà disabilitato da LSP.

</dd> <dt>

*Categoria* 
</dt> <dd>

Membro **dwCatalogEntryId** della struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP disabilitato.

</dd> </dl>

Questo evento non contiene parametri.

## <a name="remarks"></a>Commenti

L'evento di **\_ \_ \_ disabilitazione LSP ws2help di Winsock** viene tracciato per un'operazione di disabilitazione LSP quando una voce di protocollo è disabilitata nel catalogo Winsock.

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

 

 
