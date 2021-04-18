---
description: È progettato per consentire a un'applicazione di abilitare i pacchetti Keep-Alive per una connessione socket.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: Opzione socket SO_KEEPALIVE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315776"
---
# <a name="so_keepalive-socket-option"></a>\_Opzione socket KeepAlive

L'opzione per il socket **\_ KeepAlive** è progettata per consentire a un'applicazione di abilitare i pacchetti Keep-Alive per una connessione socket.

Per eseguire una query sullo stato di questa opzione socket, chiamare la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Per impostare questa opzione, chiamare la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con i parametri seguenti.

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

*livello* \[ di in\]
</dt> <dd>

Livello in corrispondenza del quale è definita l'opzione. Usare **il \_ socket Sol** per questa operazione.

</dd> <dt>

*optname* \[ in\]
</dt> <dd>

Opzione socket per la quale deve essere impostato il valore. Usare **così \_ KeepAlive** per questa operazione.

</dd> <dt>

*optVal* \[ out\]
</dt> <dd>

Puntatore al buffer che contiene il valore per l'opzione da impostare. Questo parametro deve puntare a un buffer uguale o maggiore della dimensione di un valore **DWORD** .

Questo valore viene considerato come un valore booleano con 0 usato per indicare **false** (disabilitato) e un valore diverso da zero per indicare **true** (abilitato).

</dd> <dt>

*optlen* \[ in uscita\]
</dt> <dd>

Puntatore alla dimensione, in byte, del buffer *optVal* . Questa dimensione deve essere maggiore o uguale alla dimensione di un valore **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) restituisce zero.

Se l'operazione ha esito negativo, viene restituito un valore di \_ errore socket e un codice di errore specifico può essere recuperato chiamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Codice di errore                                                                                                                                              | Significato                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Prima di utilizzare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il sottosistema di rete non è riuscito.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno dei parametri *optVal* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio degli indirizzi utente. Questo errore viene restituito anche se il valore a cui punta il parametro *optlen* è minore della dimensione di un valore **DWORD** .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | È in corso una chiamata di blocco di Windows Sockets 1,1 o il provider di servizi sta ancora elaborando una funzione di callback.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Il parametro *Level* è sconosciuto o non valido. In Windows Vista e versioni successive questo errore viene restituito anche se il socket si trovava in uno stato di transizione.<br/>                                                                                                 |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata. Questo errore viene restituito se il descrittore di socket passato al parametro *s* era per un socket di datagramma.<br/>                                                                   |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il descrittore non è un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

La funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione di socket **Keep- \_ Alive** consente a un'applicazione di recuperare lo stato corrente dell'opzione KeepAlive, anche se questa funzionalità non viene normalmente utilizzata. Se un'applicazione deve abilitare i pacchetti KeepAlive in un socket, viene semplicemente chiamata la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per abilitare l'opzione.

La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l'opzione di socket **\_ Keep** -Alive consente a un'applicazione di abilitare i pacchetti Keep-Alive per una connessione socket. Per impostazione predefinita, l'opzione **\_ Keep-Alive** per un socket è disabilitata (impostata su **false**).

Quando questa opzione socket è abilitata, lo stack TCP invia pacchetti keep-alive quando non sono stati ricevuti pacchetti di dati o di riconoscimento per la connessione entro un intervallo. Per ulteriori informazioni sull'opzione Keep-Alive, vedere la sezione 4.2.3.6 in *requisiti per gli host Internet-livelli di comunicazione* specificati in RFC 1122 disponibili sul [sito Web IETF](https://www.ietf.org/rfc/rfc1122.txt). Questa risorsa può essere disponibile solo in inglese.

Questa **opzione \_** è valida solo per i protocolli che supportano il concetto di Keep-Alive (protocolli orientati alla connessione). Per TCP, il timeout keep-alive predefinito è 2 ore e l'intervallo keep-alive è di 1 secondo. Il numero predefinito di probe Keep-Alive varia in base alla versione di Windows.

Il codice di controllo di [**sio \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) può essere usato per abilitare o disabilitare Keep-Alive e modificare il timeout e l'intervallo per una singola connessione. Se Keep-Alive è abilitato con **così \_ KeepAlive**, le impostazioni TCP predefinite vengono usate per il timeout e l'intervallo keep-alive, a meno che tali valori non siano stati modificati usando **sio \_ KeepAlive \_ Vals**.

Il valore predefinito a livello di sistema del timeout keep-alive è controllabile tramite l'impostazione del registro di sistema [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) che accetta un valore in millisecondi. Il valore predefinito a livello di sistema dell'intervallo keep-alive è controllabile tramite l'impostazione del registro di sistema [keepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) che accetta un valore in millisecondi.

In Windows Vista e versioni successive, il numero di probe Keep-Alive (ritrasmissioni dati) è impostato su 10 e non può essere modificato.

In Windows Server 2003, Windows XP e Windows 2000, l'impostazione predefinita per numero di probe Keep-Alive è 5. Il numero di probe Keep-Alive è controllabile tramite le impostazioni del registro di sistema [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) e [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) . Il numero di probe Keep-Alive è impostato sul valore più elevato tra i due valori della chiave del registro di sistema. Se questo numero è 0, i probe Keep-Alive non verranno inviati. Se questo numero è superiore a 255, viene impostato su 255.

In Windows Vista e versioni successive, l'opzione di socket **\_ Keep-Alive** può essere impostata solo utilizzando la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando il socket è in uno stato noto, non è uno stato di transizione. Per TCP, l'opzione di socket **\_ Keep-Alive** deve essere impostata prima di chiamare la funzione Connect ([**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) o dopo il completamento della richiesta di connessione. Se la funzione Connect è stata chiamata in modo asincrono, è necessario attendere il completamento della connessione prima di tentare di impostare l'opzione del socket **\_ Keep-Alive** . Se un'applicazione tenta di impostare l'opzione di socket **\_ Keep-Alive** quando una richiesta di connessione è ancora in corso, la funzione **setsockopt** avrà esito negativo e restituirà [WSAEINVAL](windows-sockets-error-codes-2.md).

In Windows Server 2003, Windows XP e Windows 2000 è possibile impostare l'opzione di socket **\_ Keep-Alive** utilizzando la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando il socket è uno stato di transizione (una richiesta di connessione è ancora in corso) e uno stato noto.

Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Ws2def. h (include Winsock2. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))
</dt> <dt>

[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))
</dt> <dt>

[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))
</dt> <dt>

[**presa**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**KeepAlive di SIO \_ \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))
</dt> <dt>

[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
