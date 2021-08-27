---
description: È progettato per consentire a un'applicazione di abilitare pacchetti keep-alive per una connessione socket.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: SO_KEEPALIVE socket (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3590b8813f584aad16896a5b990baa2e3ad5607b76a13bd987d87961ee5f6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097471"
---
# <a name="so_keepalive-socket-option"></a>Opzione \_ del socket KEEPALIVE

L'opzione socket **\_ SO KEEPALIVE** è progettata per consentire a un'applicazione di abilitare pacchetti keep-alive per una connessione socket.

Per eseguire una query sullo stato di questa opzione socket, chiamare la [**funzione getsockopt.**](/windows/desktop/api/winsock/nf-winsock-getsockopt) Per impostare questa opzione, chiamare la [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con i parametri seguenti.

## <a name="socket-option-value"></a>Valore dell'opzione socket

La costante che rappresenta questa opzione socket è 0x0008.

## <a name="syntax"></a>Sintassi


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Descrittore che identifica il socket.

</dd> <dt>

*level* \[ Pollici\]
</dt> <dd>

Livello al quale è definita l'opzione. Usare **SOL \_ SOCKET** per questa operazione.

</dd> <dt>

*optname* \[ Pollici\]
</dt> <dd>

Opzione socket per cui impostare il valore. Usare **SO \_ KEEPALIVE** per questa operazione.

</dd> <dt>

*optval* \[ Cambio\]
</dt> <dd>

Puntatore al buffer contenente il valore dell'opzione da impostare. Questo parametro deve puntare al buffer uguale o maggiore delle dimensioni di un **valore DWORD.**

Questo valore viene considerato come valore booleano con 0 usato per indicare **FALSE** (disabilitato) e un valore diverso da zero per indicare **TRUE** (abilitato).

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Puntatore alla dimensione, in byte, del buffer *optval.* Questa dimensione deve essere uguale o maggiore della dimensione di un **valore DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) restituisce zero.

Se l'operazione ha esito negativo, viene restituito il valore SOCKET ERROR e un codice di errore specifico può essere recuperato chiamando \_ [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Codice di errore                                                                                                                                              | Significato                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Prima di usare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) riuscita.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il sottosistema di rete non è riuscito.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno dei parametri *optval* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio indirizzi utente. Questo errore viene restituito anche se il valore a cui punta il *parametro optlen* è minore delle dimensioni di un **valore DWORD.**<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | È in corso Windows chiamata a Sockets 1.1 o il provider di servizi sta ancora elaborando una funzione di callback.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Il *parametro level* è sconosciuto o non valido. In Windows Vista e versioni successive, questo errore viene restituito anche se il socket si trova in uno stato di transizione.<br/>                                                                                                 |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata. Questo errore viene restituito se il descrittore del socket passato nel *parametro s* era per un socket di datagramma.<br/>                                                                   |
| <dl> <dt>**[Wsaenotsock](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il descrittore non è un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

La [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione socket **SO \_ KEEPALIVE** consente a un'applicazione di recuperare lo stato corrente dell'opzione keepalive, anche se questa funzionalità non viene usata normalmente. Se un'applicazione deve abilitare i pacchetti keepalive in un socket, chiama semplicemente la [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per abilitare l'opzione .

La [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l'opzione socket **SO \_ KEEPALIVE** consente a un'applicazione di abilitare pacchetti keep-alive per una connessione socket. **\_ L'opzione SO KEEPALIVE** per un socket è disabilitata (impostata su **FALSE)** per impostazione predefinita.

Quando questa opzione socket è abilitata, lo stack TCP invia pacchetti keep-alive quando non sono stati ricevuti pacchetti di dati o di riconoscimento per la connessione entro un intervallo. Per altre informazioni sull'opzione keep-alive, vedere la sezione 4.2.3.6 in Requisiti per gli host *Internet -* Livelli di comunicazione specificati in RFC 1122 disponibile nel sito Web [IETF](https://www.ietf.org/rfc/rfc1122.txt). Questa risorsa può essere disponibile solo in inglese.

L'opzione socket **\_ SO KEEPALIVE** è valida solo per i protocolli che supportano la nozione di keep-alive (protocolli orientati alla connessione). Per TCP, il timeout keep-alive predefinito è 2 ore e l'intervallo keep-alive è 1 secondo. Il numero predefinito di probe keep-alive varia in base alla versione di Windows.

Il [**codice di controllo SIO \_ KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) può essere usato per abilitare o disabilitare il keep-alive e modificare il timeout e l'intervallo per una singola connessione. Se keep-alive è abilitato con **SO \_ KEEPALIVE,** le impostazioni TCP predefinite vengono usate per il timeout e l'intervallo keep-alive a meno che questi valori non siano stati modificati usando **SIO \_ KEEPALIVE \_ VALS**.

Il valore predefinito a livello di sistema del timeout keep-alive è controllabile tramite l'impostazione del Registro di sistema [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) che accetta un valore in millisecondi. Il valore predefinito a livello di sistema dell'intervallo keep-alive è controllabile tramite l'impostazione del Registro di sistema [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) che accetta un valore in millisecondi.

In Windows Vista e versioni successive, il numero di probe keep-alive (ritrasmissioni dei dati) è impostato su 10 e non può essere modificato.

In Windows Server 2003, Windows XP e Windows 2000, l'impostazione predefinita per il numero di probe keep-alive è 5. Il numero di probe keep-alive è controllabile tramite le impostazioni del Registro di sistema [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) e [PPTPTcpMaxDataRetransmissions.](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) Il numero di probe keep-alive è impostato sul valore più grande dei due valori delle chiavi del Registro di sistema. Se questo numero è 0, i probe keep-alive non verranno inviati. Se questo numero è superiore a 255, viene regolato a 255.

In Windows Vista e versioni successive, l'opzione socket **SO \_ KEEPALIVE** può essere impostata solo usando la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando il socket si trova in uno stato noto e non in uno stato di transizione. Per TCP, l'opzione socket **\_ SO KEEPALIVE** deve essere impostata prima che venga chiamata la funzione connect ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) o dopo il completamento della richiesta di connessione. Se la funzione connect è stata chiamata in modo asincrono, è necessario attendere il completamento della connessione prima di provare a impostare l'opzione socket **SO \_ KEEPALIVE.** Se un'applicazione tenta di impostare l'opzione socket **SO \_ KEEPALIVE** quando una richiesta di connessione è ancora in corso, la funzione **setsockopt** avrà esito negativo e restituirà [WSAEINVAL](windows-sockets-error-codes-2.md).

In Windows Server 2003, Windows XP e Windows 2000, l'opzione socket **SO \_ KEEPALIVE** può essere impostata usando la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando il socket è uno stato di transizione (una richiesta di connessione è ancora in corso) e uno stato noto.

Si noti che il file di intestazione *Ws2def.h* viene incluso automaticamente in *Winsock2.h* e non deve mai essere usato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Ws2def.h (include Winsock2.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))
</dt> <dt>

[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))
</dt> <dt>

[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))
</dt> <dt>

[**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**SIO \_ KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))
</dt> <dt>

[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
