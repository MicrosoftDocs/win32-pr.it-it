---
description: È progettato per consentire a un'applicazione di decidere se accettare o meno una connessione in ingresso su un socket in ascolto.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: Opzione socket SO_CONDITIONAL_ACCEPT (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315777"
---
# <a name="so_conditional_accept-socket-option"></a>\_ \_ Opzione socket Accept condizionale

L'opzione del socket **\_ \_ Accept condizionale** è progettata per consentire a un'applicazione di decidere se accettare o meno una connessione in ingresso su un socket di ascolto.

## <a name="socket-option-value"></a>Valore dell'opzione socket

La costante che rappresenta questa opzione socket è 0x3002.

## <a name="syntax"></a>Sintassi


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
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

Opzione socket per la quale deve essere impostato il valore. Usare **così \_ l' \_ accettazione condizionale** per questa operazione.

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
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Il parametro *Level* è sconosciuto o non valido. Questo errore viene restituito anche se il socket si trova già in uno stato di attesa.<br/>                                                                                                                        |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata.<br/>                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il descrittore non è un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l'opzione per il socket **\_ \_ Accept condizionale** consente a un'applicazione di decidere se accettare o meno una connessione in ingresso su un socket di ascolto. Per impostazione predefinita, l'opzione Accept condizionale per un socket è disabilitata (impostata su **false**).

Quando questa opzione socket è abilitata, lo stack TCP non accetta automaticamente le connessioni. Attende che l'applicazione indichi che accetta la connessione tramite il callback Accept condizionale registrato con la funzione [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) . Una volta ricevuta una richiesta di connessione, Winsock richiama il callback Accept condizionale registrato dall'applicazione. Solo quando il callback Accept condizionale restituisce **CF \_ Accept** , Winsock notifica al trasporto di accettare completamente la connessione.

Quando l'opzione per il socket **\_ \_ Accept condizionale** è impostata su Enabled (impostata su **true**), questo ha diversi effetti collaterali sul socket:

-   In questo modo vengono disabilitate le difese di protezione degli attacchi SYN predefinite dello stack TCP, perché l'applicazione sta assumendo la proprietà di accettare le connessioni.
-   In questo modo, il backlog di ascolto viene disabilitato perché non sono accettate connessioni per conto di un socket in ascolto. Una connessione non viene mai completamente accettata finché l'applicazione non accetta completamente l'utilizzo del meccanismo di **\_ accettazione CF** .
-   Ciò significa anche che l'applicazione deve essere sempre in uno stato per gestire prontamente i callback Accept per accettare la connessione. Se l'applicazione è occupata da un'altra elaborazione, potrebbe verificarsi il timeout del lato client prima che l'applicazione accetti effettivamente la connessione. Questo comporta un'esperienza client scadente.

In genere, il motivo principale per cui le applicazioni utilizzano l'accettazione condizionale è quello di controllare la porta o l'indirizzo IP di origine utilizzato dal client che si connette, quindi decidere di accettare o rifiutare la connessione. Tuttavia, è probabile che le prestazioni delle applicazioni siano migliori se l' \_ opzione di accettazione condizionale \_ non è abilitata e l'applicazione consente allo stack TCP e al backlog di ascolto di funzionare come previsto. Quando l'applicazione gestisce la connessione accettata, se è da un indirizzo di origine IP o da una porta non corretta, l'applicazione può semplicemente chiudere il socket. Lo svantaggio di sicurezza di questo comportamento è che ora il client è in grado di confermare che l'applicazione è in ascolto su un indirizzo IP e una porta poiché ha chiuso forzatamente la connessione accettata in precedenza. Tuttavia, gli svantaggi dell'abilitazione **dell' \_ \_ accettazione condizionale** sono in genere superiori a questa limitazione.

La funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione di socket **\_ \_ Accept condizionale** consente a un'applicazione di recuperare lo stato corrente dell'opzione Accept condizionale, anche se questa funzionalità non viene normalmente utilizzata. Se un'applicazione deve abilitare l'accettazione condizionale su un socket, viene semplicemente chiamata la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per abilitare l'opzione.

Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Ws2def. h (include Winsock2. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




