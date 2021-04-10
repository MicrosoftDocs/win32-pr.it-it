---
title: Opzioni Bluetooth e socket
description: Bluetooth per Windows supporta le seguenti opzioni di socket.
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- Opzioni Bluetooth e Socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84040a98c3dae1fec292e4f0a7086f11d1ee546c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963172"
---
# <a name="bluetooth-and-socket-options"></a>Opzioni Bluetooth e socket

Bluetooth per Windows supporta le seguenti opzioni di socket. Le opzioni socket vengono impostate e sottoposte a query usando rispettivamente le funzioni [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) e [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Con la funzione **setsockopt** è possibile usare tutte le opzioni seguenti, ma solo l'opzione **\_ BTH \_ MTU** è disponibile per l'uso con la funzione **getsockopt** .

Le impostazioni seguenti sono necessarie per usare le opzioni del Socket Bluetooth:

-   Il parametro *s* deve essere un Socket Bluetooth.
-   Il parametro *Level* deve essere **Sol \_ rfcomm**.

## <a name="so_bth_authenticate"></a>\_BTH l' \_ autenticazione

Per i socket disconnessi, il modo in cui l'autenticazione di **\_ BTH \_** specifica che l'autenticazione è necessaria per il corretto completamento di un'operazione di [**connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect) o [**accettazione**](/windows/desktop/api/winsock2/nf-winsock2-accept) . L'impostazione di questa opzione socket avvia attivamente l'autenticazione durante la creazione della connessione, se i due dispositivi Bluetooth non sono stati autenticati in precedenza. L'interfaccia utente per lo scambio di passkey, se necessario, viene fornita dal sistema operativo all'esterno del contesto dell'applicazione.

Per le connessioni in uscita che richiedono l'autenticazione, l'operazione di [**connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect) ha esito negativo con **WSAEACCES** se l'autenticazione non riesce. In risposta, l'applicazione potrebbe richiedere all'utente di autenticare i due dispositivi Bluetooth prima della connessione.

Per le connessioni in ingresso, la connessione viene rifiutata se non è possibile stabilire l'autenticazione e restituisce un errore **WSAEHOSTDOWN** . Per ulteriori informazioni sull'autenticazione dei dispositivi Bluetooth, vedere [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Per l' **opzione \_ BTH \_ Authenticate** socket, *OPTVAL* è un puntatore a ULONG bAuthenticate e deve essere **true**; *optlen* è equivalente a "sizeof (ulong)".

**Windows XP con SP2: \_ BTH \_ Authenticate** avvia l'autenticazione per i socket connessi e impone l'autenticazione al momento della connessione per i socket non connessi. Per le connessioni in ingresso, la connessione viene rifiutata se non è possibile eseguire l'autenticazione.

## <a name="so_bth_encrypt"></a>QUINDI, \_ BTH \_ Crittografa

Nei socket non connessi, l'opzione di crittografia socket di **\_ BTH \_** consente di applicare la crittografia per stabilire una connessione. La crittografia è disponibile solo per le connessioni autenticate. Per le connessioni in ingresso, una connessione per la quale non è possibile stabilire la crittografia viene rifiutata automaticamente e restituisce **WSAEHOSTDOWN** come errore. Per le connessioni in uscita, la funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) ha esito negativo con **WSAEACCES** se non è possibile stabilire la crittografia. In risposta, l'applicazione potrebbe richiedere all'utente di autenticare i due dispositivi Bluetooth prima della connessione. Per ulteriori informazioni sull'autenticazione dei dispositivi Bluetooth, vedere [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Per l' \_ opzione BTH \_ Encrypt socket, *optVal* è un puntatore a ULONG **bEncrypt** e deve essere **true**; *optlen* è equivalente a sizeof (ulong).

**Windows XP con SP2:** Per un socket connesso e autenticato, **\_ BTH \_ Encrypt** avvia la crittografia.

## <a name="so_bth_mtu"></a>\_BTH \_ MTU

L'opzione di socket **\_ \_ MTU BTH** è un'opzione avanzata utilizzata principalmente per la convalida. L' **opzione \_ BTH \_ MTU** consente di ottenere o impostare la MTU rfcomm predefinita (unità di trasmissione massima) per la negoziazione della connessione a un valore diverso da quello del protocollo RFCOMM-valore predefinito.

Poiché l'MTU RFCOMM è influenzato dal valore MTU L2CAP sottostante e dai valori minimi e massimi del protocollo e dell'applicazione, il valore predefinito per **\_ BTH \_ MTU** è solo un punto di partenza per la negoziazione con il peer remoto e la MTU negoziata finale è probabilmente diversa da quella predefinita. L'impostazione del valore **\_ \_ MTU BTH** può influire negativamente sulla velocità effettiva e, di conseguenza, qualsiasi modifica deve essere eseguita con la conoscenza del protocollo Bluetooth sottostante.

L'opzione di socket **\_ \_ MTU BTH** può essere eseguita sui socket connessi, ma non ha alcun effetto se la negoziazione è già stata completata. L'impostazione del socket in ascolto (Server) non ha alcun effetto.

La quantità di dati che un'applicazione può inviare o ricevere in una singola chiamata al socket non è interessata dalla MTU; MTU influiscono solo sul modo in cui il provider del servizio Windows Sockets sottostante suddivide i pacchetti per il trasporto. Sia la MTU proposta che la MTU finale negoziata devono essere comprese tra **rfcomm \_ Min \_ MTU** e **rfcomm \_ Max \_ MTU**, come definito nel file di intestazione Ws2bth. h.

Per l'opzione di socket **\_ \_ MTU BTH** , *OPTVAL* è un puntatore a ULONG MTU; *optlen* è equivalente a "sizeof (ulong)".

## <a name="so_bth_mtu_max"></a>\_BTH \_ MTU \_ Max

L'opzione di socket **\_ BTH \_ MTU \_ Max** è un'opzione avanzata utilizzata principalmente per la convalida. L' **opzione \_ BTH \_ MTU \_ Max** Socket imposta il numero massimo di rfcomm MTU (Maximum Transmission Unit) per la negoziazione della connessione. Le connessioni con un valore MTU rfcomm maggiore o uguale a questo valore hanno esito negativo durante il processo di accettazione della [**connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [](/windows/desktop/api/winsock2/nf-winsock2-accept) . Quando è consentita l'impostazione di questa opzione socket per un socket connesso, non ha alcun effetto se la negoziazione è stata completata. L'impostazione di questa opzione socket su un socket di ascolto propaga il valore per tutte le connessioni in ingresso. Il valore MTU massimo deve essere compreso tra **rfcomm \_ Min \_ MTU** e **rfcomm \_ Max \_ MTU**, come definito nel file di intestazione Ws2bth. h.

Per l'opzione di socket **\_ \_ \_ Max BTH MTU** , *optVal* è un puntatore a ULONG Max \_ MTU; *optlen* è equivalente a "sizeof (ulong)".

## <a name="so_bth_mtu_min"></a>\_BTH \_ MTU \_ min

L' **opzione \_ BTH \_ MTU \_ min** socket è un'opzione avanzata utilizzata principalmente per la convalida. L' **opzione \_ BTH \_ MTU \_ min** Socket imposta il valore minimo rfcomm MTU (Maximum Transmission Unit) per la negoziazione della connessione. Le connessioni con un valore MTU rfcomm inferiore a questo valore hanno esito negativo durante il processo di accettazione della [**connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [](/windows/desktop/api/winsock2/nf-winsock2-accept) . Quando è consentita l'impostazione di questa opzione socket per un socket connesso, non ha alcun effetto se la negoziazione è stata completata. L'impostazione di questa opzione socket su un socket di ascolto propaga il valore per tutte le connessioni in ingresso.

Solo un socket in ascolto può rivedere l'MTU verso il basso, pertanto se il valore proposto dal socket di connessione è inferiore al valore impostato **per \_ BTH \_ MTU \_ min** sul socket in ascolto, la connessione viene rifiutata. Il valore MTU minimo deve essere compreso tra **rfcomm \_ Min \_ MTU** e **rfcomm \_ Max \_ MTU**, come definito nel file di intestazione Ws2bth. h.

Per l' \_ opzione BTH \_ MTU \_ min socket, *optVal* è un puntatore a ULONG min \_ MTU; *optlen* è equivalente a "sizeof (ulong)".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[**connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**accettare**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 