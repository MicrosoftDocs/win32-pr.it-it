---
description: Windows Codici di errore socket (Winsock) restituiti dalla funzione WSAGetLastError.
ms.assetid: 50b924f3-2c88-443b-8a90-4293fe5c3048
title: Windows Codici di errore dei socket (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece53093e7aca31d9d883680005f92ca8b30a76120209affb4dba42d6826d0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322004"
---
# <a name="windows-sockets-error-codes"></a>Windows Codici di errore dei socket

La Windows socket 2 non restituisce la causa specifica di un errore quando la funzione restituisce un risultato. Per informazioni, vedere [l'argomento Gestione degli errori Winsock.](handling-winsock-errors.md)

La [**funzione WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce l'ultimo errore che si è verificato per il thread chiamante. Quando una particolare Windows Sockets indica che si è verificato un errore, questa funzione deve essere chiamata immediatamente per recuperare il codice di errore esteso per la chiamata di funzione non riuscita. Questi codici di errore e una breve descrizione di testo associata a un codice di errore sono definiti nel file *di intestazione Winerror.h.* La [**funzione FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) può essere usata per ottenere la stringa di messaggio per l'errore restituito.

Per informazioni su come gestire i codici di errore durante la portabilità di applicazioni socket in Winsock, vedere Codici di errore [- errno, h \_ errno e WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md).

Nell'elenco seguente vengono descritti i possibili codici di errore restituiti [**dalla funzione WSAGetLastError.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) Gli errori sono elencati in ordine numerico con il nome della macro di errore. Alcuni codici di errore definiti nel file *di intestazione Winsock2.h* non vengono restituiti da alcuna funzione.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice/valore restituito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="WSA_INVALID_HANDLE"></span><span id="wsa_invalid_handle"></span><dl> <dt><strong>WSA_INVALID_HANDLE</strong></dt> <dt>6</dt> </dl></td>
<td><dl> <dt><span id="Specified_event_object_handle_is_invalid."></span><span id="specified_event_object_handle_is_invalid."></span><span id="SPECIFIED_EVENT_OBJECT_HANDLE_IS_INVALID."></span>L'handle dell'oggetto evento specificato non è valido.</dt> <dd> Un'applicazione tenta di usare un oggetto evento, ma l'handle specificato non è valido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span><dl> <dt><strong>WSA_NOT_ENOUGH_MEMORY</strong></dt> <dt>8</dt> </dl></td>
<td><dl> <dt><span id="Insufficient_memory_available."></span><span id="insufficient_memory_available."></span><span id="INSUFFICIENT_MEMORY_AVAILABLE."></span>Memoria disponibile insufficiente.</dt> <dd> In un'applicazione è stata Windows una funzione Sockets che esegue direttamente il mapping a Windows funzione. La Windows funzione indica una mancanza di risorse di memoria necessarie.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_INVALID_PARAMETER"></span><span id="wsa_invalid_parameter"></span><dl> <dt><strong>WSA_INVALID_PARAMETER</strong></dt> <dt>87</dt> </dl></td>
<td><dl> <dt><span id="One_or_more_parameters_are_invalid."></span><span id="one_or_more_parameters_are_invalid."></span><span id="ONE_OR_MORE_PARAMETERS_ARE_INVALID."></span>Uno o più parametri non sono validi.</dt> <dd> In un'applicazione è stata Windows una funzione Sockets che esegue direttamente il mapping a una Windows funzione. La Windows funzione indica un problema con uno o più parametri.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span><dl> <dt><strong>WSA_OPERATION_ABORTED</strong></dt> <dt>995</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_operation_aborted."></span><span id="overlapped_operation_aborted."></span><span id="OVERLAPPED_OPERATION_ABORTED."></span>Operazione sovrapposta interrotta.</dt> <dd> Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando SIO_FLUSH in <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_IO_INCOMPLETE"></span><span id="wsa_io_incomplete"></span><dl> <dt><strong>WSA_IO_INCOMPLETE</strong></dt> <dt>996</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_I_O_event_object_not_in_signaled_state."></span><span id="overlapped_i_o_event_object_not_in_signaled_state."></span><span id="OVERLAPPED_I_O_EVENT_OBJECT_NOT_IN_SIGNALED_STATE."></span>Oggetto evento di I/O sovrapposto non in stato segnalato.</dt> <dd> L'applicazione ha tentato di determinare lo stato di un'operazione sovrapposta che non è ancora stata completata. Le applicazioni che usano <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult"><strong>WSAGetOverlappedResult</strong></a> (con il flag <em>fWait</em> impostato su <strong>FALSE)</strong>in modalità di polling per determinare quando un'operazione sovrapposta è stata completata, ottenere questo codice di errore fino al completamento dell'operazione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_IO_PENDING"></span><span id="wsa_io_pending"></span><dl> <dt><strong>WSA_IO_PENDING</strong></dt> <dt>997</dt> </dl></td>
<td>Le operazioni sovrapposte verranno completate in un secondo momento. <br/> <dl> <dt><span></span></dt> <dd> È stata avviata un'operazione sovrapposta che non è possibile completare immediatamente. Un'indicazione di completamento verrà specificata in un secondo momento al termine dell'operazione.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINTR"></span><span id="wsaeintr"></span><dl> <dt><strong>WSAEINTR</strong></dt> <dt>10004</dt> </dl></td>
<td><dl> <dt><span id="Interrupted_function_call."></span><span id="interrupted_function_call."></span><span id="INTERRUPTED_FUNCTION_CALL."></span>Chiamata di funzione interrotta.</dt> <dd> Un'operazione di blocco è stata interrotta da una chiamata a <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall.</a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEBADF"></span><span id="wsaebadf"></span><dl> <dt><strong>WSAEBADF</strong></dt> <dt>10009</dt> </dl></td>
<td><dl> <dt><span id="File_handle_is_not_valid."></span><span id="file_handle_is_not_valid."></span><span id="FILE_HANDLE_IS_NOT_VALID."></span>Handle di file non valido.</dt> <dd> L'handle di file specificato non è valido. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEACCES"></span><span id="wsaeacces"></span><dl> <dt><strong>WSAEACCES</strong></dt> <dt>10013</dt> </dl></td>
<td><dl> <dt><span id="Permission_denied."></span><span id="permission_denied."></span><span id="PERMISSION_DENIED."></span>Autorizzazione negata.</dt> <dd> Si è tentato di accedere a un socket in un modo non consentito dalle relative autorizzazioni di accesso. Un esempio è l'uso di un indirizzo di trasmissione per <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> senza l'autorizzazione di trasmissione impostata tramite <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a>(SO_BROADCAST). <br/> Un altro possibile motivo dell'errore WSAEACCES è che quando viene chiamata la funzione di associazione (in Windows NT 4.0 con SP4 e versioni successive), un altro driver in modalità applicazione, servizio o kernel è associato allo stesso indirizzo con accesso esclusivo. <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong></strong></a> Tale accesso esclusivo è una nuova funzionalità di Windows NT 4.0 con SP4 e versioni successive e viene implementato usando <a href="/windows/desktop/winsock/so-exclusiveaddruse">l'opzione SO_EXCLUSIVEADDRUSE.</a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEFAULT"></span><span id="wsaefault"></span><dl> <dt><strong>WSAEFAULT</strong></dt> <dt>10014</dt> </dl></td>
<td><dl> <dt><span id="Bad_address."></span><span id="bad_address."></span><span id="BAD_ADDRESS."></span>Indirizzo non valido.</dt> <dd> Il sistema ha rilevato un indirizzo puntatore non valido nel tentativo di usare un argomento puntatore di una chiamata. Questo errore si verifica se un'applicazione passa un valore di puntatore non valido o se la lunghezza del buffer è troppo piccola. Ad esempio, se la lunghezza di un argomento, ovvero una struttura <a href="/windows/desktop/winsock/sockaddr-2"><strong>sockaddr,</strong></a> è inferiore a sizeof(sockaddr).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVAL"></span><span id="wsaeinval"></span><dl> <dt><strong>WSAEINVAL</strong></dt> <dt>10022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_argument."></span><span id="invalid_argument."></span><span id="INVALID_ARGUMENT."></span>Argomento non valido.</dt> <dd> È stato fornito un argomento non valido , ad esempio specificando un livello non valido per la <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>funzione setsockopt.</strong></a> In alcuni casi, si riferisce anche allo stato corrente del socket, ad esempio la chiamata di <a href="/windows/desktop/api/Winsock2/nf-winsock2-accept"><strong>accept</strong></a> su un socket che non è in ascolto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMFILE"></span><span id="wsaemfile"></span><dl> <dt><strong>WSAEMFILE</strong></dt> <dt>10024</dt> </dl></td>
<td><dl> <dt><span id="Too_many_open_files."></span><span id="too_many_open_files."></span><span id="TOO_MANY_OPEN_FILES."></span>Troppi file aperti.</dt> <dd> Troppi socket aperti. Ogni implementazione può avere un numero massimo di handle di socket disponibili, a livello globale, per processo o per thread.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span><dl> <dt><strong>WSAEWOULDBLOCK</strong></dt> <dt>10035</dt> </dl></td>
<td><dl> <dt><span id="Resource_temporarily_unavailable."></span><span id="resource_temporarily_unavailable."></span><span id="RESOURCE_TEMPORARILY_UNAVAILABLE."></span>Risorsa temporaneamente non disponibile.</dt> <dd> Questo errore viene restituito da operazioni su socket non bloccanti che non possono essere completati immediatamente, ad esempio <a href="/windows/desktop/api/winsock/nf-winsock-recv"><strong>recv</strong></a> quando non viene accodato alcun dato da leggere dal socket. Si tratta di un errore non irreversibile e l'operazione deve essere ritentata in un secondo momento. È normale che WSAEWOULDBLOCK sia segnalato come <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong></strong></a> risultato della chiamata di connect su un socket SOCK_STREAM non bloccante, poiché deve trascorrere del tempo prima che la connessione sia stabilita.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span><dl> <dt><strong>WSAEINPROGRESS</strong></dt> <dt>10036</dt> </dl></td>
<td><dl> <dt><span id="Operation_now_in_progress."></span><span id="operation_now_in_progress."></span><span id="OPERATION_NOW_IN_PROGRESS."></span>Operazione in corso.</dt> <dd> È in corso un'operazione di blocco. Windows I socket consentono solo l'attesa di una singola operazione di blocco, per attività o thread, e se viene eseguita qualsiasi altra chiamata di funzione (indipendentemente dal fatto che faccia riferimento a tale o a qualsiasi altro socket), la funzione ha esito negativo con l'errore WSAEINPROGRESS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEALREADY"></span><span id="wsaealready"></span><dl> <dt><strong>WSAEALREADY</strong></dt> <dt>10037</dt> </dl></td>
<td><dl> <dt><span id="Operation_already_in_progress."></span><span id="operation_already_in_progress."></span><span id="OPERATION_ALREADY_IN_PROGRESS."></span>Operazione già in corso.</dt> <dd> È stata tentata un'operazione su un socket non bloccante <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong></strong></a> con un'operazione già in corso, ovvero la chiamata di connect una seconda volta su un socket non bloccante già connesso o l'annullamento di una richiesta asincrona (<strong>WSAAsyncGetXbyY</strong>) che è già stata annullata o completata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span><dl> <dt><strong>WSAENOTSOCK</strong></dt> <dt>10038</dt> </dl></td>
<td><dl> <dt><span id="Socket_operation_on_nonsocket."></span><span id="socket_operation_on_nonsocket."></span><span id="SOCKET_OPERATION_ON_NONSOCKET."></span>Operazione socket su nonsocket.</dt> <dd> È stata tentata un'operazione su un elemento che non è un socket. Il parametro dell'handle del socket non fa riferimento a un socket valido oppure, <strong>per</strong> <a href="/windows/desktop/api/Winsock2/nf-winsock2-select"><strong>select,</strong></a>un membro di un fd_set non è valido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span><dl> <dt><strong>WSAEDESTADDRREQ</strong></dt> <dt>10039</dt> </dl></td>
<td><dl> <dt><span id="Destination_address_required."></span><span id="destination_address_required."></span><span id="DESTINATION_ADDRESS_REQUIRED."></span>Indirizzo di destinazione obbligatorio.</dt> <dd> Un indirizzo obbligatorio è stato omesso da un'operazione su un socket. Ad esempio, questo errore viene restituito se <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> viene chiamato con l'indirizzo remoto di ADDR_ANY.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span><dl> <dt><strong>WSAEMSGSIZE</strong></dt> <dt>10040</dt> </dl></td>
<td><dl> <dt><span id="Message_too_long."></span><span id="message_too_long."></span><span id="MESSAGE_TOO_LONG."></span>Messaggio troppo lungo.</dt> <dd> Un messaggio inviato su un socket di datagramma è più grande del buffer dei messaggi interno o di un altro limite di rete oppure il buffer utilizzato per ricevere un datagramma è inferiore al datagramma stesso.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span><dl> <dt><strong>WSAEPROTOTYPE</strong></dt> <dt>10041</dt> </dl></td>
<td><dl> <dt><span id="Protocol_wrong_type_for_socket."></span><span id="protocol_wrong_type_for_socket."></span><span id="PROTOCOL_WRONG_TYPE_FOR_SOCKET."></span>Tipo di protocollo errato per il socket.</dt> <dd> Nella chiamata di funzione socket è stato <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>specificato</strong></a> un protocollo che non supporta la semantica del tipo di socket richiesto. Ad esempio, il protocollo UDP Internet ARPA non può essere specificato con un tipo di socket SOCK_STREAM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span><dl> <dt><strong>WSAENOPROTOOPT</strong></dt> <dt>10042</dt> </dl></td>
<td><dl> <dt><span id="Bad_protocol_option."></span><span id="bad_protocol_option."></span><span id="BAD_PROTOCOL_OPTION."></span>Opzione di protocollo non valida.</dt> <dd> In una chiamata <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt"><strong>getsockopt</strong></a> o <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> è stata specificata un'opzione o un livello sconosciuto, non valido o non supportato.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span><dl> <dt><strong>WSAEPROTONOSUPPORT</strong></dt> <dt>10043</dt> </dl></td>
<td><dl> <dt><span id="Protocol_not_supported."></span><span id="protocol_not_supported."></span><span id="PROTOCOL_NOT_SUPPORTED."></span>Protocollo non supportato.</dt> <dd> Il protocollo richiesto non è stato configurato nel sistema o non esiste alcuna implementazione per esso. Ad esempio, una <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>chiamata socket</strong></a> richiede un SOCK_DGRAM socket, ma specifica un protocollo di flusso.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span><dl> <dt><strong>WSAESOCKTNOSUPPORT</strong></dt> <dt>10044</dt> </dl></td>
<td><dl> <dt><span id="Socket_type_not_supported."></span><span id="socket_type_not_supported."></span><span id="SOCKET_TYPE_NOT_SUPPORTED."></span>Tipo di socket non supportato.</dt> <dd> Il supporto per il tipo di socket specificato non esiste in questa famiglia di indirizzi. Ad esempio, il tipo facoltativo SOCK_RAW essere selezionato in una chiamata <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>socket</strong></a> e l'implementazione non supporta affatto SOCK_RAW socket.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span><dl> <dt><strong>WSAEOPNOTSUPP</strong></dt> <dt>10045</dt> </dl></td>
<td><dl> <dt><span id="Operation_not_supported."></span><span id="operation_not_supported."></span><span id="OPERATION_NOT_SUPPORTED."></span>Operazione non supportata.</dt> <dd> L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento. In genere ciò si verifica quando un descrittore socket a un socket che non supporta questa operazione tenta di accettare una connessione in un socket di datagramma.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span><dl> <dt><strong>WSAEPFNOSUPPORT</strong></dt> <dt>10046</dt> </dl></td>
<td><dl> <dt><span id="Protocol_family_not_supported."></span><span id="protocol_family_not_supported."></span><span id="PROTOCOL_FAMILY_NOT_SUPPORTED."></span>Famiglia di protocolli non supportata.</dt> <dd> La famiglia di protocolli non è stata configurata nel sistema o non esiste alcuna implementazione. Questo messaggio ha un significato leggermente diverso da WSAEAFNOSUPPORT. Tuttavia, è intercambiabile nella maggior parte dei casi e tutte le funzioni socket Windows che restituiscono uno di questi messaggi specificano anche WSAEAFNOSUPPORT.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span><dl> <dt><strong>WSAEAFNOSUPPORT</strong></dt> <dt>10047</dt> </dl></td>
<td><dl> <dt><span id="Address_family_not_supported_by_protocol_family."></span><span id="address_family_not_supported_by_protocol_family."></span><span id="ADDRESS_FAMILY_NOT_SUPPORTED_BY_PROTOCOL_FAMILY."></span>Famiglia di indirizzi non supportata dalla famiglia di protocolli.</dt> <dd> È stato usato un indirizzo incompatibile con il protocollo richiesto. Tutti i socket vengono creati con una famiglia di indirizzi associata(ovvero, AF_INET per i protocolli Internet) e un tipo di protocollo generico (ovvero, SOCK_STREAM). Questo errore viene restituito se nella chiamata <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>socket</strong></a> viene richiesto in modo esplicito un protocollo non corretto o se viene usato un indirizzo della famiglia errata per un socket, ad esempio in <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span><dl> <dt><strong>WSAEADDRINUSE</strong></dt> <dt>10048</dt> </dl></td>
<td><dl> <dt><span id="Address_already_in_use."></span><span id="address_already_in_use."></span><span id="ADDRESS_ALREADY_IN_USE."></span>Indirizzo già in uso.</dt> <dd> In genere, è consentito un solo utilizzo di ogni indirizzo socket (protocollo/indirizzo IP/porta). Questo errore si verifica se un'applicazione tenta di associare un socket <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>a</strong></a> un indirizzo IP/porta già usato per un socket esistente o un socket che non è stato chiuso correttamente o uno ancora in corso di chiusura. Per le applicazioni server che devono <strong>associare</strong> più socket allo stesso numero di porta, è consigliabile usare <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> (SO_REUSEADDR). Le applicazioni client in genere non devono chiamare <strong>l'associazione.</strong> <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>La connessione</strong></a> sceglie automaticamente una porta non utilizzata. Quando <strong>l'associazione</strong> viene chiamata con un indirizzo con caratteri jolly (ADDR_ANY), un errore WSAEADDRINUSE può essere ritardato fino a quando non viene eseguito il commit dell'indirizzo specifico. Ciò potrebbe verificarsi con una chiamata a un'altra funzione in un secondo momento, tra cui <strong>connect</strong>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-listen"><strong>listen</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect</strong></a>o <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span><dl> <dt><strong>WSAEADDRNOTAVAIL</strong></dt> <dt>10049</dt> </dl></td>
<td><dl> <dt><span id="Cannot_assign_requested_address."></span><span id="cannot_assign_requested_address."></span><span id="CANNOT_ASSIGN_REQUESTED_ADDRESS."></span>Impossibile assegnare l'indirizzo richiesto.</dt> <dd> L'indirizzo richiesto non è valido nel contesto. Ciò in genere è il risultato di un <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>tentativo di</strong></a> associazione a un indirizzo non valido per il computer locale. Ciò può derivare anche da <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>connect</strong></a>, <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf</strong></a>o <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsasendto"><strong>WSASendTo</strong></a> quando l'indirizzo remoto o la porta non è valida per un computer remoto (ad esempio, indirizzo o porta 0).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span><dl> <dt><strong>WSAENETDOWN</strong></dt> <dt>10050</dt> </dl></td>
<td><dl> <dt><span id="Network_is_down."></span><span id="network_is_down."></span><span id="NETWORK_IS_DOWN."></span>La rete non è disponibile.</dt> <dd> Rete inattiva rilevata durante l'operazione del socket. Ciò potrebbe indicare un guasto grave del sistema di rete (vale a dire, lo stack del protocollo su cui viene eseguito Windows Sockets.dll), dell'interfaccia di rete o della stessa rete locale.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span><dl> <dt><strong>WSAENETUNREACH</strong></dt> <dt>10051</dt> </dl></td>
<td><dl> <dt><span id="Network_is_unreachable."></span><span id="network_is_unreachable."></span><span id="NETWORK_IS_UNREACHABLE."></span>La rete non è raggiungibile.</dt> <dd> È stata tentata un'operazione socket in una rete non raggiungibile. Questo significa in genere che il software locale non conosce alcuna route per raggiungere l'host remoto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETRESET"></span><span id="wsaenetreset"></span><dl> <dt><strong>WSAENETRESET</strong></dt> <dt>10052</dt> </dl></td>
<td><dl> <dt><span id="Network_dropped_connection_on_reset."></span><span id="network_dropped_connection_on_reset."></span><span id="NETWORK_DROPPED_CONNECTION_ON_RESET."></span>Connessione di rete eliminata al ripristino.</dt> <dd> La connessione è stata interrotta a causa di un'attività keep-alive che rileva un errore durante l'operazione. Può anche essere restituito da <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> se viene effettuato un tentativo di impostare SO_KEEPALIVE <a href="/windows/desktop/winsock/so-keepalive"><strong>su</strong></a> una connessione che ha già avuto esito negativo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span><dl> <dt><strong>WSAECONNABORTED</strong></dt> <dt>10053</dt> </dl></td>
<td><dl> <dt><span id="Software_caused_connection_abort."></span><span id="software_caused_connection_abort."></span><span id="SOFTWARE_CAUSED_CONNECTION_ABORT."></span>Il software ha causato l'interruzione della connessione.</dt> <dd> Una connessione stabilita è stata interrotta dal software nel computer host, probabilmente a causa di un timeout della trasmissione dei dati o di un errore di protocollo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span><dl> <dt><strong>WSAECONNRESET</strong></dt> <dt>10054</dt> </dl></td>
<td><dl> <dt><span id="Connection_reset_by_peer."></span><span id="connection_reset_by_peer."></span><span id="CONNECTION_RESET_BY_PEER."></span>Reimpostazione della connessione in base al peer.</dt> <dd> Connessione in corso interrotta forzatamente dall'host remoto. Ciò si verifica in genere se l'applicazione peer nell'host remoto viene improvvisamente arrestata, l'host viene riavviato, l'host o l'interfaccia di rete remota è disabilitata o l'host remoto usa una chiusura rigida (vedere <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> per altre informazioni sull'opzione SO_LINGER nel socket remoto). Questo errore può verificarsi anche se una connessione è stata interrotta a causa di un'attività keep-alive che rileva un errore durante una o più operazioni in corso. Le operazioni in corso hanno esito negativo con WSAENETRESET. Le operazioni successive hanno esito negativo con WSAECONNRESET.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span><dl> <dt><strong>WSAENOBUFS</strong></dt> <dt>10055</dt> </dl></td>
<td><dl> <dt><span id="No_buffer_space_available."></span><span id="no_buffer_space_available."></span><span id="NO_BUFFER_SPACE_AVAILABLE."></span>Non è disponibile spazio nel buffer.</dt> <dd> Non è stato possibile eseguire un'operazione su un socket perché il sistema non dispone di spazio nel buffer sufficiente o perché una coda era piena.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEISCONN"></span><span id="wsaeisconn"></span><dl> <dt><strong>WSAEISCONN</strong></dt> <dt>10056</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_already_connected."></span><span id="socket_is_already_connected."></span><span id="SOCKET_IS_ALREADY_CONNECTED."></span>Il socket è già connesso.</dt> <dd> È stata effettuata una richiesta di connessione in un socket già connesso. Alcune implementazioni restituiscono anche questo errore se <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> viene chiamato su un socket SOCK_DGRAM connesso (per i socket SOCK_STREAM, il <em>parametro to</em> in <strong>sendto</strong> viene ignorato), anche se altre implementazioni lo trattano come un evento legale.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span><dl> <dt><strong>WSAENOTCONN</strong></dt> <dt>10057</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_not_connected."></span><span id="socket_is_not_connected."></span><span id="SOCKET_IS_NOT_CONNECTED."></span>Il socket non è connesso.</dt> <dd> Una richiesta di invio o ricezione di dati non è consentita perché il socket non è connesso e (quando si invia su un socket di datagrammi tramite <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>) non è stato fornito alcun indirizzo. Anche qualsiasi altro tipo di operazione potrebbe restituire questo <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>errore,</strong></a> ad esempio imposta l'impostazione SO_KEEPALIVE <a href="/windows/desktop/winsock/so-keepalive"><strong>se</strong></a> la connessione è stata reimpostata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span><dl> <dt><strong>WSAESHUTDOWN</strong></dt> <dt>10058</dt> </dl></td>
<td><dl> <dt><span id="Cannot_send_after_socket_shutdown."></span><span id="cannot_send_after_socket_shutdown."></span><span id="CANNOT_SEND_AFTER_SOCKET_SHUTDOWN."></span>Impossibile inviare dopo l'arresto del socket.</dt> <dd> Una richiesta di invio o ricezione di dati non è consentita perché il socket era già stato arrestato in tale direzione con una chiamata <a href="/windows/desktop/api/winsock/nf-winsock-shutdown"><strong>di arresto</strong></a> precedente. Chiamando <strong>shutdown viene</strong> richiesta una chiusura parziale di un socket, ovvero un segnale che invia o riceve o entrambi sono stati sospesi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span><dl> <dt><strong>WSAETOOMANYREFS</strong></dt> <dt>10059</dt> </dl></td>
<td><dl> <dt><span id="Too_many_references."></span><span id="too_many_references."></span><span id="TOO_MANY_REFERENCES."></span>Troppi riferimenti.</dt> <dd> Troppi riferimenti a un oggetto kernel.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span><dl> <dt><strong>WSAETIMEDOUT</strong></dt> <dt>10060</dt> </dl></td>
<td><dl> <dt><span id="Connection_timed_out."></span><span id="connection_timed_out."></span><span id="CONNECTION_TIMED_OUT."></span>Timeout della connessione.</dt> <dd> Un tentativo di connessione non è riuscito perché la parte connessa non ha risposto correttamente dopo un periodo di tempo oppure la connessione stabilita non è riuscita perché l'host connesso non è riuscito a rispondere.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span><dl> <dt><strong>WSAECONNREFUSED</strong></dt> <dt>10061</dt> </dl></td>
<td><dl> <dt><span id="Connection_refused."></span><span id="connection_refused."></span><span id="CONNECTION_REFUSED."></span>Connessione rifiutata.</dt> <dd> Non è stato possibile stabilire alcuna connessione perché il computer di destinazione l'ha rifiutata attivamente. Ciò si verifica in genere quando si tenta di connettersi a un servizio inattivo nell'host estraneo, ovvero senza un'applicazione server in esecuzione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAELOOP"></span><span id="wsaeloop"></span><dl> <dt><strong>WSAELOOP</strong></dt> <dt>10062</dt> </dl></td>
<td><dl> <dt><span id="Cannot_translate_name."></span><span id="cannot_translate_name."></span><span id="CANNOT_TRANSLATE_NAME."></span>Impossibile convertire il nome.</dt> <dd> Impossibile convertire un nome.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span><dl> <dt><strong>WSAENAMETOOLONG</strong></dt> <dt>10063</dt> </dl></td>
<td><dl> <dt><span id="Name_too_long."></span><span id="name_too_long."></span><span id="NAME_TOO_LONG."></span>Nome troppo lungo.</dt> <dd> Un componente del nome o un nome era troppo lungo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span><dl> <dt><strong>WSAEHOSTDOWN</strong></dt> <dt>10064</dt> </dl></td>
<td><dl> <dt><span id="Host_is_down."></span><span id="host_is_down."></span><span id="HOST_IS_DOWN."></span>L'host non è disponibile.</dt> <dd> Un'operazione socket non è riuscita perché l'host di destinazione non è disponibile. Un'operazione socket ha rilevato un host non in esecuzione. L'attività di rete nell'host locale non è stata avviata. È più probabile che queste condizioni siano indicate dall'errore WSAETIMEDOUT.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span><dl> <dt><strong>WSAEHOSTUNREACH</strong></dt> <dt>10065</dt> </dl></td>
<td><dl> <dt><span id="No_route_to_host."></span><span id="no_route_to_host."></span><span id="NO_ROUTE_TO_HOST."></span>Nessuna route da ospitare.</dt> <dd> Tentativo di operazione del socket verso un host non raggiungibile. Vedere WSAENETUNREACH.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span><dl> <dt><strong>WSAENOTEMPTY</strong></dt> <dt>10066</dt> </dl></td>
<td><dl> <dt><span id="Directory_not_empty."></span><span id="directory_not_empty."></span><span id="DIRECTORY_NOT_EMPTY."></span>Directory non vuota.</dt> <dd> Impossibile rimuovere una directory non vuota.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span><dl> <dt><strong>WSAEPROCLIM</strong></dt> <dt>10067</dt> </dl></td>
<td><dl> <dt><span id="Too_many_processes."></span><span id="too_many_processes."></span><span id="TOO_MANY_PROCESSES."></span>Troppi processi.</dt> <dd> Un Windows'implementazione di Sockets può avere un limite al numero di applicazioni che possono usarla contemporaneamente. <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> potrebbe non riuscire con questo errore se è stato raggiunto il limite.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEUSERS"></span><span id="wsaeusers"></span><dl> <dt><strong>WSAEUSERS</strong></dt> <dt>10068</dt> </dl></td>
<td><dl> <dt><span id="User_quota_exceeded."></span><span id="user_quota_exceeded."></span><span id="USER_QUOTA_EXCEEDED."></span>La quota utente è stata superata.</dt> <dd> La quota utente è esaurita. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDQUOT"></span><span id="wsaedquot"></span><dl> <dt><strong>WSAEDQUOT</strong></dt> <dt>10069</dt> </dl></td>
<td><dl> <dt><span id="Disk_quota_exceeded."></span><span id="disk_quota_exceeded."></span><span id="DISK_QUOTA_EXCEEDED."></span>Quota del disco superata.</dt> <dd> Esaurita la quota del disco. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESTALE"></span><span id="wsaestale"></span><dl> <dt><strong>WSAESTALE</strong></dt> <dt>10070</dt> </dl></td>
<td><dl> <dt><span id="Stale_file_handle_reference."></span><span id="stale_file_handle_reference."></span><span id="STALE_FILE_HANDLE_REFERENCE."></span>Riferimento all'handle di file non obsoleto.</dt> <dd> Il riferimento all'handle di file non è più disponibile. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEREMOTE"></span><span id="wsaeremote"></span><dl> <dt><strong>WSAEREMOTE</strong></dt> <dt>10071</dt> </dl></td>
<td><dl> <dt><span id="Item_is_remote."></span><span id="item_is_remote."></span><span id="ITEM_IS_REMOTE."></span>L'elemento è remoto.</dt> <dd> L'elemento non è disponibile in locale. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span><dl> <dt><strong>WSASYSNOTREADY</strong></dt> <dt>10091</dt> </dl></td>
<td><dl> <dt><span id="Network_subsystem_is_unavailable."></span><span id="network_subsystem_is_unavailable."></span><span id="NETWORK_SUBSYSTEM_IS_UNAVAILABLE."></span>Il sottosistema di rete non è disponibile.</dt> <dd> Questo errore viene restituito da <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> se l'implementazione di Windows Sockets non può funzionare in questo momento perché il sistema sottostante che usa per fornire servizi di rete non è attualmente disponibile. Gli utenti devono controllare:<br/> </dd> </dl>
<ul>
<li>Che il file DLL Windows Sockets appropriato si trova nel percorso corrente.</li>
<li>Che non stiano tentando di usare più di un'implementazione Windows Sockets contemporaneamente. Se nel sistema sono presenti più DLL Winsock, assicurarsi che la prima nel percorso sia appropriata per il sottosistema di rete attualmente caricato.</li>
<li>La Windows di implementazione di Sockets per assicurarsi che tutti i componenti necessari siano attualmente installati e configurati correttamente.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span><dl> <dt><strong>WSAVERNOTSUPPORTED</strong></dt> <dt>10092</dt> </dl></td>
<td><dl> <dt><span id="Winsock.dll_version_out_of_range."></span><span id="winsock.dll_version_out_of_range."></span><span id="WINSOCK.DLL_VERSION_OUT_OF_RANGE."></span>Winsock.dll versione non compreso nell'intervallo.</dt> <dd> L'implementazione Windows Sockets corrente non supporta la versione della specifica Windows Sockets richiesta dall'applicazione. Controllare che non vengano utilizzati file DLL di socket di Windows obsoleti.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span><dl> <dt><strong>WSANOTINITIALISED</strong></dt> <dt>10093</dt> </dl></td>
<td><dl> <dt><span id="Successful_WSAStartup_not_yet_performed."></span><span id="successful_wsastartup_not_yet_performed."></span><span id="SUCCESSFUL_WSASTARTUP_NOT_YET_PERFORMED."></span>WSAStartup riuscito non ancora eseguito.</dt> <dd> L'applicazione non ha chiamato <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup o</strong></a> <strong>WSAStartup non</strong> è riuscita. È possibile che l'applicazione stia accedendo a un socket di cui l'attività attiva corrente non è proprietaria(ovvero tenta di condividere un socket tra attività) o <a href="/windows/desktop/api/winsock/nf-winsock-wsacleanup"><strong>che WSACleanup</strong></a> sia stato chiamato troppe volte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDISCON"></span><span id="wsaediscon"></span><dl> <dt><strong>WSAEDISCON</strong></dt> <dt>10101</dt> </dl></td>
<td><dl> <dt><span id="Graceful_shutdown_in_progress."></span><span id="graceful_shutdown_in_progress."></span><span id="GRACEFUL_SHUTDOWN_IN_PROGRESS."></span>Arresto normale in corso.</dt> <dd> Restituito <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecv"><strong>da WSARecv</strong></a> e <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom"><strong>WSARecvFrom</strong></a> per indicare che l'entità remota ha avviato una sequenza di arresto normale.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOMORE"></span><span id="wsaenomore"></span><dl> <dt><strong>WSAENOMORE</strong></dt> <dt>10102</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Nessun altro risultato.</dt> <dd> Non è possibile restituire altri risultati dalla <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>funzione WSALookupServiceNext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span><dl> <dt><strong>WSAECANCELLED</strong></dt> <dt>10103</dt> </dl></td>
<td><dl> <dt><span id="Call_has_been_canceled."></span><span id="call_has_been_canceled."></span><span id="CALL_HAS_BEEN_CANCELED."></span>La chiamata è stata annullata.</dt> <dd> È stata effettuata una <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>chiamata alla funzione WSALookupServiceEnd</strong></a> durante l'elaborazione della chiamata. La chiamata è stata annullata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span><dl> <dt><strong>WSAEINVALIDPROCTABLE</strong></dt> <dt>10104</dt> </dl></td>
<td><dl> <dt><span id="Procedure_call_table_is_invalid."></span><span id="procedure_call_table_is_invalid."></span><span id="PROCEDURE_CALL_TABLE_IS_INVALID."></span>La tabella delle chiamate di procedura non è valida.</dt> <dd> La tabella delle chiamate di procedura del provider di servizi non è valida. Un provider di servizi ha restituito una tabella di procedura falsa Ws2_32.dll. Ciò è in genere causato da uno o più puntatori a <strong>funzione</strong>null.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span><dl> <dt><strong>WSAEINVALIDPROVIDER</strong></dt> <dt>10105</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_is_invalid."></span><span id="service_provider_is_invalid."></span><span id="SERVICE_PROVIDER_IS_INVALID."></span>Provider di servizi non valido.</dt> <dd> Il provider di servizi richiesto non è valido. Questo errore viene restituito dalle funzioni <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo"><strong>WSCGetProviderInfo</strong></a> e <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32"><strong>WSCGetProviderInfo32</strong></a> se non è stato possibile trovare la voce di protocollo specificata. Questo errore viene restituito anche se il provider di servizi ha restituito un numero di versione diverso dalla 2.0.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span><dl> <dt><strong>WSAEPROVIDERFAILEDINIT</strong></dt> <dt>10106</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_failed_to_initialize."></span><span id="service_provider_failed_to_initialize."></span><span id="SERVICE_PROVIDER_FAILED_TO_INITIALIZE."></span>Impossibile inizializzare il provider di servizi.</dt> <dd> Impossibile caricare o inizializzare il provider di servizi richiesto. Questo errore viene restituito se non è stato possibile caricare la DLL di un provider di servizi (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> non riuscita) o se la funzione <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup"><strong>WSPStartup</strong></a> o <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup"><strong>NSPStartup</strong></a> del provider non è riuscita.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span><dl> <dt><strong>WSASYSCALLFAILURE</strong></dt> <dt>10107</dt> </dl></td>
<td><dl> <dt><span id="System_call_failure."></span><span id="system_call_failure."></span><span id="SYSTEM_CALL_FAILURE."></span>Errore di chiamata di sistema.</dt> <dd> Una chiamata di sistema che non deve mai avere esito negativo ha avuto esito negativo. Si tratta di un codice di errore generico, restituito in diverse condizioni. <br/> Restituito quando una chiamata di sistema che non deve mai avere esito negativo ha esito negativo. Ad esempio, se una chiamata a <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents"><strong>WaitForMultipleEvents</strong></a> ha esito negativo o una delle funzioni del Registro di sistema non riesce a modificare i cataloghi di protocollo/spazio dei nomi.<br/> Restituito quando un provider non restituisce SUCCESS e non fornisce un codice di errore esteso. Può indicare un errore di implementazione del provider di servizi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span><dl> <dt><strong>WSASERVICE_NOT_FOUND</strong></dt> <dt>10108</dt> </dl></td>
<td><dl> <dt><span id="Service_not_found."></span><span id="service_not_found."></span><span id="SERVICE_NOT_FOUND."></span>Servizio non trovato.</dt> <dd> Non è noto alcun servizio di questo tipo. Impossibile trovare il servizio nello spazio dei nomi specificato.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span><dl> <dt><strong>WSATYPE_NOT_FOUND</strong></dt> <dt>10109</dt> </dl></td>
<td><dl> <dt><span id="Class_type_not_found."></span><span id="class_type_not_found."></span><span id="CLASS_TYPE_NOT_FOUND."></span>Tipo di classe non trovato.</dt> <dd> La classe specificata non è stata trovata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span><dl> <dt><strong>WSA_E_NO_MORE</strong></dt> <dt>10110</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Nessun altro risultato.</dt> <dd> Non è possibile restituire altri risultati dalla <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>funzione WSALookupServiceNext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span><dl> <dt><strong>WSA_E_CANCELLED</strong></dt> <dt>10111</dt> </dl></td>
<td><dl> <dt><span id="Call_was_canceled."></span><span id="call_was_canceled."></span><span id="CALL_WAS_CANCELED."></span>La chiamata è stata annullata.</dt> <dd> È stata effettuata una <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>chiamata alla funzione WSALookupServiceEnd</strong></a> durante l'elaborazione della chiamata. La chiamata è stata annullata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEREFUSED"></span><span id="wsaerefused"></span><dl> <dt><strong>WSAEREFUSED</strong></dt> <dt>10112</dt> </dl></td>
<td><dl> <dt><span id="Database_query_was_refused."></span><span id="database_query_was_refused."></span><span id="DATABASE_QUERY_WAS_REFUSED."></span>La query di database è stata rifiutata.</dt> <dd> Una query di database non è riuscita perché è stata rifiutata attivamente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span><dl> <dt><strong>WSAHOST_NOT_FOUND</strong></dt> <dt>11001</dt> </dl></td>
<td><dl> <dt><span id="Host_not_found."></span><span id="host_not_found."></span><span id="HOST_NOT_FOUND."></span>Host non trovato.</dt> <dd> L'host è sconosciuto. Il nome non è un nome host o un alias ufficiale oppure non è stato trovato nei database su cui viene eseguita la query. Questo errore può essere restituito anche per le query di protocollo e servizio e significa che il nome specificato non è stato trovato nel database pertinente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span><dl> <dt><strong>WSATRY_AGAIN</strong></dt> <dt>11002</dt> </dl></td>
<td><dl> <dt><span id="Nonauthoritative_host_not_found."></span><span id="nonauthoritative_host_not_found."></span><span id="NONAUTHORITATIVE_HOST_NOT_FOUND."></span>Host non autorevole non trovato.</dt> <dd> Si tratta in genere di un errore temporaneo durante la risoluzione del nome host e indica che il server locale non ha ricevuto una risposta da un server autorevole. La risposta potrebbe essere ricevuta ripetendo l'operazione in un altro momento.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span><dl> <dt><strong>WSANO_RECOVERY</strong></dt> <dt>11003</dt> </dl></td>
<td><dl> <dt><span id="This_is_a_nonrecoverable_error."></span><span id="this_is_a_nonrecoverable_error."></span><span id="THIS_IS_A_NONRECOVERABLE_ERROR."></span>Si tratta di un errore non irreversibile.</dt> <dd> Ciò indica che si è verificato un tipo di errore non irreversibile durante una ricerca nel database. Ciò può essere dovuto al fatto che i file di database (ad esempio, i file HOSTS, SERVICES o PROTOCOLS compatibili con BSD) non sono stati trovati o che il server ha restituito una richiesta DNS con un errore grave.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANO_DATA"></span><span id="wsano_data"></span><dl> <dt><strong>WSANO_DATA</strong></dt> <dt>11004</dt> </dl></td>
<td><dl> <dt><span id="Valid_name__no_data_record_of_requested_type."></span><span id="valid_name__no_data_record_of_requested_type."></span><span id="VALID_NAME__NO_DATA_RECORD_OF_REQUESTED_TYPE."></span>Nome valido, nessun record di dati di tipo richiesto.</dt> <dd> Il nome richiesto è valido ed è stato trovato nel database, ma non dispone dei dati associati corretti per cui è in corso la risoluzione. L'esempio consueto è un tentativo di conversione da nome host a indirizzo (usando <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname"><strong>gethostbyname</strong></a> o <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname"><strong>WSAAsyncGetHostByName</strong></a>) che usa IL DNS (Domain Name Server). Viene restituito un record MX, ma non un record A, che indica che l'host stesso esiste, ma non è direttamente raggiungibile.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span><dl> <dt><strong>WSA_QOS_RECEIVERS</strong></dt> <dt>11005</dt> </dl></td>
<td><dl> <dt><span id="QoS_receivers."></span><span id="qos_receivers."></span><span id="QOS_RECEIVERS."></span>Ricevitori QoS.</dt> <dd> È arrivata almeno una riserva QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span><dl> <dt><strong>WSA_QOS_SENDERS</strong></dt> <dt>11006</dt> </dl></td>
<td><dl> <dt><span id="QoS_senders."></span><span id="qos_senders."></span><span id="QOS_SENDERS."></span>Mittenti QoS.</dt> <dd> È stato raggiunto almeno un percorso di invio QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span><dl> <dt><strong>WSA_QOS_NO_SENDERS</strong></dt> <dt>11007</dt> </dl></td>
<td><dl> <dt><span id="No_QoS_senders."></span><span id="no_qos_senders."></span><span id="NO_QOS_SENDERS."></span>Nessun mittente QoS.</dt> <dd> Non sono presenti mittenti QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span><dl> <dt><strong>WSA_QOS_NO_RECEIVERS</strong></dt> <dt>11008</dt> </dl></td>
<td><dl> <dt><span id="QoS_no_receivers."></span><span id="qos_no_receivers."></span><span id="QOS_NO_RECEIVERS."></span>QoS senza ricevitori.</dt> <dd> Non sono presenti ricevitori QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span><dl> <dt><strong>WSA_QOS_REQUEST_CONFIRMED</strong></dt> <dt>11009</dt> </dl></td>
<td><dl> <dt><span id="QoS_request_confirmed."></span><span id="qos_request_confirmed."></span><span id="QOS_REQUEST_CONFIRMED."></span>Richiesta QoS confermata.</dt> <dd> La richiesta di prenotazione QoS è stata confermata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span><dl> <dt><strong>WSA_QOS_ADMISSION_FAILURE</strong></dt> <dt>11010</dt> </dl></td>
<td><dl> <dt><span id="QoS_admission_error."></span><span id="qos_admission_error."></span><span id="QOS_ADMISSION_ERROR."></span>Errore di ammissione QoS.</dt> <dd> Si è verificato un errore QoS a causa della mancanza di risorse.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span><dl> <dt><strong>WSA_QOS_POLICY_FAILURE</strong></dt> <dt>11011</dt> </dl></td>
<td><dl> <dt><span id="QoS_policy_failure."></span><span id="qos_policy_failure."></span><span id="QOS_POLICY_FAILURE."></span>Errore dei criteri QoS.</dt> <dd> La richiesta QoS è stata rifiutata perché il sistema dei criteri non è riuscito ad allocare la risorsa richiesta all'interno dei criteri esistenti. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span><dl> <dt><strong>WSA_QOS_BAD_STYLE</strong></dt> <dt>11012</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_style."></span><span id="qos_bad_style."></span><span id="QOS_BAD_STYLE."></span>Stile QoS non applicato.</dt> <dd> È stato rilevato uno stile QoS sconosciuto o in conflitto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span><dl> <dt><strong>WSA_QOS_BAD_OBJECT</strong></dt> <dt>11013</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_object."></span><span id="qos_bad_object."></span><span id="QOS_BAD_OBJECT."></span>Oggetto QoS non valido.</dt> <dd> Si è verificato un problema con una parte di filterspec o il buffer specifico del provider in generale.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span><dl> <dt><strong>WSA_QOS_TRAFFIC_CTRL_ERROR</strong></dt> <dt>11014</dt> </dl></td>
<td><dl> <dt><span id="QoS_traffic_control_error."></span><span id="qos_traffic_control_error."></span><span id="QOS_TRAFFIC_CONTROL_ERROR."></span>Errore di controllo del traffico QoS.</dt> <dd> Un errore con l'API di controllo del traffico sottostante come richiesta QoS generica è stato convertito per l'imposizione locale dall'API TC. Ciò potrebbe essere dovuto a un errore di memoria insufficiente o a un errore interno del provider QoS. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span><dl> <dt><strong>WSA_QOS_GENERIC_ERROR</strong></dt> <dt>11015</dt> </dl></td>
<td><dl> <dt><span id="QoS_generic_error."></span><span id="qos_generic_error."></span><span id="QOS_GENERIC_ERROR."></span>Errore generico QoS.</dt> <dd> Errore QoS generale.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span><dl> <dt><strong>WSA_QOS_ESERVICETYPE</strong></dt> <dt>11016</dt> </dl></td>
<td><dl> <dt><span id="QoS_service_type_error."></span><span id="qos_service_type_error."></span><span id="QOS_SERVICE_TYPE_ERROR."></span>Errore del tipo di servizio QoS.</dt> <dd> È stato trovato un tipo di servizio non valido o non riconosciuto in flowspec QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span><dl> <dt><strong>WSA_QOS_EFLOWSPEC</strong></dt> <dt>11017</dt> </dl></td>
<td><dl> <dt><span id="QoS_flowspec_error."></span><span id="qos_flowspec_error."></span><span id="QOS_FLOWSPEC_ERROR."></span>Errore flowspec QoS.</dt> <dd> È stato trovato un oggetto flowspec non valido o incoerente nella <a href="/windows/win32/api/winsock2/ns-winsock2-qos"><strong>struttura QOS.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span><dl> <dt><strong>WSA_QOS_EPROVSPECBUF</strong></dt> <dt>11018</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider_buffer."></span><span id="invalid_qos_provider_buffer."></span><span id="INVALID_QOS_PROVIDER_BUFFER."></span>Buffer del provider QoS non valido.</dt> <dd> Buffer specifico del provider QoS non valido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span><dl> <dt><strong>WSA_QOS_EFILTERSTYLE</strong></dt> <dt>11019</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_style."></span><span id="invalid_qos_filter_style."></span><span id="INVALID_QOS_FILTER_STYLE."></span>Stile di filtro QoS non valido.</dt> <dd> È stato usato uno stile di filtro QoS non valido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span><dl> <dt><strong>WSA_QOS_EFILTERTYPE</strong></dt> <dt>11020</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_type."></span><span id="invalid_qos_filter_type."></span><span id="INVALID_QOS_FILTER_TYPE."></span>Tipo di filtro QoS non valido.</dt> <dd> È stato usato un tipo di filtro QoS non valido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span><dl> <dt><strong>WSA_QOS_EFILTERCOUNT</strong></dt> <dt>11021</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_filter_count."></span><span id="incorrect_qos_filter_count."></span><span id="INCORRECT_QOS_FILTER_COUNT."></span>Conteggio del filtro QoS non corretto.</dt> <dd> È stato specificato un numero errato di FILTRI QoSPEC in FLOWDESCRIPTOR.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span><dl> <dt><strong>WSA_QOS_EOBJLENGTH</strong></dt> <dt>11022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_object_length."></span><span id="invalid_qos_object_length."></span><span id="INVALID_QOS_OBJECT_LENGTH."></span>Lunghezza dell'oggetto QoS non valida.</dt> <dd> Nel buffer specifico del provider QoS è stato specificato un oggetto con un campo ObjectLength non valido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span><dl> <dt><strong>WSA_QOS_EFLOWCOUNT</strong></dt> <dt>11023</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_flow_count."></span><span id="incorrect_qos_flow_count."></span><span id="INCORRECT_QOS_FLOW_COUNT."></span>Numero di flussi QoS non corretto.</dt> <dd> Nella struttura QoS è stato specificato un numero errato di descrittori di flusso.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span><dl> <dt><strong>WSA_QOS_EUNKOWNPSOBJ</strong></dt> <dt>11024</dt> </dl></td>
<td><dl> <dt><span id="Unrecognized_QoS_object."></span><span id="unrecognized_qos_object."></span><span id="UNRECOGNIZED_QOS_OBJECT."></span>Oggetto QoS non riconosciuto.</dt> <dd> È stato trovato un oggetto non riconosciuto nel buffer specifico del provider QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span><dl> <dt><strong>WSA_QOS_EPOLICYOBJ</strong></dt> <dt>11025</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_policy_object."></span><span id="invalid_qos_policy_object."></span><span id="INVALID_QOS_POLICY_OBJECT."></span>Oggetto criterio QoS non valido.</dt> <dd> È stato trovato un oggetto criteri non valido nel buffer specifico del provider QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span><dl> <dt><strong>WSA_QOS_EFLOWDESC</strong></dt> <dt>11026</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_flow_descriptor."></span><span id="invalid_qos_flow_descriptor."></span><span id="INVALID_QOS_FLOW_DESCRIPTOR."></span>Descrittore di flusso QoS non valido.</dt> <dd> È stato trovato un descrittore di flusso QoS non valido nell'elenco dei descrittori di flusso.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span><dl> <dt><strong>WSA_QOS_EPSFLOWSPEC</strong></dt> <dt>11027</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_flowspec."></span><span id="invalid_qos_provider-specific_flowspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FLOWSPEC."></span>Flowspec specifico del provider QoS non valido.</dt> <dd> È stato rilevato un flowspec non valido o incoerente nel buffer specifico del provider QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span><dl> <dt><strong>WSA_QOS_EPSFILTERSPEC</strong></dt> <dt>11028</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_filterspec."></span><span id="invalid_qos_provider-specific_filterspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FILTERSPEC."></span>Filterspec specifico del provider QoS non valido.</dt> <dd> È stato trovato un FILTERSPEC non valido nel buffer specifico del provider QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span><dl> <dt><strong>WSA_QOS_ESDMODEOBJ</strong></dt> <dt>11029</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shape_discard_mode_object."></span><span id="invalid_qos_shape_discard_mode_object."></span><span id="INVALID_QOS_SHAPE_DISCARD_MODE_OBJECT."></span>Oggetto modalità di eliminazione della forma QoS non valido.</dt> <dd> Nel buffer specifico del provider QoS è stato trovato un oggetto in modalità di eliminazione forma non valido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span><dl> <dt><strong>WSA_QOS_ESHAPERATEOBJ</strong></dt> <dt>11030</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shaping_rate_object."></span><span id="invalid_qos_shaping_rate_object."></span><span id="INVALID_QOS_SHAPING_RATE_OBJECT."></span>Oggetto frequenza di shaping QoS non valido.</dt> <dd> È stato trovato un oggetto della frequenza di shaping non valido nel buffer specifico del provider QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span><dl> <dt><strong>WSA_QOS_RESERVED_PETYPE</strong></dt> <dt>11031</dt> </dl></td>
<td><dl> <dt><span id="Reserved_policy_QoS_element_type."></span><span id="reserved_policy_qos_element_type."></span><span id="RESERVED_POLICY_QOS_ELEMENT_TYPE."></span>Tipo di elemento QoS dei criteri riservati.</dt> <dd> È stato trovato un elemento criteri riservati nel buffer specifico del provider QoS.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winsock2.h; </dt> <dt>Winerror.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore : errno, h \_ errno e WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Gestione degli errori di Winsock](handling-winsock-errors.md)
</dt> <dt>

[**Messaggio di formato**](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
