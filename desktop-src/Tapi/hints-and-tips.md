---
description: Di seguito sono riportati alcuni suggerimenti e suggerimenti da tenere in considerazione durante la scrittura di un'applicazione per TAPI 3
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Suggerimenti e suggerimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9202bdef97fb87b9f0736ed032b298af56917d8c
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321172"
---
# <a name="hints-and-tips"></a>Suggerimenti e suggerimenti

Di seguito sono riportati alcuni suggerimenti e suggerimenti da tenere in considerazione durante la scrittura di un'applicazione per TAPI 3:

1.  COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) crea indirettamente Windows; Questa operazione è particolarmente importante per il threading dell'Apartment. Se un thread crea qualsiasi finestra, deve elaborare i messaggi. Se i thread chiamano **CoInitialize**, eseguire un message pump per evitare problemi. Ad esempio, COM potrebbe interrompere correttamente il marshalling oppure i metodi su interfacce COM, ad esempio **IGlobalInterfaceTable** , potrebbero bloccarsi.

    Nel threading dell'Apartment è necessario disporre di un message pump indipendentemente dal fatto che si attendano gli oggetti di sincronizzazione. Questa operazione è particolarmente importante se si dispone di un'applicazione console o si scrive un oggetto server locale/remoto COM con threading Apartment (in cui non è presente una console o un'interfaccia utente grafica, ma il controllo viene semplicemente "eseguito" nel sistema).

    > [!Caution]  
    > Quando si chiamano le funzioni di attesa e di sincronizzazione, ad esempio [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)e così via. Usare invece [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ed elaborare i messaggi oppure usare [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), che rileverà automaticamente il tipo di Apartment in cui si trova il thread (sta o MTA) e aspetterà in un ciclo com (If sta) o in un blocco su **WaitForMultipleObjects** (se MTA). **MsgWaitForMultipleObjects** e **CoWaitForMultipleHandles** elaborano anche i messaggi di Windows in base alle regole com.

     

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

2.  **ITTAPIEventNotification:: Event** è la funzione di evento Apps chiamata in un thread di callback di TAPI 3.

    Eseguire il minimo nella routine di evento; usare invece il proprio thread laddove possibile.

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

3.  Non modificare gli oggetti COM dopo aver chiamato [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). I risultati sono imprevedibili e dannosi a un'applicazione integra. Alcuni esempi in cui questo può verificarsi sono i thread di lavoro e i distruttori C++ che possono essere eseguiti dopo che un'applicazione chiama **CoUninitialize**.

 

 
