---
title: Bluetooth e WSASetService
description: Bluetooth usa la funzione WSASetService per registrare o rimuovere un'istanza del servizio nello spazio dei nomi Bluetooth (NS \_ BTH) dal registro di sistema.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- WSASetService Bluetooth
- Bluetooth e WSASetService Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473246"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth e WSASetService

Bluetooth usa la funzione [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) per registrare o rimuovere un'istanza del servizio nello spazio dei nomi Bluetooth (NS \_ BTH) dal registro di sistema. L'handle restituito da questa operazione può essere utilizzato solo per eliminare il servizio.

Bluetooth offre due metodi per la pubblicità dei servizi tramite la funzione [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :

-   L'applicazione può fare in modo che il sistema annunci un semplice record di servizio Bluetooth SDP, costruito da membri standard nella struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .
-   L'applicazione può fare in modo che il sistema annunci il proprio record SDP Bluetooth passando una struttura del [**\_ \_ servizio set BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) nel membro **lpBlob** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . Si tratta di un approccio più complesso.

> [!Note]  
> I record SDP annunciati da [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) non vengono mantenuti dopo la chiusura del processo che li ha pubblicati.

 

L'uso di [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) con Bluetooth prevede i requisiti seguenti:

-   Il parametro *lpqsRegInfo* è l'indirizzo della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) da registrare.
-   Il parametro *essOperation* è un'enumerazione che contiene una delle operazioni mostrate nella tabella seguente.



| Valore                  | Descrizione                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| \_Registro RNRSERVICE   | Inizia a annunciare il servizio alle radio remote che eseguono query usando il protocollo Bluetooth SDP. |
| RNRSERVICE \_ annullare la registrazione | Non valido. Restituisce un errore.                                                               |
| eliminazione di RNRSERVICE \_     | Interrompe la pubblicità del servizio.                                                             |



 

> [!Note]  
> Gli handle del servizio individuati durante una chiamata [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) o [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) non sono compatibili con l' \_ operazione di eliminazione RNRSERVICE.

 

-   Il parametro *dwControlFlags* è riservato e deve essere zero.

Per altre informazioni e per un elenco delle opzioni dei Socket Bluetooth, vedere [Opzioni per Bluetooth e socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 