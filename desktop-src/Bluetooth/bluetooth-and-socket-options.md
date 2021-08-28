---
title: Bluetooth e socket
description: Bluetooth per Windows supporta le opzioni socket seguenti.
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- Bluetooth opzioni socket e Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631eb2b041fcc320723155d4a5df1742e6c0dc79cb579815de141334906708e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588431"
---
# <a name="bluetooth-and-socket-options"></a>Bluetooth e socket

Bluetooth per Windows supporta le opzioni socket seguenti. Le opzioni socket vengono impostate e sottoposti a query usando rispettivamente le funzioni [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) e [**getsockopt.**](/windows/desktop/api/winsock/nf-winsock-getsockopt) Tutte le opzioni seguenti possono essere usate con la funzione **setsockopt,** ma solo l'opzione **\_ SO BTH \_ MTU** è disponibile per l'uso con la **funzione getsockopt.**

Per l'uso delle opzioni socket Bluetooth seguenti:

-   Il *parametro s* deve essere un Bluetooth socket.
-   Il *parametro level* deve essere SOL **\_ RFCOMM.**

## <a name="so_bth_authenticate"></a>QUINDI \_ BTH ESEGUE \_ L'AUTENTICAZIONE

Per i socket disconnessi, **SO \_ BTH \_ AUTHENTICATE** specifica [](/windows/desktop/api/winsock2/nf-winsock2-connect) che [](/windows/desktop/api/winsock2/nf-winsock2-accept) l'autenticazione è necessaria per il corretto completamento di un'operazione di connessione o accettazione. L'impostazione di questa opzione socket avvia attivamente l'autenticazione durante la creazione della connessione, se i due Bluetooth non sono stati autenticati in precedenza. L'interfaccia utente per lo scambio di passkey, se necessario, viene fornita dal sistema operativo all'esterno del contesto dell'applicazione.

Per le connessioni in [](/windows/desktop/api/winsock2/nf-winsock2-connect) uscita che richiedono l'autenticazione, l'operazione di connessione ha esito negativo **con WSAEACCES** se l'autenticazione non riesce. In risposta, l'applicazione può richiedere all'utente di autenticare i due dispositivi Bluetooth prima della connessione.

Per le connessioni in ingresso, la connessione viene rifiutata se non è possibile stabilire l'autenticazione e restituisce un **errore WSAEHOSTDOWN.** Per altre informazioni sull'autenticazione Bluetooth dispositivi, vedere [**BluetoothAuthenticateDevice.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)

Per **l'opzione SO \_ BTH \_ AUTHENTICATE** socket, *optval* è un puntatore a ULONG bAuthenticate e deve essere **TRUE;** *optlen* equivale a "sizeof(ULONG)".

**Windows XP con SP2: SO \_ BTH \_ AUTHENTICATE avvia** l'autenticazione per i socket connessi e forza l'autenticazione al momento della connessione per i socket non connessi. Per le connessioni in ingresso, la connessione viene rifiutata se non è possibile eseguire l'autenticazione.

## <a name="so_bth_encrypt"></a>QUINDI \_ BTH \_ ENCRYPT

Nei socket non collegati, **l'opzione SO \_ BTH \_ ENCRYPT** del socket impone la crittografia per stabilire una connessione. La crittografia è disponibile solo per le connessioni autenticate. Per le connessioni in ingresso, una connessione per cui non è possibile stabilire la crittografia viene rifiutata automaticamente e restituisce **WSAEHOSTDOWN** come errore. Per le connessioni in uscita, [**la funzione connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) ha esito negativo con **WSAEACCES** se non è possibile stabilire la crittografia. In risposta, l'applicazione può richiedere all'utente di autenticare i due dispositivi Bluetooth prima della connessione. Per altre informazioni sull'autenticazione Bluetooth dispositivi, vedere [**BluetoothAuthenticateDevice.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)

Per l'opzione del socket SO BTH ENCRYPT, optval è un puntatore \_ \_ a ULONG **bEncrypt** e deve essere **TRUE;**  *optlen* equivale a sizeof(ULONG).

**Windows XP con SP2:** Per un socket connesso e autenticato, **SO \_ BTH \_ ENCRYPT avvia** la crittografia.

## <a name="so_bth_mtu"></a>SO \_ BTH \_ MTU

**\_ L'opzione so BTH \_ MTU** socket è un'opzione avanzata usata principalmente per la convalida. **\_ L'opzione SO BTH \_ MTU** ottiene o imposta il valore predefinito RFCOMM MTU (unità massima di trasmissione) per la negoziazione della connessione su un valore diverso dal valore predefinito del protocollo RFCOMM.

Poiché la MTU RFCOMM è interessata dal valore MTU L2CAP sottostante e dai valori minimi e massimi del protocollo e dell'applicazione, il valore predefinito per SO **\_ BTH \_ MTU** è solo un punto di partenza per la negoziazione con il peer remoto ed è probabile che il valore MTU negoziato finale sia diverso da quello predefinito. **L'impostazione del \_ valore \_ MTU SO BTH** può influire negativamente sulla velocità effettiva e, di conseguenza, qualsiasi modifica deve essere eseguita con la conoscenza del protocollo Bluetooth sottostante.

**L'opzione so \_ BTH \_ MTU** socket può essere eseguita sui socket connessi, ma non ha alcun effetto se la negoziazione è già stata completata. L'impostazione sul socket in ascolto (server) non ha alcun effetto.

La quantità di dati che un'applicazione può inviare o ricevere in una singola chiamata socket non è interessata dall'MTU. L'MTU influisce solo sul modo in cui il provider Windows Sockets segmenta i pacchetti per il trasporto. Sia la MTU proposta che la MTU negoziata devono essere tra **RFCOMM \_ MIN \_ MTU** e **RFCOMM \_ MAX \_ MTU,** come definito nel file di intestazione Ws2bth.h.

Per **l'opzione so \_ BTH \_ MTU** socket, *optval* è un puntatore a ULONG mtu; *optlen* equivale a "sizeof(ULONG)".

## <a name="so_bth_mtu_max"></a>SO \_ BTH \_ MTU \_ MAX

**L'opzione SO \_ BTH \_ MTU \_ MAX** socket è un'opzione avanzata usata principalmente per la convalida. **L'opzione SO \_ BTH \_ MTU \_ MAX** socket imposta il valore massimo di RFCOMM MTU (unità massima di trasmissione) per la negoziazione della connessione. Le connessioni con un MTU RFCOMM uguale o maggiore di questo valore hanno esito negativo durante il [**processo di**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**accettazione della**](/windows/desktop/api/winsock2/nf-winsock2-accept) connessione. Mentre l'impostazione di questa opzione socket è consentita per un socket connesso, non ha alcun effetto se la negoziazione è stata completata. L'impostazione di questa opzione socket su un socket di ascolto propaga il valore per tutte le connessioni in ingresso. Il valore max MTU deve essere compreso tra **RFCOMM \_ MIN \_ MTU** e **RFCOMM \_ MAX \_ MTU,** come definito nel file di intestazione Ws2bth.h.

Per **l'opzione SO \_ BTH \_ MTU \_ MAX** socket, *optval* è un puntatore a ULONG max \_ mtu; *optlen* equivale a "sizeof(ULONG)".

## <a name="so_bth_mtu_min"></a>SO \_ BTH \_ MTU \_ MIN

**L'opzione SO \_ BTH \_ MTU \_ MIN** socket è un'opzione avanzata usata principalmente per la convalida. **L'opzione SO \_ BTH \_ MTU \_ MIN** socket imposta il valore minimo di RFCOMM MTU (unità massima di trasmissione) per la negoziazione della connessione. Le connessioni con un MTU RFCOMM inferiore a questo valore hanno esito negativo durante il [**processo di**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**accettazione della**](/windows/desktop/api/winsock2/nf-winsock2-accept) connessione. Mentre l'impostazione di questa opzione socket è consentita per un socket connesso, non ha alcun effetto se la negoziazione è stata completata. L'impostazione di questa opzione socket su un socket di ascolto propaga il valore per tutte le connessioni in ingresso.

Solo un socket di ascolto può modificare il valore MTU verso il basso, pertanto se il valore proposto dal socket di connessione è minore del valore impostato per **SO \_ BTH \_ MTU \_ MIN** sul socket di ascolto, la connessione viene rifiutata. Il valore minimo di MTU deve essere compreso tra **RFCOMM \_ MIN \_ MTU** e **RFCOMM \_ MAX \_ MTU,** come definito nel file di intestazione Ws2bth.h.

Per l'opzione SO \_ BTH \_ MTU \_ MIN socket, *optval* è un puntatore a ULONG min \_ mtu; *optlen* equivale a "sizeof(ULONG)".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[**connettersi**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**Accettare**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 