---
title: Sviluppo di server con handle di contesto
description: Dal punto di vista dello sviluppo di un programma server, un handle di contesto è un puntatore non tipizzato. I programmi server inizializzano gli handle di contesto puntando i dati in memoria o in un'altra forma di archiviazione (ad esempio file su dischi).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f743a4a6aa4a2aa7b6987bb54dc56e55cffbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045158"
---
# <a name="server-development-using-context-handles"></a>Sviluppo di server con handle di contesto

Dal punto di vista dello sviluppo di un programma server, un handle di contesto è un puntatore non tipizzato. I programmi server inizializzano gli handle di contesto puntando i dati in memoria o in un'altra forma di archiviazione (ad esempio file su dischi).

Si supponga, ad esempio, che un client utilizzi un handle di contesto per richiedere una serie di aggiornamenti a un record in un database. Il client chiama una procedura remota sul server e la passa a una chiave di ricerca. Il programma server cerca la chiave di ricerca nel database e ottiene il numero di record integer del record corrispondente. Il server può quindi puntare un puntatore a void in una posizione di memoria contenente il numero di record. Quando viene restituito, la procedura remota deve restituire il puntatore come handle di contesto tramite il relativo valore restituito o l'elenco di parametri. Il client deve passare il puntatore al server ogni volta che ha chiamato le procedure remote per aggiornare il record. Durante ogni operazione di aggiornamento, il server eseguirà il cast del puntatore void come puntatore a un Integer.

Dopo che il programma server ha puntato all'handle di contesto nei dati di contesto, l'handle viene considerato aperto. Gli handle contenenti un valore **null** sono chiusi. Il server gestisce un handle di contesto aperto finché il client non chiama una procedura remota che la chiude. Se la sessione client termina quando l'handle è aperto, il tempo di esecuzione RPC chiama la routine di esecuzione del server per liberare l'handle.

Nel frammento di codice seguente viene illustrato come un server può implementare un handle di contesto. In questo esempio, il server gestisce un file di dati che il client scrive in utilizzando le procedure remote. Le informazioni sul contesto sono un handle di file che tiene traccia della posizione corrente nel file in cui i dati vengono scritti dal server. L'handle di file è incluso nel pacchetto come handle di contesto nell'elenco di parametri per le chiamate di procedure remote. Una struttura contiene il nome file e l'handle di file. La definizione dell'interfaccia per questo esempio viene illustrata nello [sviluppo di interfacce con handle di contesto](interface-development-using-context-handles.md).


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



La funzione RemoteOpen apre un file nel server:


```C++
short RemoteOpen(
    PPCONTEXT_HANDLE_TYPE pphContext,
    unsigned char *pszFileName)
{
    FILE               *hFile;
    FILE_CONTEXT_TYPE  *pFileContext;
 
    if ((hFile = fopen(pszFileName, "r")) == NULL) 
    {
        *pphContext = (PCONTEXT_HANDLE_TYPE) NULL;
        return(-1);
    }
    else 
    {
        pFileContext = (FILE_CONTEXT_TYPE *) 
                       MIDL_user_allocate(sizeof(FILE_CONTEXT_TYPE));
        pFileContext->hFile = hFile;
        // check if pszFileName is longer than 256 and if yes, return
        // an error
        strcpy_s(pFileContext->achFile, srlen(pszFileName), pszFileName);
        *pphContext = (PCONTEXT_HANDLE_TYPE) pFileContext;
        return(0);
    }
}
```



La funzione RemoteRead legge un file nel server.


```C++
short RemoteRead(
    PCONTEXT_HANDLE_TYPE phContext, 
    unsigned char *pbBuf, 
    short *pcbBuf) 
{ 
    FILE_CONTEXT_TYPE *pFileContext; 
    printf("in RemoteRead\n"); 
    pFileContext = (FILE_CONTEXT_TYPE *) phContext; 
    *pcbBuf = (short) fread(pbBuf, sizeof(char), 
                            BUFSIZE, 
                            pFileContext->hFile); 
    return(*pcbBuf); 
}
```



La funzione RemoteClose chiude un file nel server. Si noti che l'applicazione server deve assegnare **null** all'handle di contesto come parte della funzione close. In questo modo si comunica allo stub del server e alla libreria di runtime RPC che l'handle di contesto è stato eliminato. In caso contrario, la connessione verrà mantenuta aperta e infine si verificherà un errore di esecuzione del contesto.


```C++
void RemoteClose(PPCONTEXT_HANDLE_TYPE pphContext)
{
    FILE_CONTEXT_TYPE *pFileContext;
 
    if (*pphContext == NULL)
    {
        //Log error, client tried to close a NULL handle.
        return;
    }
    pFileContext = (FILE_CONTEXT_TYPE *)*pphContext;
    printf("File %s closed.\n", pFileContext->achFile);
    fclose(pFileConext->hFile);
    MIDL_user_free(pFileContext);
 
    // This tells the run-time, when it is marshalling the out 
    // parameters, that the context handle has been closed normally.
    *pphContext = NULL;
}
```



> [!Note]  
> Sebbene sia previsto che il client passi un handle di contesto valido a una chiamata con \[ in, \] attributi direzionali out, RPC non rifiuta gli handle di contesto **null** per questa combinazione di attributi direzionali. L'handle del contesto **null** viene passato al server come puntatore **null** . È necessario scrivere il codice server per le chiamate contenenti un \[ \] handle del contesto out per evitare una violazione di accesso quando viene ricevuto un puntatore **null** .

 

 

 




