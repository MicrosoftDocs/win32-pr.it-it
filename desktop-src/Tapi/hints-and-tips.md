---
description: Di seguito sono riportati suggerimenti e suggerimenti da considerare quando si scrive un'applicazione per TAPI 3
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Suggerimenti e Suggerimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d51e8c7e3f8c6e4a9e38b27fa5cfe4c10e45d37cfa67af095d573eea319614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762935"
---
# <a name="hints-and-tips"></a>Suggerimenti e Suggerimenti

Di seguito sono riportati suggerimenti e suggerimenti da considerare quando si scrive un'applicazione per TAPI 3:

1.  Com [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) crea indirettamente finestre. Ciò è particolarmente importante per il threading di apartment. Se un thread crea finestre, deve elaborare i messaggi. Se i thread chiamano **CoInitialize,** eseguire un message pump per evitare problemi. Ad esempio, COM potrebbe interrompere correttamente il marshalling oppure i metodi nelle interfacce COM, ad esempio **IGlobalInterfaceTable,** potrebbero bloccarsi.

    Nel threading di apartment è necessario disporre di un message pump indipendentemente dal fatto che si attenda o meno gli oggetti di sincronizzazione. Ciò è particolarmente importante se si dispone di un'applicazione console o si scrive un oggetto server locale/remoto COM con thread apartment (in cui non si dispone di una console o di un'interfaccia utente grafica, ma il controllo viene semplicemente "eseguito" nel sistema).

    > [!Caution]  
    > Quando si chiamano le funzioni di attesa e sincronizzazione, ad esempio [**Sleep,**](/windows/desktop/api/synchapi/nf-synchapi-sleep) [**WaitForMultipleObjects,**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) [**WaitForMultipleObjectsEx,**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex) [**WaitForSingleObject,**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)e così via. Usare invece [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ed elaborare i messaggi oppure [**usare CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), che rileverà automaticamente il tipo di apartment in cui si trova il thread (STA o MTA) e attenderà in un ciclo modale COM (se STA) o in un blocco **in WaitForMultipleObjects** (se MTA). **Anche MsgWaitForMultipleObjects** e **CoWaitForMultipleHandles** elaborano i messaggi di Windows in base alle regole COM.

     

    Ad esempio, anziché:

    `Sleep (5000);`

    Usare:

    ``` syntax
     {
       DWORD dwSignalled;
       HANDLE heventDone = CreateEvent(0, FALSE, FALSE, 0);

       CoWaitForMultipleHandles (COWAIT_ALERTABLE,
                             5000,
                             1,
                             &heventDone,
                             &dwSignalled);

       CloseHandle(heventDone);
     }
    ```

2.  **ITTAPIEventNotification::Event** è la funzione Event delle app chiamata in un thread di callback TAPI 3.

    Eseguire il valore minimo nella routine Event. usare invece il proprio thread, laddove possibile.

    Tenere presente che viene fornito l'esempio di codice seguente, ma non è un requisito.

    ```syntax
    #include <windows.h>

    HRESULT
    STDMETHODCALLTYPE
    CTAPIEventNotification::Event(
        TAPI_EVENT TapiEvent,
        IDispatch *pEvent)
    {
        //
        // Addref the event so that it does not go away.
        //
        pEvent->AddRef();

        //
        // Post a message for reference.
        //
        BOOL RetVal = PostMessage(
                                  ghDlg,
                                  WM_PRIVATETAPIEVENT,
                                  (WPARAM) TapiEvent,
                                  (LPARAM) pEvent
                                  );

        // If (RetVal == 0 ) process error here.

        return S_OK;
    }     
    ```

3.  Non modificare gli oggetti COM dopo aver chiamato [**CoUninitialize.**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) I risultati sono imprevedibili e dannosi per un'applicazione integra. Alcuni esempi in cui ciò può verificarsi sono i thread di lavoro e i distruttori C++ che possono essere eseguiti dopo che un'applicazione chiama **CoUninitialize.**

 

 
