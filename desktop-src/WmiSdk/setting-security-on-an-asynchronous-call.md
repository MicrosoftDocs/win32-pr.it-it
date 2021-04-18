---
description: Le chiamate asincrone presentano gravi rischi di sicurezza perché una richiamata al sink potrebbe non essere il risultato della chiamata asincrona da parte dell'applicazione o dello script originale.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Impostazione della sicurezza per una chiamata asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318525"
---
# <a name="setting-security-on-an-asynchronous-call"></a>Impostazione della sicurezza per una chiamata asincrona

Le chiamate asincrone presentano gravi rischi di sicurezza perché una richiamata al [*sink*](gloss-s.md) potrebbe non essere il risultato della chiamata asincrona da parte dell'applicazione o dello script originale. La sicurezza nelle connessioni remote è basata sulla crittografia della comunicazione tra il client e il provider nel computer remoto. In C++ è possibile impostare la crittografia tramite il parametro del livello di autenticazione nella chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). In scripting impostare *AuthenticationLevel* nella connessione del moniker o in un oggetto [**SWbemSecurity**](swbemsecurity.md) . Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

I rischi per la sicurezza per le chiamate asincrone sono dovuti al fatto che WMI abbassa il livello di autenticazione in un callback finché il callback non riesce. In una chiamata asincrona in uscita, il client può impostare il livello di autenticazione per la connessione a WMI. WMI recupera le impostazioni di sicurezza nella chiamata client e tenta di richiamare con lo stesso livello di autenticazione. Il callback viene sempre avviato a livello di **\_ \_ \_ \_ \_ privacy PKT del livello auth C RPC** . Se il callback ha esito negativo, WMI abbassa il livello di autenticazione a un livello in cui il callback può avere esito positivo, se necessario, per il livello di autenticazione **RPC \_ C \_ \_ \_**. Nel contesto delle chiamate all'interno del sistema locale in cui il servizio di autenticazione non è Kerberos, il callback viene sempre restituito a **\_ \_ livello auth \_ \_ C RPC**.

Il livello di autenticazione minimo è il **\_ \_ livello auth \_ C \_ PKT** (**wbemAuthenticationLevelPkt** per lo scripting). Tuttavia, è possibile specificare un livello superiore, ad esempio **la \_ \_ privacy del livello di autenticazione \_ \_ PKT \_** (**wbemAuthenticationLevelPktPrivacy**) RPC C. È consigliabile che le applicazioni client o gli script impostino il livello di autenticazione sul **\_ \_ \_ \_ valore predefinito del livello di autenticazione RPC C** (**wbemAuthenticationLevelDefault**), che consente la negoziazione del livello di autenticazione al livello specificato dal server.

Il valore del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controlla se WMI controlla la presenza di un livello di autenticazione accettabile nei callback. Questo è l'unico meccanismo per proteggere la sicurezza del sink per le chiamate asincrone effettuate in script o Visual Basic. Per impostazione predefinita, questa chiave del registro di sistema è impostata su zero. Se la chiave del registro di sistema è zero, WMI non verifica i livelli di autenticazione. Per proteggere le chiamate asincrone nello scripting, impostare la chiave del registro di sistema su 1. I client C++ possono chiamare [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) per controllare l'accesso al sink. Per impostazione predefinita, il valore viene creato ovunque.

Negli argomenti seguenti vengono forniti esempi di impostazione della sicurezza delle chiamate asincrone:

-   [Impostazione della sicurezza per una chiamata asincrona in VBScript](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   Impostazione della sicurezza delle chiamate asincrone in C++

## <a name="setting-asynchronous-call-security-in-c"></a>Impostazione della sicurezza delle chiamate asincrone in C++

Il metodo [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) è simile al metodo [**IUnsecuredApartment:: CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) e crea un sink in un processo separato, Unsecapp.exe, per ricevere i callback. Tuttavia, il metodo **CreateSinkStub** dispone di un parametro *dwFlag* che specifica il modo in cui il processo separato gestisce il controllo di accesso.

Il parametro *dwFlag* specifica una delle azioni seguenti per Unsecapp.exe:

-   Utilizzare l'impostazione della chiave del registro di sistema per determinare se controllare o meno l'accesso.
-   Ignorare la chiave del registro di sistema e controllare sempre l'accesso.
-   Ignorare la chiave del registro di sistema e non controllare mai l'accesso.

Per eseguire correttamente la compilazione, l'esempio di codice in questo argomento richiede la seguente \# istruzione include.


```C++
#include <wbemidl.h>
```



Nella procedura seguente viene descritto come eseguire una chiamata asincrona con [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).

**Per eseguire una chiamata asincrona con IWbemUnsecuredApartment**

1.  Creare un processo dedicato con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Nell'esempio di codice seguente viene chiamato [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un processo dedicato.

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
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

    Nell'esempio di codice seguente viene creato uno stub per il sink.

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  Rilasciare il puntatore all'oggetto sink.

    È possibile rilasciare il puntatore all'oggetto perché lo stub è ora proprietario del puntatore.

    Nell'esempio di codice seguente viene rilasciato il puntatore all'oggetto.

    ```C++
    pSink->Release();
    ```

    

5.  Utilizzare lo stub in qualsiasi chiamata asincrona.

    Al termine della chiamata, rilasciare il conteggio dei riferimenti locali.

    Nell'esempio di codice seguente viene utilizzato lo stub in una chiamata asincrona.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    In alcuni casi potrebbe essere necessario annullare una chiamata asincrona dopo aver effettuato la chiamata. Se è necessario annullare la chiamata, annullare la chiamata con lo stesso puntatore che ha originariamente effettuato la chiamata.

    Nell'esempio di codice riportato di seguito viene descritto come annullare una chiamata asincrona.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  Rilasciare il conteggio dei riferimenti locale al termine dell'utilizzo della chiamata asincrona.

    Assicurarsi di rilasciare il puntatore *pStubSink* solo dopo aver verificato che la chiamata asincrona non deve essere annullata. Inoltre, non rilasciare *pStubSink* dopo che WMI rilascia il puntatore di sink *pSink* . Il rilascio di *pStubSink* dopo *pSink* crea un conteggio dei riferimenti circolari in cui sia il sink che lo stub rimarranno sempre in memoria. Al contrario, una posizione possibile per rilasciare il puntatore si trova nella chiamata [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , eseguita da WMI per segnalare che la chiamata asincrona originale è stata completata.

7.  Al termine, annullare l'inizializzazione di COM con una chiamata a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

    Nell'esempio di codice seguente viene illustrato come chiamare [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore *pUnsecApp* .

    ```C++
    pUnsecApp->Release();
    ```

    

Per ulteriori informazioni sulla funzione e sui parametri [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , vedere la documentazione [com](../cossdk/component-services-portal.md) .

 

 
