---
title: Ricerca di sistemi host server
description: Ricerca di sistemi host server utilizzando binding di stringa ed eseguendo una query su un database del servizio nome per il percorso di un programma server.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856298"
---
# <a name="finding-server-host-systems"></a>Ricerca di sistemi host server

Un sistema host server è il computer che esegue il programma server dell'applicazione distribuita. In una rete potrebbero essere presenti uno o più sistemi host server. Il modo in cui il programma client trova un server a cui connettersi dipende dalle esigenze del programma.

Esistono due metodi per trovare i sistemi host server:

-   Uso delle informazioni archiviate nelle stringhe nel codice sorgente del client, nelle variabili di ambiente o nei file di configurazione specifici dell'applicazione. L'applicazione client può usare i dati nella stringa per comporre un'associazione tra il client e il server.
-   Esecuzione di query su un database del servizio nome per il percorso di un programma server.

In questa sezione vengono presentate informazioni su entrambe le tecniche negli argomenti seguenti:

-   [Uso di associazioni di stringa](#using-string-bindings)
-   [Importazione dai database del servizio dei nomi](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>Uso di associazioni di stringa

Le applicazioni possono creare binding da informazioni archiviate in stringhe. L'applicazione client compone queste informazioni sotto forma di stringa, quindi chiama la funzione [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) . Il client deve fornire le informazioni seguenti per identificare il server:

-   Nome dell'interfaccia, identificatore univoco globale (GUID) dell'oggetto o UUID dell'oggetto. Per altre informazioni, vedere [generazione di UUID di interfaccia](generating-interface-uuids.md) e [UUID di stringa](string-uuid.md).
-   Tipo di trasporto su cui comunicare, ad esempio named pipe o TCP/IP. Per informazioni dettagliate, vedere [terminologia di associazione RPC essenziale](essential-rpc-binding-terminology.md) e [selezione di una sequenza di protocolli](selecting-a-protocol-sequence.md).
-   Indirizzo di rete o nome del computer host del server.
-   Endpoint del programma server nel computer host del server. Per altre informazioni, vedere [ricerca di endpoint](finding-endpoints.md)e [specifica di endpoint](specifying-endpoints.md).

(L'UUID dell'oggetto e le informazioni sull'endpoint sono facoltativi).

Negli esempi seguenti, il parametro *pszNetworkAddress* e altri parametri includono barre rovesciate incorporate. La barra rovesciata è un carattere di escape nel linguaggio di programmazione C. Sono necessarie due barre rovesciate per rappresentare ogni carattere barra rovesciata singolo valore letterale. La struttura di associazione di stringhe deve contenere quattro caratteri di barra rovesciata per rappresentare i due caratteri letterali che precedono il nome del server.

Nell'esempio seguente viene illustrato che il nome del server deve essere preceduto da otto barre rovesciate, in modo che nella struttura dei dati di associazione di stringa vengano visualizzati quattro caratteri di barra rovesciata letterali dopo che la funzione **sprintf \_ s** elabora la stringa.


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



Nell'esempio seguente, l'associazione di stringa viene visualizzata come:

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP: \\ \\ \\ \\ *ServerName* \[ \\ \\ pipe \\ \\ *pipeName*\]

Il client chiama quindi [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per ottenere l'handle di associazione:


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



Una funzione comoda, [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembla l'UUID dell'oggetto, la sequenza di protocollo, l'indirizzo di rete e l'endpoint nella sintassi corretta per la chiamata a [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding). Non è necessario preoccuparsi di inserire la e commerciale, i due punti e i vari componenti per ogni sequenza di protocollo nel posto giusto; è sufficiente specificare le stringhe come parametri della funzione. La libreria di runtime alloca anche la memoria necessaria per l'associazione di stringa.


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



Un'altra funzione di praticità, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), accetta un handle di associazione come input e produce l'associazione di stringa corrispondente.

## <a name="importing-from-name-service-databases"></a>Importazione dai database del servizio dei nomi

Nome archivio dei database del servizio, tra le altre cose, handle di binding e UUID. L'applicazione client può cercare uno dei due o entrambi quando è necessario eseguire l'associazione al server. Per una descrizione delle informazioni archiviate da un nome e del formato di archiviazione, vedere [il database del servizio nome RPC](the-rpc-name-service-database.md).

La libreria RPC fornisce due set di funzioni che il programma client può usare per cercare il nome del database del servizio. I nomi di un set iniziano con RpcNsBindingImport. I nomi dell'altro set iniziano con RpcNsBindingLookup. La differenza tra i due gruppi di funzioni è che le funzioni RpcNsBindingImport restituiscono un singolo handle di binding per chiamata e le funzioni RpcNsBindingLookup restituiscono gruppi di handle per ogni chiamata.

Per iniziare una ricerca con le funzioni RpcNsBindingImport, chiamare prima [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), come illustrato nel frammento di codice seguente.


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



Quando le funzioni RPC eseguono ricerche nel database del servizio dei nomi, è necessario disporre di una posizione per iniziare la ricerca. Nella terminologia RPC, questo viene chiamato nome della voce. Il programma client passa il nome della voce come secondo parametro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Questo parametro può essere **null** se si desidera eseguire la ricerca nell'intero database del servizio. In alternativa, è possibile cercare la voce del server passando un nome di voce del server o cercare la voce di gruppo passando un nome di voce di gruppo. Il passaggio di un nome di voce limita la ricerca al contenuto di tale voce.

Nell'esempio precedente, il valore predefinito della \_ sintassi RPC C \_ NS \_ \_ viene passato come primo parametro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Viene selezionata la sintassi predefinita per il nome della voce. Attualmente, questa è l'unica sintassi supportata per i nomi di voce.

L'applicazione client può cercare nel database del servizio dei nomi un nome di interfaccia, un UUID o entrambi. Se si vuole che venga cercata un'interfaccia in base al nome, passare la variabile di interfaccia globale generata dal compilatore MIDL dal file IDL come terzo parametro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). La relativa dichiarazione sarà presente nel file di intestazione generato dal compilatore MIDL quando ha generato lo stub del client. Se si vuole che il programma client cerchi solo per UUID, impostare il terzo parametro su **null**.

Quando si esegue la ricerca di un UUID nel database del servizio dei nomi, impostare il quarto parametro di [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) sull'UUID che si desidera cercare. Se non si sta cercando un UUID, impostare questo parametro su **null**.

La funzione [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) passa l'indirizzo di un servizio nome-handle del contesto di ricerca tramite il quinto parametro. Passare questo parametro ad altre funzioni di RpcNsBindingImport.

In particolare, la funzione successiva chiamata dall'applicazione client è [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext). I programmi client utilizzano questa funzione per recuperare gli handle di binding compatibili dal database del servizio dei nomi. Il frammento di codice seguente illustra come può essere chiamata questa funzione:


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



Una volta chiamata la funzione [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) per ottenere un handle di binding, l'applicazione client può determinare se l'handle ricevuto è accettabile. In caso contrario, il programma client può eseguire un ciclo e chiamare di nuovo **RpcNsBindingImportNext** per verificare se il servizio nome contiene un handle più appropriato. Per ogni chiamata a **RpcNsBindingImportNext**, è necessario che sia presente una chiamata corrispondente a RpcNsBindingFree. Al termine della ricerca, chiamare la funzione [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) per liberare il contesto di ricerca.

Quando l'applicazione client dispone di un handle di binding accettabile, deve verificare che l'applicazione server sia in esecuzione. Il client può usare due metodi per eseguire questa verifica. Il primo consiste nel chiamare una funzione nell'interfaccia client. Se il programma del server è in esecuzione, la chiamata verrà completata. In caso contrario, la chiamata avrà esito negativo. Un modo migliore per verificare che il server sia in esecuzione consiste nel richiamare [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), seguito da una chiamata a [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening). Per ulteriori informazioni sul database del servizio nomi, vedere [il database del servizio nome RPC](the-rpc-name-service-database.md).

 

 




