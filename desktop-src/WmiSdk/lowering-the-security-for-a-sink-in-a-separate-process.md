---
description: Strumentazione gestione Windows (WMI) può creare il sink per ricevere callback asincroni per un'applicazione client in un processo separato.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Riduzione della sicurezza per un sink in un processo separato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314597"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a>Riduzione della sicurezza per un sink in un processo separato

Strumentazione gestione Windows (WMI) può creare il sink per ricevere callback asincroni per un'applicazione client in un processo separato. Il processo separato è Unsecapp.exe. Usare l'interfaccia [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) . **IWbemUnsecuredApartment** consente di controllare se Unsecapp.exe autentica i callback per il sink. Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

È quindi possibile abbassare la sicurezza del processo e WMI può accedere al sink senza restrizioni. Per supportare questa tecnica, WMI fornisce il processo Unsecapp.exe per funzionare come processo separato. È possibile ospitare Unsecapp.exe con una chiamata all'interfaccia [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .

L'interfaccia [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) consente a un'applicazione client di creare un processo dedicato separato che esegue Unsecapp.exe per l'hosting di un'implementazione di [**IWbemObjectSink**](iwbemobjectsink.md) . Il processo dedicato può chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per concedere l'accesso WMI al processo dedicato senza compromettere la sicurezza del processo principale. Dopo l'inizializzazione, il processo dedicato funge da intermediario tra il processo principale e WMI.

Nella procedura seguente viene descritto come eseguire una chiamata asincrona con [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).

**Per eseguire una chiamata asincrona con IUnsecuredApartment**

1.  Creare un processo dedicato con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Nell'esempio di codice seguente viene chiamato [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un processo dedicato.

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  Creare un'istanza dell'oggetto sink.

    Nell'esempio di codice seguente viene creato un nuovo oggetto sink.

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  Creare uno stub per il sink.

    Uno Stub è una funzione wrapper prodotta dal sink.

    Nell'esempio di codice seguente viene chiamato [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) per creare uno stub per il sink.

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per il wrapper e richiedere un puntatore all'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .

    Nell'esempio di codice seguente viene chiamato [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e viene richiesto un puntatore all'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  Rilasciare il puntatore all'oggetto sink.

    È possibile rilasciare il puntatore all'oggetto perché lo stub è ora proprietario del puntatore.

    Nell'esempio di codice seguente viene rilasciato il puntatore all'oggetto sink.

    ```C++
    pSink->Release();
    ```

    

6.  Utilizzare lo stub in qualsiasi chiamata asincrona.

    Al termine della chiamata, rilasciare il conteggio dei riferimenti locali.

    Nell'esempio di codice seguente viene utilizzato lo stub in una chiamata asincrona.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    In alcuni casi potrebbe essere necessario annullare una chiamata asincrona dopo aver effettuato la chiamata. Se è necessario annullare la chiamata, annullare la chiamata con lo stesso puntatore che ha originariamente effettuato la chiamata.

    Nell'esempio di codice seguente viene illustrato come annullare una chiamata asincrona.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  Rilasciare il conteggio dei riferimenti locale al termine dell'utilizzo della chiamata asincrona.

    Assicurarsi di rilasciare il puntatore *pStubSink* solo dopo aver verificato che non è necessario annullare la chiamata asincrona. Inoltre, non rilasciare *pStubSink* dopo che WMI rilascia il puntatore di sink *pSink* . Il rilascio di *pStubSink* dopo *pSink* crea un conteggio dei riferimenti circolari in cui sia il sink che lo stub rimarranno sempre in memoria. Al contrario, una posizione possibile per rilasciare il puntatore si trova nella chiamata [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , eseguita da WMI per segnalare che la chiamata asincrona originale è stata completata.

8.  Al termine, annullare l'inizializzazione di COM con una chiamata a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

    Nell'esempio di codice seguente viene illustrato come chiamare [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore *pUnsecApp* .

    ```C++
    pUnsecApp->Release();
    ```

    

    Gli esempi di codice in questo argomento richiedono il riferimento e l' \# istruzione include seguenti per la corretta compilazione.

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

Per ulteriori informazioni sulla funzione e sui parametri [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , vedere la documentazione [com](../cossdk/component-services-portal.md) in Platform Software Development Kit (SDK).

 

 
