---
title: Ricerca di sistemi host server
description: Ricerca di sistemi host del server tramite associazioni di stringhe ed esecuzione di query su un database del servizio nomi per individuare il percorso di un programma server.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180e2e43c0350f55defb74762d6ab1b6b656dafbc1468bcc7f077ed9780a2e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929990"
---
# <a name="finding-server-host-systems"></a>Ricerca di sistemi host server

Un sistema host server è il computer che esegue il programma server dell'applicazione distribuita. In una rete possono essere presenti uno o più sistemi host server. Il modo in cui il programma client trova un server a cui connettersi dipende dalle esigenze del programma.

Esistono due metodi per trovare i sistemi host del server:

-   Uso delle informazioni archiviate nelle stringhe nel codice sorgente del client, nelle variabili di ambiente o nei file di configurazione specifici dell'applicazione. L'applicazione client può usare i dati nella stringa per comporre un'associazione tra il client e il server.
-   Esecuzione di query su un database del servizio nomi per il percorso di un programma server.

Questa sezione presenta informazioni su entrambe queste tecniche negli argomenti seguenti:

-   [Uso di associazioni di stringhe](#using-string-bindings)
-   [Importazione da database del servizio nomi](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>Uso di associazioni di stringhe

Le applicazioni possono creare associazioni dalle informazioni archiviate nelle stringhe. L'applicazione client compone queste informazioni come stringa, quindi chiama la [**funzione RpcBindingFromStringBinding.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) Il client deve fornire le informazioni seguenti per identificare il server:

-   Nome dell'interfaccia, identificatore univoco globale (GUID) dell'oggetto o UUID dell'oggetto. Per altre informazioni, vedere [Generazione di UUID dell'interfaccia](generating-interface-uuids.md) e [UUID stringa.](string-uuid.md)
-   Tipo di trasporto su cui comunicare, ad esempio named pipe o TCP/IP. Per informazioni dettagliate, vedere [Terminologia di binding RPC essenziale e](essential-rpc-binding-terminology.md) Selezione di una sequenza di [protocollo.](selecting-a-protocol-sequence.md)
-   Indirizzo di rete o nome del computer host del server.
-   Endpoint del programma server nel computer host del server. Per altre informazioni, vedere [Ricerca di endpoint](finding-endpoints.md)e Specifica di [endpoint](specifying-endpoints.md).

L'UUID dell'oggetto e le informazioni sull'endpoint sono facoltativi.

Negli esempi seguenti il parametro *pszNetworkAddress* e altri parametri includono barre rovesciate incorporate. La barra rovesciata è un carattere di escape nel linguaggio di programmazione C. Sono necessarie due barre rovesciate per rappresentare ogni singolo carattere barra rovesciata letterale. La struttura di associazione di stringhe deve contenere quattro caratteri barra rovesciata per rappresentare i due caratteri barra rovesciata letterale che precedono il nome del server.

L'esempio seguente mostra che il nome del server deve essere preceduto da otto barre rovesciate in modo che quattro caratteri letterali barra rovesciata vengano visualizzati nella struttura dei dati di associazione di stringhe dopo che la funzione **sprintf \_** ha elaborata la stringa.


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



Nell'esempio seguente l'associazione di stringhe viene visualizzata come:

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np: \\ \\ \\ \\ *nomeserver* \[ \\ \\ \\ \\ *pipename*\]

Il client chiama quindi [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per ottenere l'handle di associazione:


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



Una funzione di praticità, [**RpcStringBindingCompose,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembla l'oggetto UUID, la sequenza del protocollo, l'indirizzo di rete e l'endpoint nella sintassi corretta per la chiamata a [**RpcBindingFromStringBinding.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) Non è necessario preoccuparsi di inserire la e commerciale, i due punti e i vari componenti per ogni sequenza di protocollo nel posto giusto; è sufficiente specificare le stringhe come parametri per la funzione. La libreria di runtime alloca anche la memoria necessaria per l'associazione di stringhe.


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

## <a name="importing-from-name-service-databases"></a>Importazione da database del servizio nomi

I database del servizio dei nomi archiviano, tra le altre cose, gli handle di associazione e gli UUID. L'applicazione client può cercare uno o entrambi questi elementi quando è necessario eseguire l'associazione al server. Per una descrizione delle informazioni archiviate da un servizio nomi e del formato di archiviazione, vedere Database del servizio nomi [RPC](the-rpc-name-service-database.md).

La libreria RPC fornisce due set di funzioni che il programma client può usare per cercare il database del servizio dei nomi. I nomi di un set iniziano con RpcNsBindingImport. I nomi dell'altro set iniziano con RpcNsBindingLookup. La differenza tra i due gruppi di funzioni è che le funzioni RpcNsBindingImport restituiscono un singolo handle di associazione per ogni chiamata e le funzioni RpcNsBindingLookup restituiscono gruppi di handle per ogni chiamata.

Per iniziare una ricerca con le funzioni RpcNsBindingImport, chiamare [**prima RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), come illustrato nel frammento di codice seguente.


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



Quando le funzioni RPC esereranno una ricerca nel database del servizio dei nomi, è necessario un punto in cui iniziare la ricerca. Nella terminologia RPC si tratta del nome della voce. Il programma client passa il nome della voce come secondo parametro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Questo parametro può essere **NULL** se si vuole cercare l'intero database del servizio dei nomi. In alternativa, è possibile cercare la voce del server passando un nome di voce del server o la voce del gruppo passando un nome di voce di gruppo. Il passaggio di un nome di voce limita la ricerca al contenuto di tale voce.

Nell'esempio precedente il valore RPC C NS SYNTAX DEFAULT viene passato come primo parametro \_ \_ a \_ \_ [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). In questo modo viene selezionata la sintassi del nome di voce predefinita. Attualmente, questa è l'unica sintassi di entry-name supportata.

L'applicazione client può cercare nel database del servizio dei nomi un nome di interfaccia, un UUID o entrambi. Per cercare un'interfaccia in base al nome, passare la variabile di interfaccia globale generata dal compilatore MIDL dal file IDL come terzo parametro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). La dichiarazione è presente nel file di intestazione generato dal compilatore MIDL quando ha generato lo stub client. Se si vuole che il programma client eseere la ricerca solo in base all'UUID, impostare il terzo parametro su **NULL.**

Quando si cerca un UUID nel database del servizio dei nomi, impostare il quarto parametro di [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) sull'UUID da cercare. Se non si sta cercando un UUID, impostare questo parametro su **NULL.**

La [**funzione RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) passa l'indirizzo di un handle del contesto di ricerca del servizio dei nomi tramite il quinto parametro. Questo parametro viene passato ad altre funzioni RpcNsBindingImport.

In particolare, la funzione successiva chiamata dall'applicazione client è [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext). I programmi client usano questa funzione per recuperare gli handle di associazione compatibili dal database del servizio dei nomi. Il frammento di codice seguente illustra come chiamare questa funzione:


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



Dopo aver chiamato la [**funzione RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) per ottenere un handle di associazione, l'applicazione client può determinare se l'handle ricevuto è accettabile. In caso contrario, il programma client può eseguire un ciclo e chiamare di nuovo **RpcNsBindingImportNext** per verificare se il servizio dei nomi contiene un handle più appropriato. Per ogni chiamata a **RpcNsBindingImportNext,** deve essere presente una chiamata corrispondente a RpcNsBindingFree. Al termine della ricerca, chiamare la [**funzione RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) per liberare il contesto di ricerca.

Dopo che l'applicazione client ha un handle di associazione accettabile, deve verificare che l'applicazione server sia in esecuzione. Per eseguire questa verifica, il client può usare due metodi. Il primo è chiamare una funzione nell'interfaccia client. Se il programma server è in esecuzione, la chiamata verrà completata. In caso contrario, la chiamata avrà esito negativo. Un modo migliore per verificare che il server sia in esecuzione è richiamare [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), seguito da una chiamata a [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening). Per altre informazioni sul database del servizio dei nomi, vedere [Database del servizio](the-rpc-name-service-database.md)nomi RPC .

 

 




