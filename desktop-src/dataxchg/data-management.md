---
title: Gestione dati
description: In questo argomento viene illustrato come gli oggetti memoria passano i dati da un'applicazione a un'altra.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Windows Interfaccia utente,Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), gestione dei dati
- DDE (Dynamic Data Exchange),gestione dei dati
- scambio di dati, Dynamic Data Exchange (DDE)
- Windows Interfaccia utente,Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange Management Library (DDEML), gestione dei dati
- DDEML (Dynamic Data Exchange Management Library),gestione dati
- scambio di dati, Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange (DDE), oggetti
- DDE (Dynamic Data Exchange),oggetti
- Dynamic Data Exchange Management Library (DDEML), oggetti
- DDEML (Dynamic Data Exchange Management Library),oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dc9b8ccd82d184866ac9ed28f15bdeac424ec0bf9bd7767a520dea69bc4d11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953741"
---
# <a name="data-management"></a>Gestione dati

Poiché Dynamic Data Exchange (DDE) usa oggetti di memoria per passare dati da un'applicazione a un'altra, la libreria DDEML (Dynamic Data Exchange Management Library) fornisce un set di funzioni che le applicazioni DDE possono usare per creare e gestire oggetti DDE.

Tutte le transazioni che comportano lo scambio di dati richiedono all'applicazione di fornire i dati per creare un buffer locale contenente i dati e quindi chiamare la [**funzione DdeCreateDataHandle.**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) Questa funzione alloca un oggetto DDE, copia i dati dal buffer all'oggetto e restituisce un handle di dati. Un handle di dati è **un valore DWORD** utilizzato da DDEML per fornire l'accesso ai dati nell'oggetto DDE. Per condividere i dati in un oggetto DDE, un'applicazione passa l'handle di dati a DDEML e DDEML passa l'handle alla funzione di callback DDE dell'applicazione che riceve la transazione di dati.

Nell'esempio seguente viene illustrato come creare un oggetto DDE e ottenere un handle per l'oggetto . Durante la [**transazione \_ XTYP ADVREQ,**](xtyp-advreq.md) la funzione di callback converte l'ora corrente in una stringa ASCII, copia la stringa in un buffer locale e quindi crea un oggetto DDE contenente la stringa. La funzione di callback restituisce l'handle all'oggetto DDE (HDDEDATA) a DDEML, che passa l'handle all'applicazione client.


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



L'applicazione ricevente ottiene un puntatore all'oggetto DDE passando l'handle di dati alla [**funzione DdeAccessData.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) Il puntatore restituito **da DdeAccessData fornisce** l'accesso in sola lettura. L'applicazione deve usare il puntatore per esaminare i dati e quindi chiamare la [**funzione DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) per invalidare il puntatore. L'applicazione può copiare i dati in un buffer locale usando la [**funzione DdeGetData.**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)

L'esempio seguente ottiene un puntatore all'oggetto DDE identificato dal parametro *hData,* copia il contenuto in un buffer locale e quindi invalida il puntatore.


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



In genere, quando un'applicazione che ha creato un handle di dati passa tale handle a DDEML, l'handle non è più valido nell'applicazione di creazione. Questa situazione non rappresenta un problema se l'applicazione deve condividere i dati con una sola applicazione. Se un'applicazione deve condividere gli stessi dati con più applicazioni, tuttavia, l'applicazione che crea deve specificare il flag HDATA \_ APPOWNED in [**DdeCreateDataHandle.**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) In questo modo viene data la proprietà dell'oggetto DDE all'applicazione di creazione e si impedisce a DDEML di invalidare l'handle di dati. L'applicazione può quindi passare l'handle di dati un numero qualsiasi di volte dopo aver **chiamato DdeCreateDataHandle una** sola volta.

Se un'applicazione specifica il flag HDATA APPOWNED nel parametro \_ *afCmd* di [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), deve chiamare la funzione [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) per liberare l'handle di memoria, indipendentemente dal fatto che l'handle sia passato a DDEML. Prima del termine, un'applicazione deve chiamare **DdeFreeDataHandle** per liberare qualsiasi handle di dati creato ma non passato a DDEML.

Un'applicazione che non ha ancora passato l'handle a un oggetto DDE a DDEML può aggiungere dati all'oggetto o sovrascrivere i dati nell'oggetto usando la [**funzione DdeAddData.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) In genere, **un'applicazione usa DdeAddData** per riempire un oggetto DDE non inizializzato. Dopo che un'applicazione passa un handle di dati a DDEML, l'oggetto DDE identificato dall'handle non può essere modificato. può essere liberato solo.

 

 




