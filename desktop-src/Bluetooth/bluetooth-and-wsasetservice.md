---
title: Bluetooth e WSASetService
description: Bluetooth usa la funzione WSASetService per registrare o rimuovere un'istanza del servizio all'interno dello spazio dei nomi Bluetooth (NS \_ BTH) dal Registro di sistema.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- WSASetService Bluetooth
- Bluetooth e WSASetService Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671e43636de67cee1e1c3c945a3647b5db59e7b0dd22b6eefd70b51f4977c31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004171"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth e WSASetService

Bluetooth usa la [**funzione WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) per registrare o rimuovere un'istanza del servizio all'interno dello spazio dei nomi Bluetooth (NS \_ BTH) dal Registro di sistema. L'handle restituito da questa operazione può essere usato solo per eliminare il servizio.

Bluetooth dispone di due mezzi di pubblicità che usano la [**funzione WSASetService:**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)

-   L'applicazione può fare in modo che il sistema annunci un record Bluetooth servizio SDP semplice, costruito da membri standard nella [**struttura WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
-   L'applicazione può fare in modo che il sistema annunci il proprio record SDP Bluetooth passando una struttura [**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) nel membro **lpBlob** della [**struttura WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) Si tratta di un approccio più complesso.

> [!Note]  
> I record SDP annunciati da [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) non vengono mantenuti dopo la chiusura del processo che li ha pubblicati.

 

[**L'uso di WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) con Bluetooth presenta i requisiti seguenti:

-   Il *parametro lpqsRegInfo* è l'indirizzo della [**struttura WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) da registrare.
-   Il *parametro essOperation* è un'enumerazione che contiene una delle operazioni illustrate nella tabella seguente.



| Valore                  | Descrizione                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| REGISTRO \_ RNRSERVICE   | Avvia la pubblicità del servizio alle radio remote che esere query usando Bluetooth protocollo SDP. |
| ANNULLAMENTO DELLA REGISTRAZIONE DI RNRSERVICE \_ | Non valido. Restituisce un errore.                                                               |
| RNRSERVICE \_ DELETE     | Arresta la pubblicità del servizio.                                                             |



 

> [!Note]  
> Gli handle del servizio individuati durante una chiamata [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) o [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) non sono compatibili con l'operazione RNRSERVICE \_ DELETE.

 

-   Il *parametro dwControlFlags* è riservato e deve essere zero.

Per altre informazioni e un elenco di opzioni Bluetooth socket, vedere Bluetooth [e Opzioni socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 