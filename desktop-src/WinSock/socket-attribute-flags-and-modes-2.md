---
description: Esistono diversi attributi socket che possono essere indicati tramite il parametro flags in WSPSocket.
ms.assetid: 5fd4321b-a5cc-4921-bec5-bdf625261ea2
title: Flag e modalità dell'attributo socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da1a5f621a7d9f489f4e91782462c215659772b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315775"
---
# <a name="socket-attribute-flags-and-modes"></a>Flag e modalità dell'attributo socket

Esistono diversi attributi socket che possono essere indicati tramite il parametro *Flags* in [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Il \_ flag WSA \_ OVERLAPPED flag indica che verrà utilizzato un socket per le operazioni di I/O sovrapposte. Il supporto di questo attributo è obbligatorio per tutti i provider di servizi. Per ulteriori informazioni, vedere [I/O sovrapposti](overlapped-i-o-2.md) . Si noti che la creazione di un socket con l'attributo Overlapped non ha alcun effetto sul fatto che un socket sia attualmente in modalità di blocco o non blocco. I socket creati con l'attributo Overlapped possono essere utilizzati per eseguire operazioni di I/O sovrapposte e non modificano la modalità di blocco di un socket. Poiché le operazioni di I/O sovrapposte non vengono bloccate, la modalità di blocco di un socket è irrilevante per queste operazioni.

Quando si creano socket da usare per le operazioni multipoint e/o multicast e il supporto per questi attributi è facoltativo, vengono usati quattro flag di attributo aggiuntivi. I provider che supportano gli attributi multipoint indicano questo problema tramite il \_ \_ bit multipoint XP1 supporto nelle rispettive strutture di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Vedere [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) e [multicast indipendente dal protocollo e MultiPoint nell'API](protocol-independent-multicast-and-multipoint-in-the-spi-2.md) per la definizione e l'uso di ognuno di questi flag. Solo i socket creati con attributi correlati a MultiPoint possono essere usati nella funzione [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per la creazione di sessioni multipoint.

Un socket si trova in una delle due modalità, bloccando e non bloccando, in qualsiasi momento. Per impostazione predefinita, i socket vengono creati in modalità di blocco e possono essere modificati in modalità non di blocco chiamando [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)). Un socket può tornare alla modalità di blocco usando **WSPIoctl** se non è attivo alcun **WSPAsyncSelect** o **WSPEventSelect** . La modalità per un socket interessa solo le funzioni che possono bloccarsi e non influisce sulle operazioni di I/O sovrapposte. Per ulteriori informazioni, vedere [operazioni di blocco](blocking-operations-2.md) .

 

 
