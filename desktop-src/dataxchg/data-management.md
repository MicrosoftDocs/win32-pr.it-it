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
# <a name="data-management"></a><span data-ttu-id="5f0f5-115">Gestione dati</span><span class="sxs-lookup"><span data-stu-id="5f0f5-115">Data Management</span></span>

<span data-ttu-id="5f0f5-116">Poiché Dynamic Data Exchange (DDE) utilizza oggetti memoria per passare dati da un'applicazione a un'altra, la libreria di gestione Dynamic Data Exchange (DDEML) fornisce un set di funzioni che le applicazioni DDE possono utilizzare per creare e gestire oggetti DDE.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-116">Because Dynamic Data Exchange (DDE) uses memory objects to pass data from one application to another, the Dynamic Data Exchange Management Library (DDEML) provides a set of functions that DDE applications can use to create and manage DDE objects.</span></span>

<span data-ttu-id="5f0f5-117">Per tutte le transazioni che comportano lo scambio di dati, è necessario che l'applicazione fornisca i dati per creare un buffer locale contenente i dati e quindi chiamare la funzione [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) .</span><span class="sxs-lookup"><span data-stu-id="5f0f5-117">All transactions that involve the exchange of data require the application supplying the data to create a local buffer containing the data and then to call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function.</span></span> <span data-ttu-id="5f0f5-118">Questa funzione alloca un oggetto DDE, copia i dati dal buffer nell'oggetto e restituisce un handle di dati.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-118">This function allocates a DDE object, copies the data from the buffer to the object, and returns a data handle.</span></span> <span data-ttu-id="5f0f5-119">Un handle di dati è un valore **DWORD** utilizzato dal DDEML per fornire l'accesso ai dati nell'oggetto DDE.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-119">A data handle is a **DWORD** value that the DDEML uses to provide access to data in the DDE object.</span></span> <span data-ttu-id="5f0f5-120">Per condividere i dati in un oggetto DDE, un'applicazione passa l'handle di dati a DDEML e DDEML passa l'handle alla funzione di callback DDE dell'applicazione che riceve la transazione di dati.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-120">To share the data in a DDE object, an application passes the data handle to the DDEML, and the DDEML passes the handle to the DDE callback function of the application that is receiving the data transaction.</span></span>

<span data-ttu-id="5f0f5-121">Nell'esempio seguente viene illustrato come creare un oggetto DDE e ottenere un handle per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-121">The following example shows how to create a DDE object and obtain a handle to the object.</span></span> <span data-ttu-id="5f0f5-122">Durante la transazione [**XTYP \_ ADVREQ**](xtyp-advreq.md) , la funzione di callback converte l'ora corrente in una stringa ASCII, copia la stringa in un buffer locale e quindi crea un oggetto DDE che contiene la stringa.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-122">During the [**XTYP\_ADVREQ**](xtyp-advreq.md) transaction, the callback function converts the current time to an ASCII string, copies the string to a local buffer, and then creates a DDE object that contains the string.</span></span> <span data-ttu-id="5f0f5-123">La funzione di callback restituisce l'handle per l'oggetto DDE (HDDEDATA) a DDEML, che passa l'handle all'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-123">The callback function returns the handle to the DDE object (HDDEDATA) to the DDEML, which passes the handle to the client application.</span></span>


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



<span data-ttu-id="5f0f5-124">L'applicazione ricevente ottiene un puntatore all'oggetto DDE passando l'handle di dati alla funzione [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) .</span><span class="sxs-lookup"><span data-stu-id="5f0f5-124">The receiving application obtains a pointer to the DDE object by passing the data handle to the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function.</span></span> <span data-ttu-id="5f0f5-125">Il puntatore restituito da **DdeAccessData** fornisce l'accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-125">The pointer returned by **DdeAccessData** provides read-only access.</span></span> <span data-ttu-id="5f0f5-126">L'applicazione deve usare il puntatore per esaminare i dati e quindi chiamare la funzione [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) per invalidare il puntatore.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-126">The application should use the pointer to review the data and then call the [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) function to invalidate the pointer.</span></span> <span data-ttu-id="5f0f5-127">L'applicazione può copiare i dati in un buffer locale usando la funzione [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) .</span><span class="sxs-lookup"><span data-stu-id="5f0f5-127">The application can copy the data to a local buffer by using the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function.</span></span>

<span data-ttu-id="5f0f5-128">Nell'esempio seguente viene ottenuto un puntatore all'oggetto DDE identificato dal parametro *hData* , viene copiato il contenuto in un buffer locale e quindi viene invalidato il puntatore.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-128">The following example obtains a pointer to the DDE object identified by the *hData* parameter, copies the contents to a local buffer, and then invalidates the pointer.</span></span>


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



<span data-ttu-id="5f0f5-129">In genere, quando un'applicazione che ha creato un handle di dati passa tale handle a DDEML, l'handle diventa non valido nell'applicazione di creazione.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-129">Usually, when an application that created a data handle passes that handle to the DDEML, the handle becomes invalid in the creating application.</span></span> <span data-ttu-id="5f0f5-130">Questa situazione non costituisce un problema se l'applicazione deve condividere i dati con una sola applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-130">This situation is not a problem if the application must share data with only a single application.</span></span> <span data-ttu-id="5f0f5-131">Se un'applicazione deve condividere gli stessi dati con più applicazioni, tuttavia, l'applicazione di creazione deve specificare il \_ flag HDATA APPOWNED in [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle).</span><span class="sxs-lookup"><span data-stu-id="5f0f5-131">If an application must share the same data with multiple applications, however, the creating application should specify the HDATA\_APPOWNED flag in [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle).</span></span> <span data-ttu-id="5f0f5-132">In questo modo, la proprietà dell'oggetto DDE viene assegnata all'applicazione di creazione e impedisce a DDEML di invalidare l'handle di dati.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-132">Doing so gives ownership of the DDE object to the creating application and prevents the DDEML from invalidating the data handle.</span></span> <span data-ttu-id="5f0f5-133">L'applicazione può quindi passare l'handle di dati un numero qualsiasi di volte dopo la chiamata di **DdeCreateDataHandle** una sola volta.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-133">The application can then pass the data handle any number of times after calling **DdeCreateDataHandle** only once.</span></span>

<span data-ttu-id="5f0f5-134">Se un'applicazione specifica il \_ flag HDATA APPOWNED nel parametro *AfCmd* di [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), deve chiamare la funzione [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) per liberare l'handle di memoria, indipendentemente dal fatto che abbia passato l'handle a DDEML.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-134">If an application specifies the HDATA\_APPOWNED flag in the *afCmd* parameter of [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), it must call the [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) function to free the memory handle, regardless of whether it passed the handle to the DDEML.</span></span> <span data-ttu-id="5f0f5-135">Prima di terminare, un'applicazione deve chiamare **DdeFreeDataHandle** per liberare qualsiasi handle di dati creato ma non passato a DDEML.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-135">Before it terminates, an application must call **DdeFreeDataHandle** to free any data handle that it created but did not pass to the DDEML.</span></span>

<span data-ttu-id="5f0f5-136">Un'applicazione che non ha ancora passato l'handle a un oggetto DDE a DDEML può aggiungere dati all'oggetto o sovrascrivere i dati nell'oggetto tramite la funzione [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) .</span><span class="sxs-lookup"><span data-stu-id="5f0f5-136">An application that has not yet passed the handle to a DDE object to the DDEML can add data to the object or overwrite data in the object by using the [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) function.</span></span> <span data-ttu-id="5f0f5-137">In genere, un'applicazione utilizza **DdeAddData** per riempire un oggetto DDE non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-137">Typically, an application uses **DdeAddData** to fill an uninitialized DDE object.</span></span> <span data-ttu-id="5f0f5-138">Quando un'applicazione passa un handle di dati a DDEML, l'oggetto DDE identificato dall'handle non può essere modificato. può essere liberata.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-138">After an application passes a data handle to the DDEML, the DDE object identified by the handle cannot be changed; it can only be freed.</span></span>

 

 




