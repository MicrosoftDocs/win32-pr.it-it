---
title: Gestione dati
description: In questo argomento viene illustrato come gli oggetti memoria passano i dati da un'applicazione a un'altra.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), gestione dati
- DDE (Dynamic Data Exchange), gestione dati
- scambio di dati, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Libreria di gestione Dynamic Data Exchange (DDEML), gestione dati
- DDEML (libreria di gestione Dynamic Data Exchange), gestione dati
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
- Dynamic Data Exchange (DDE), oggetti
- DDE (Dynamic Data Exchange), oggetti
- Libreria di gestione Dynamic Data Exchange (DDEML), oggetti
- DDEML (libreria di gestione Dynamic Data Exchange), oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc5178f636cf4b75111d4fc48e17fd144400a91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396903"
---
# <a name="data-management"></a>Gestione dati

Poiché Dynamic Data Exchange (DDE) utilizza oggetti memoria per passare dati da un'applicazione a un'altra, la libreria di gestione Dynamic Data Exchange (DDEML) fornisce un set di funzioni che le applicazioni DDE possono utilizzare per creare e gestire oggetti DDE.

Per tutte le transazioni che comportano lo scambio di dati, è necessario che l'applicazione fornisca i dati per creare un buffer locale contenente i dati e quindi chiamare la funzione [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) . Questa funzione alloca un oggetto DDE, copia i dati dal buffer nell'oggetto e restituisce un handle di dati. Un handle di dati è un valore **DWORD** utilizzato dal DDEML per fornire l'accesso ai dati nell'oggetto DDE. Per condividere i dati in un oggetto DDE, un'applicazione passa l'handle di dati a DDEML e DDEML passa l'handle alla funzione di callback DDE dell'applicazione che riceve la transazione di dati.

Nell'esempio seguente viene illustrato come creare un oggetto DDE e ottenere un handle per l'oggetto. Durante la transazione [**XTYP \_ ADVREQ**](xtyp-advreq.md) , la funzione di callback converte l'ora corrente in una stringa ASCII, copia la stringa in un buffer locale e quindi crea un oggetto DDE che contiene la stringa. La funzione di callback restituisce l'handle per l'oggetto DDE (HDDEDATA) a DDEML, che passa l'handle all'applicazione client.


```
typedef struct tagTIME 
{ 
    INT     hour;   // 0 - 11 hours for analog clock 
    INT     hour12; // 12-hour format 
    INT     hour24; // 24-hour format 
    INT     minute; 
    INT     second; 
    INT     ampm;   // 0 - AM , 1 - PM 
} TIME; 
 
HDDEDATA EXPENTRY DdeCallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
 
    CHAR szBuf[32];
    HRESULT hResult;
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uType) 
    { 
    case XTYP_ADVREQ: 
        if ((hsz1 == hszTime && hsz2 == hszNow) && 
                (uFmt == CF_TEXT)) 
        { 
            // Copy the formatted string to a buffer. 
 
            itoa(tmTime.hour, szBuf, 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.minute < 10)
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
                if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            } 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.minute, &szBuf[*pcch], 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.second < 10) 
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.second, &szBuf[*pcch], 10);
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            } 
            szBuf[*pcch] = '\0'; 
 
            // Create a global object and return its data handle. 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            return (DdeCreateDataHandle( 
                idInst, 
                (LPBYTE) szBuf,     // instance identifier 
                *pcch + 1,          // source buffer length 
                0,                  // offset from beginning 
                hszNow,             // item name string 
                CF_TEXT,            // clipboard format 
                0));                // no creation flags 
        } else return (HDDEDATA) NULL; 
 
    // Process other transactions. 
    } 
} 
```



L'applicazione ricevente ottiene un puntatore all'oggetto DDE passando l'handle di dati alla funzione [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) . Il puntatore restituito da **DdeAccessData** fornisce l'accesso in sola lettura. L'applicazione deve usare il puntatore per esaminare i dati e quindi chiamare la funzione [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) per invalidare il puntatore. L'applicazione può copiare i dati in un buffer locale usando la funzione [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) .

Nell'esempio seguente viene ottenuto un puntatore all'oggetto DDE identificato dal parametro *hData* , viene copiato il contenuto in un buffer locale e quindi viene invalidato il puntatore.


```
HDDEDATA hdata; 
LPBYTE lpszAdviseData; 
DWORD cbDataLen; 
DWORD i; 
char szData[32]; 
 
// 
case XTYP_ADVDATA: 
    lpszAdviseData = DdeAccessData(hdata, &cbDataLen); 
    for (i = 0; i < cbDataLen; i++) 
        szData[i] = *lpszAdviseData++; 
    DdeUnaccessData(hdata); 
    return (HDDEDATA) TRUE; 
//
```



In genere, quando un'applicazione che ha creato un handle di dati passa tale handle a DDEML, l'handle diventa non valido nell'applicazione di creazione. Questa situazione non costituisce un problema se l'applicazione deve condividere i dati con una sola applicazione. Se un'applicazione deve condividere gli stessi dati con più applicazioni, tuttavia, l'applicazione di creazione deve specificare il \_ flag HDATA APPOWNED in [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle). In questo modo, la proprietà dell'oggetto DDE viene assegnata all'applicazione di creazione e impedisce a DDEML di invalidare l'handle di dati. L'applicazione può quindi passare l'handle di dati un numero qualsiasi di volte dopo la chiamata di **DdeCreateDataHandle** una sola volta.

Se un'applicazione specifica il \_ flag HDATA APPOWNED nel parametro *AfCmd* di [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), deve chiamare la funzione [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) per liberare l'handle di memoria, indipendentemente dal fatto che abbia passato l'handle a DDEML. Prima di terminare, un'applicazione deve chiamare **DdeFreeDataHandle** per liberare qualsiasi handle di dati creato ma non passato a DDEML.

Un'applicazione che non ha ancora passato l'handle a un oggetto DDE a DDEML può aggiungere dati all'oggetto o sovrascrivere i dati nell'oggetto tramite la funzione [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) . In genere, un'applicazione utilizza **DdeAddData** per riempire un oggetto DDE non inizializzato. Quando un'applicazione passa un handle di dati a DDEML, l'oggetto DDE identificato dall'handle non può essere modificato. può essere liberata.

 

 




