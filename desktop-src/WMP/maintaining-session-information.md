---
title: Gestione delle informazioni sulla sessione
description: Gestione delle informazioni sulla sessione
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, gestione delle informazioni sulla sessione
- archivi online, gestione delle informazioni sulla sessione
- digitare 2 archivi online, gestione delle informazioni sulla sessione
- Windows Media Player Online Stores, informazioni sulla sessione
- archivi online, informazioni sulla sessione
- digitare 2 archivi online, informazioni sulla sessione
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- gestione delle informazioni sulla sessione
- informazioni sulla sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332679"
---
# <a name="maintaining-session-information"></a>Gestione delle informazioni sulla sessione

## <a name="how-the-sample-stores-information"></a>Come archiviare le informazioni nell'esempio

La pagina Web di esempio gestisce i dati tramite cookie. I cookie sono semplicemente coppie nome/valore permanenti che possono essere archiviate dal Web browser.

Quando la pagina Web si chiude, viene eseguita la funzione **Shutdown** . **Shutdown** chiama la funzione **SetPendingCookies**. Questa funzione esegue il ciclo dell'elenco di raccolta di download, archiviato nella casella di riepilogo a discesa denominata selDLC. Se una raccolta di download contiene elementi incompleti, la funzione chiama il metodo **Secookie**, passando un nome e un valore. La stringa del nome viene determinata aggiungendo un valore integer a un valore costante, **WMPDLC**, archiviato nella variabile denominata g \_ sPreCookie. Per la terza raccolta di download in sospeso, ad esempio, il nome del cookie sarà "WMPDLC2", perché il meccanismo di conteggio è in base zero. Quando ogni cookie viene creato, la funzione incrementa la variabile globale g \_ in sospeso per contenere un conteggio dei download in sospeso. Il codice viene riprodotto qui per praticità:


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



**IsDLCComplete** è una funzione di supporto che esegue semplicemente il ciclo di ogni elemento di download nella raccolta di download per determinare se un elemento è in sospeso. Se è presente un elemento in sospeso, la funzione restituisce false.

**Secookie** è la funzione che crea il cookie.

Quando **SetPendingCookies** restituisce, **Shutdown** crea il cookie di conteggio, che archivia il valore dalla variabile g \_ in sospeso. Questo valore è importante perché la pagina Web richiede un modo per determinare il numero di cookie da recuperare quando viene ricaricato. Il nome del cookie di conteggio viene archiviato nella variabile denominata g \_ sCountCookie.

## <a name="how-the-sample-retrieves-information"></a>Come vengono recuperate le informazioni nell'esempio

Quando viene caricata la pagina Web, viene eseguita la funzione **init** . Per prima cosa, la funzione chiama **GetPendingDlCount** per recuperare il cookie di conteggio. Quindi Archivia questo valore nella variabile denominata g \_ in sospeso. Chiama quindi la funzione **PopulateDLList** per recuperare ogni cookie della sessione di download e aggiungere il relativo identificatore alla casella di riepilogo a discesa. Ecco il codice per la funzione:


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



La funzione **Clear** list rimuove tutti gli elementi dalla casella di riepilogo.

La funzione immette quindi un ciclo. Ogni nome di cookie viene compilato come stringa e quindi il cookie viene recuperato chiamando la funzione helper **GetCookie**. Una volta recuperato, il cookie viene eliminato chiamando **DelCookie**. Se il cookie ha un valore, il valore viene aggiunto alla casella di riepilogo. Questa azione avvia l'evento **OnChange** per l'elenco selDLC, che a sua volta chiama la funzione di gestione denominata **OnSelectDLC**. Si tratta della stessa funzione che viene eseguita quando l'utente seleziona una raccolta di download; si tratta del codice che compila la casella di riepilogo Scarica elemento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di Download Manager**](using-the-download-manager.md)
</dt> </dl>

 

 




