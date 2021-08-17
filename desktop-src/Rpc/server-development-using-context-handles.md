---
title: Sviluppo di server tramite handle di contesto
description: Dal punto di vista dello sviluppo di programmi server, un handle di contesto è un puntatore non tipiato. I programmi server inizializzano gli handle di contesto puntandoli ai dati in memoria o in un'altra forma di archiviazione, ad esempio file su dischi.
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db05441f7314fba628d1ec07db5f99266c595c84e672ada976b38f7576ab5d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925337"
---
# <a name="server-development-using-context-handles"></a>Sviluppo di server tramite handle di contesto

Dal punto di vista dello sviluppo di programmi server, un handle di contesto è un puntatore non tipiato. I programmi server inizializzano gli handle di contesto puntandoli ai dati in memoria o in un'altra forma di archiviazione, ad esempio file su dischi.

Si supponga, ad esempio, che un client usi un handle di contesto per richiedere una serie di aggiornamenti a un record in un database. Il client chiama una procedura remota sul server e le passa una chiave di ricerca. Il programma server cerca nel database la chiave di ricerca e ottiene il numero intero del record corrispondente. Il server può quindi puntare un puntatore a void in una posizione di memoria contenente il numero di record. Quando viene restituita, la procedura remota deve restituire il puntatore come handle di contesto tramite il relativo valore restituito o il relativo elenco di parametri. Il client deve passare il puntatore al server ogni volta che chiama procedure remote per aggiornare il record. Durante ognuna di queste operazioni di aggiornamento, il server esegue il cast del puntatore void come puntatore a un integer.

Quando il programma server punta l'handle di contesto ai dati di contesto, l'handle viene considerato aperto. Gli handle contenenti **un valore NULL** vengono chiusi. Il server mantiene un handle di contesto aperto fino a quando il client non chiama una procedura remota che lo chiude. Se la sessione client termina mentre l'handle è aperto, il run-time RPC chiama la routine di run-down del server per liberare l'handle.

Nel frammento di codice seguente viene illustrato come un server potrebbe implementare un handle di contesto. In questo esempio il server gestisce un file di dati in cui il client scrive utilizzando procedure remote. Le informazioni di contesto sono un handle di file che tiene traccia della posizione corrente nel file in cui il server scriverà i dati. L'handle di file viene in pacchetto come handle di contesto nell'elenco di parametri per le chiamate di procedura remota. Una struttura contiene il nome del file e l'handle di file. La definizione dell'interfaccia per questo esempio è illustrata in [Sviluppo di interfacce tramite handle di contesto.](interface-development-using-context-handles.md)


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



La funzione RemoteClose chiude un file nel server. Si noti che l'applicazione server deve **assegnare NULL** all'handle di contesto come parte della funzione close. In questo modo, lo stub del server e la libreria di runtime RPC comunicano che l'handle di contesto è stato eliminato. In caso contrario, la connessione verrà mantenuta aperta e alla fine si verificherà un run-down del contesto.


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
> Sebbene sia previsto che il client passi un handle di contesto valido a una chiamata con attributi direzionali in, out, RPC non rifiuta gli handle di contesto NULL per questa combinazione di \[ \] attributi direzionali.  **L'handle** di contesto NULL viene passato al server come **puntatore NULL.** Il codice server per le chiamate contenenti un handle di contesto in ingresso e in uscita deve essere scritto per evitare una violazione di accesso quando \[ \] viene ricevuto un **puntatore** NULL.

 

 

 




