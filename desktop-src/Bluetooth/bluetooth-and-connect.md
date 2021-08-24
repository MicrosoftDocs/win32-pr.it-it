---
title: Bluetooth e connettersi
description: Bluetooth la funzione connect per connettersi a un dispositivo Bluetooth di destinazione usando un socket Bluetooth creato in precedenza.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- connettersi Bluetooth
- Bluetooth e connettersi Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e00456b3174c49676e081a0fa6188da13fd54f8e07940edcf703e7f5b680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588461"
---
# <a name="bluetooth-and-connect"></a>Bluetooth e connettersi

Bluetooth usa la [**funzione connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) per connettersi a un dispositivo Bluetooth di destinazione, usando un socket Bluetooth precedente. Il *parametro name* della funzione **connect,** che è una struttura [**SOCKADDR \_ BTH,**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) deve specificare una destinazione Bluetooth dispositivo. Per identificare il dispositivo di destinazione vengono usati due meccanismi:

-   La [**struttura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) può specificare direttamente il numero di porta a cui viene richiesta una connessione. Questo meccanismo richiede all'applicazione di eseguire le proprie query SDP prima di tentare [**un'operazione di**](/windows/desktop/api/winsock2/nf-winsock2-connect) connessione.
-   La [**struttura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) può specificare l'ID univoco della classe di servizio del servizio a cui si vuole connettersi. Se il dispositivo peer ha più di una porta corrispondente all'ID della classe del servizio, la chiamata di funzione [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) si connette al primo servizio valido. Questo meccanismo può essere usato senza query SDP precedenti.

Quando si usa [**la struttura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la [**funzione connect,**](/windows/desktop/api/winsock2/nf-winsock2-connect) si applicano i requisiti seguenti:

-   Il **membro btAddr** deve essere un indirizzo radio remoto valido.
-   Per il **membro serviceClassId,** se il membro della porta è zero, il sistema tenta di usare **serviceClassId** per risolvere la porta remota corrispondente al servizio. La classe di servizio è un GUID normalizzato a 128 bit, definito dalla Bluetooth specifica. I GUID comuni sono definiti dal documento Bluetooth numeri assegnati. In alternativa, è possibile usare un GUID univoco per un'applicazione specifica del dominio.
-   Il **membro** della porta deve essere una porta remota valida oppure zero se viene specificato il membro **serviceClassId.**

Nella tabella seguente sono elencati i codici di risultato per Bluetooth e la [**funzione connect.**](/windows/desktop/api/winsock2/nf-winsock2-connect)

| Errore/errore\#                    | Descrizione                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | La [**funzione connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) chiamata per il socket già connesso. |
| WSAEACCES10013<br/>        | La connessione dell'applicazione ha richiesto l'autenticazione, ma l'autenticazione non è riuscita.        |
| WSAENOBUFS10055<br/>       | Errore di memoria insufficiente irreversibile.                                                 |
| WSAEADDRINUSE10048<br/>    | Il numero di porta/canale richiesto è in uso.                                       |
| WSAETIMEDOUT10060<br/>     | Timeout dell'I/O a livello Bluetooth radio (TIMEOUT \_ PAGINA).                    |
| WSAEDISCON10101<br/>       | Canale RFCOMM disconnesso dal peer remoto.                                    |
| WSAECONNRESET10054<br/>    | Multiplexor RFCOMM (sessione) disconnesso dal peer remoto.                      |
| WSAECONNABORTED10053<br/>  | Socket arrestato dall'applicazione.                                                   |
| WSAENETUNREACH10051<br/>   | Errore diverso dal timeout a livello di L2CAP o Bluetooth radio.                       |
| WSAEHOSTDOWN10064<br/>     | RfcOMM ha ricevuto la risposta DM.                                                   |
| WSAENETDOWN10050<br/>      | Errore di rete imprevisto.                                                          |
| WSAESHUTDOWN10058<br/>     | Canale L2CAP disconnesso dal peer remoto.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Bluetooth porta/canale o indirizzo del dispositivo non valido.                                |
| WSAEINVAL10022<br/>        | Plug and Play, l'evento driver-stack o un altro errore ha causato un errore.                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**connettersi**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

