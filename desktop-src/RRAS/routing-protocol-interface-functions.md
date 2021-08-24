---
title: Funzioni dell'interfaccia del protocollo di routing
description: Implementare le funzioni seguenti per una DLL del protocollo di routing
ms.assetid: fd780458-ef23-4ef2-8fe8-29b32100917f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f050c27bbfd498b1ffd36d90a1e5792fdf9283a6eb47e86a35747df6b8cb8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672751"
---
# <a name="routing-protocol-interface-functions"></a>Funzioni dell'interfaccia del protocollo di routing

Implementare le funzioni seguenti per una DLL del protocollo di routing:

[**AddInterface**](/windows/desktop/api/Routprot/nc-routprot-padd_interface)

[**ConnectClient**](/windows/desktop/api/Routprot/nc-routprot-pconnect_client)

[**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)

[**DisconnectClient**](/windows/desktop/api/Routprot/nc-routprot-pdisconnect_client)

[**DoUpdateRoutes**](/windows/desktop/api/Routprot/nc-routprot-pdo_update_routes)

[*DoUpdateServices*](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))

[**GetEventMessage**](/windows/desktop/api/Routprot/nc-routprot-pget_event_message)

[**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)

[**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)

[**GetMfeStatus**](/windows/desktop/api/Routprot/nc-routprot-pget_mfe_status)

[**GetNeighbors**](/windows/desktop/api/Routprot/nc-routprot-pget_neighbors)

[**InterfaceStatus**](/windows/desktop/api/Routprot/nc-routprot-pinterface_status)

[**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)

[**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)

[**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)

[**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)

[**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)

[*MibGetTrapInfo*](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)

[**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)

[**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

[**QueryPower**](/windows/desktop/api/Routprot/nc-routprot-pquery_power)

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)

[**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)

[**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

[**SetPower**](/windows/desktop/api/Routprot/nc-routprot-pset_power)

[**StartComplete**](/windows/desktop/api/Routprot/nc-routprot-pstart_complete)

[**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)

[**StopProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstop_protocol)

[**UnbindInterface**](/previous-versions/windows/desktop/legacy/aa382296(v=vs.85))

Se il protocollo di routing supporta la gestione dei servizi, implementare la funzione seguente oltre a quelle elencate in precedenza:

[**DoUpdateServices**](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))

 

 