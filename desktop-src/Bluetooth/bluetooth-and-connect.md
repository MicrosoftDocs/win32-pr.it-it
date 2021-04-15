---
title: Bluetooth e Connetti
description: Bluetooth usa la funzione Connect per connettersi a un dispositivo Bluetooth di destinazione usando un Socket Bluetooth creato in precedenza.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- Connetti Bluetooth
- Bluetooth e connessione Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b631aabbcd44d009ba30b9deb486e92a22feaec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474062"
---
# <a name="bluetooth-and-connect"></a>Bluetooth e Connetti

Bluetooth usa la funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) per connettersi a un dispositivo Bluetooth di destinazione usando un Socket Bluetooth creato in precedenza. Il parametro *Name* della funzione **Connect** , che è una struttura [**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) , deve specificare un dispositivo Bluetooth di destinazione. Per identificare il dispositivo di destinazione vengono usati due meccanismi:

-   La struttura [**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) può specificare direttamente il numero di porta a cui viene richiesta una connessione. Questo meccanismo richiede che l'applicazione esegua le proprie query SDP prima di tentare un'operazione di [**connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect) .
-   La struttura [**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) può specificare l'ID univoco della classe del servizio a cui si desidera connettersi. Se il dispositivo peer ha più di una porta che corrisponde all'ID della classe del servizio, la chiamata della funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) si connette al primo servizio valido. Questo meccanismo può essere usato senza query SDP precedenti.

Quando si usa la struttura [**\_ BTH di SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) , si applicano i requisiti seguenti:

-   Il membro **btAddr** deve essere un indirizzo di radio remoto valido.
-   Per il membro **serviceClassId** , se il membro della porta è zero, il sistema tenta di usare **serviceClassId** per risolvere la porta remota corrispondente al servizio. La classe del servizio è un GUID normalizzato a 128 bit, definito dalla specifica Bluetooth. I GUID comuni sono definiti dal documento relativo ai numeri assegnati Bluetooth. In alternativa, è possibile utilizzare un GUID univoco per un'applicazione specifica del dominio.
-   Il membro della **porta** deve essere una porta remota valida oppure zero se il membro **serviceClassId** è specificato.

Nella tabella seguente sono elencati i codici di risultato per Bluetooth e la funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

| Errore/errore\#                    | Descrizione                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | Funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) chiamata per il socket già connesso. |
| WSAEACCES10013<br/>        | Connessione dell'autenticazione richiesta dall'applicazione, ma autenticazione non riuscita.        |
| WSAENOBUFS10055<br/>       | Errore irreversibile di memoria insufficiente.                                                 |
| WSAEADDRINUSE10048<br/>    | Il numero di porta/canale richiesto è in uso.                                       |
| WSAETIMEDOUT10060<br/>     | Si è verificato il timeout di i/O a livello di radio Bluetooth (timeout della pagina \_ ).                    |
| WSAEDISCON10101<br/>       | Canale RFCOMM disconnesso dal peer remoto.                                    |
| WSAECONNRESET10054<br/>    | Multiplexer RFCOMM (sessione) disconnesso dal peer remoto.                      |
| WSAECONNABORTED10053<br/>  | Socket arrestato dall'applicazione.                                                   |
| WSAENETUNREACH10051<br/>   | Errore diverso dal timeout a livello di L2CAP o di radio Bluetooth.                       |
| WSAEHOSTDOWN10064<br/>     | RFCOMM ha ricevuto la risposta DM.                                                   |
| WSAENETDOWN10050<br/>      | Errore di rete imprevisto.                                                          |
| WSAESHUTDOWN10058<br/>     | Canale L2CAP disconnesso dal peer remoto.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Porta/canale Bluetooth o indirizzo del dispositivo non valido.                                |
| WSAEINVAL10022<br/>        | Plug and Play, evento dello stack del driver o altro errore causato da un errore.                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**\_BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

