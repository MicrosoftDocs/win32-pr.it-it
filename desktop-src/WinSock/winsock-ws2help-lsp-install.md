---
description: Evento di modifica del catalogo Winsock per un'operazione di installazione di un provider di servizi a più livelli (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: Evento WINSOCK_WS2HELP_LSP_INSTALL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968056"
---
# <a name="winsock_ws2help_lsp_install-event"></a>Evento di installazione di WINSOCK \_ ws2help \_ LSP \_

> [!Note]  
> I provider di servizi sovrapposti sono deprecati. A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

L'evento di **installazione di Winsock \_ ws2help \_ LSP \_** è un evento di modifica del catalogo Winsock per un'operazione di installazione di un provider di servizi a più livelli (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome LSP* 
</dt> <dd>

Nome dello LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da installare.

</dd> <dt>

*Catalogo* 
</dt> <dd>

Il catalogo Winsock (32 bit o 64 bit) in cui viene installato lo LSP. Si tratta di un valore intero che può essere 32 o 64.

</dd> <dt>

*Programma di installazione* 
</dt> <dd>

Il nome file del modulo dell'applicazione che effettua la chiamata di installazione di LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valore GUID del provider di trasporto Winsock in cui viene installato il LSP.

</dd> <dt>

*Categoria* 
</dt> <dd>

Membro **dwCatalogEntryId** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da installare.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'evento di **installazione di Winsock \_ ws2help \_ LSP \_** viene tracciato per un'operazione di installazione di LSP quando viene installata una voce di protocollo nel catalogo Winsock.

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

 

 
