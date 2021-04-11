---
title: Informazioni sui controlli Rich Edit senza finestra
description: Un controllo Rich Edit senza finestra, noto anche come oggetto servizi di testo, è un oggetto che fornisce la funzionalità di un controllo Rich Edit senza fornire la finestra.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1c8bc685dff5f8ddb041011089a84eb2e12008
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963477"
---
# <a name="about-windowless-rich-edit-controls"></a>Informazioni sui controlli Rich Edit senza finestra

Un controllo Rich Edit senza finestra, noto anche come oggetto servizi di testo, è un oggetto che fornisce la funzionalità di un [controllo Rich Edit](rich-edit-controls.md) senza fornire la finestra. Per fornire la funzionalità di una finestra, ad esempio la possibilità di ricevere messaggi e un contesto di dispositivo in cui è possibile creare, i controlli Rich Edit senza finestra usano una coppia di interfacce: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

Per creare un controllo Rich Edit senza finestra, chiamare la funzione [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) con un puntatore all'implementazione dell'interfaccia [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) . **CreateTextServices** restituisce un puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) su cui è possibile eseguire una query per recuperare un puntatore all'implementazione [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) del controllo privo di finestra.

Msftedit.dll esporta un identificatore di interfaccia (IID) denominato **IID \_ ITextServices** che è possibile usare per eseguire una query sul puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) per l'interfaccia [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . Nell'esempio seguente viene illustrato come recuperare **IID \_ ITextServices** e usarlo per ottenere l'interfaccia **ITextServices** .


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



Msftedit.dll esporta anche un identificatore di interfaccia (IID) denominato **IID \_ ITextHost** che può essere usato in modo analogo per eseguire query per l'interfaccia [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .

L'interfaccia [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) dispone di metodi che il controllo senza finestra chiama per recuperare informazioni sulla finestra. Ad esempio, l'oggetto servizi di testo chiama il metodo [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) per recuperare un contesto di dispositivo in cui può essere disegnato. Il controllo senza finestra chiama il metodo [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) per l'invio di notifiche, ad esempio i messaggi di notifica Rich Edit, all'host di testo. L'oggetto servizi di testo chiama altri metodi **ITextHost** per richiedere all'host di testo di eseguire altri servizi correlati alla finestra. Ad esempio, il metodo [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) richiede all'host di testo di aggiungere un rettangolo all'area di aggiornamento della finestra.

Un controllo Rich Edit standard prevede una procedura finestra che elabora messaggi di sistema e messaggi dall'applicazione. È possibile usare l'handle della finestra del controllo per inviare i messaggi per l'esecuzione di modifiche del testo e altre operazioni. Tuttavia, un controllo Rich Edit senza finestra non ha alcuna routine di finestra per la ricezione e l'elaborazione dei messaggi. Fornisce invece un'interfaccia [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . Per inviare messaggi a un controllo Rich Edit senza finestra, chiamare il metodo [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) . È possibile utilizzare questo metodo per inviare qualsiasi messaggio Rich Edit o per passare altri messaggi che interessano il controllo, ad esempio i messaggi di sistema per l'input del mouse o della tastiera.

È anche possibile creare l'oggetto servizi di testo come parte di un [oggetto aggregato com](/windows/desktop/com/aggregation). In questo modo è più semplice aggregare l'oggetto servizi di testo con un oggetto Component Object Model senza finestra (COM).

 

 