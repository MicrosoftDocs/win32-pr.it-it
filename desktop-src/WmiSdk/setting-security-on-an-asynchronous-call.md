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
# <a name="setting-security-on-an-asynchronous-call"></a><span data-ttu-id="ac7df-103">Impostazione della sicurezza per una chiamata asincrona</span><span class="sxs-lookup"><span data-stu-id="ac7df-103">Setting Security on an Asynchronous Call</span></span>

<span data-ttu-id="ac7df-104">Le chiamate asincrone presentano gravi rischi di sicurezza perché una richiamata al [*sink*](gloss-s.md) potrebbe non essere il risultato della chiamata asincrona da parte dell'applicazione o dello script originale.</span><span class="sxs-lookup"><span data-stu-id="ac7df-104">Asynchronous calls present serious security risks because a callback to the [*sink*](gloss-s.md) may not be a result of the asynchronous call by the original application or script.</span></span> <span data-ttu-id="ac7df-105">La sicurezza nelle connessioni remote è basata sulla crittografia della comunicazione tra il client e il provider nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="ac7df-105">Security in remote connections is based on encryption of the communication between the client and the provider on the remote computer.</span></span> <span data-ttu-id="ac7df-106">In C++ è possibile impostare la crittografia tramite il parametro del livello di autenticazione nella chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="ac7df-106">In C++ you can set encryption through the authentication level parameter in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="ac7df-107">In scripting impostare *AuthenticationLevel* nella connessione del moniker o in un oggetto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="ac7df-107">In scripting, set the *AuthenticationLevel* in the moniker connection or on an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="ac7df-108">Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="ac7df-108">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="ac7df-109">I rischi per la sicurezza per le chiamate asincrone sono dovuti al fatto che WMI abbassa il livello di autenticazione in un callback finché il callback non riesce.</span><span class="sxs-lookup"><span data-stu-id="ac7df-109">The security risks for asynchronous calls exist because WMI lowers the authentication level on a callback until the callback succeeds.</span></span> <span data-ttu-id="ac7df-110">In una chiamata asincrona in uscita, il client può impostare il livello di autenticazione per la connessione a WMI.</span><span class="sxs-lookup"><span data-stu-id="ac7df-110">On an outgoing asynchronous call, the client can set the authentication level on the connection to WMI.</span></span> <span data-ttu-id="ac7df-111">WMI recupera le impostazioni di sicurezza nella chiamata client e tenta di richiamare con lo stesso livello di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ac7df-111">WMI retrieves the security settings on the client call and attempts to call back with the same authentication level.</span></span> <span data-ttu-id="ac7df-112">Il callback viene sempre avviato a livello di **\_ \_ \_ \_ \_ privacy PKT del livello auth C RPC** .</span><span class="sxs-lookup"><span data-stu-id="ac7df-112">The callback is always initiated at the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** level.</span></span> <span data-ttu-id="ac7df-113">Se il callback ha esito negativo, WMI abbassa il livello di autenticazione a un livello in cui il callback può avere esito positivo, se necessario, per il livello di autenticazione **RPC \_ C \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="ac7df-113">If the callback fails, WMI lowers the authentication level to a level where the callback can succeed, if necessary, to **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span> <span data-ttu-id="ac7df-114">Nel contesto delle chiamate all'interno del sistema locale in cui il servizio di autenticazione non è Kerberos, il callback viene sempre restituito a **\_ \_ livello auth \_ \_ C RPC**.</span><span class="sxs-lookup"><span data-stu-id="ac7df-114">In the context of calls within the local system where the authentication service is not Kerberos, the callback is always returned at **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span>

<span data-ttu-id="ac7df-115">Il livello di autenticazione minimo è il **\_ \_ livello auth \_ C \_ PKT** (**wbemAuthenticationLevelPkt** per lo scripting).</span><span class="sxs-lookup"><span data-stu-id="ac7df-115">The minimum authentication level is **RPC\_C\_AUTHN\_LEVEL\_PKT** (**wbemAuthenticationLevelPkt** for scripting).</span></span> <span data-ttu-id="ac7df-116">Tuttavia, è possibile specificare un livello superiore, ad esempio **la \_ \_ privacy del livello di autenticazione \_ \_ PKT \_** (**wbemAuthenticationLevelPktPrivacy**) RPC C.</span><span class="sxs-lookup"><span data-stu-id="ac7df-116">However, you can specify a higher level, such as **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="ac7df-117">È consigliabile che le applicazioni client o gli script impostino il livello di autenticazione sul **\_ \_ \_ \_ valore predefinito del livello di autenticazione RPC C** (**wbemAuthenticationLevelDefault**), che consente la negoziazione del livello di autenticazione al livello specificato dal server.</span><span class="sxs-lookup"><span data-stu-id="ac7df-117">It is recommended that client applications or scripts set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** (**wbemAuthenticationLevelDefault**) which allows the authentication level to be negotiated to the level specified by the server.</span></span>

<span data-ttu-id="ac7df-118">Il valore del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controlla se WMI controlla la presenza di un livello di autenticazione accettabile nei callback.</span><span class="sxs-lookup"><span data-stu-id="ac7df-118">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level in callbacks.</span></span> <span data-ttu-id="ac7df-119">Questo è l'unico meccanismo per proteggere la sicurezza del sink per le chiamate asincrone effettuate in script o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ac7df-119">This is the only mechanism for protecting sink security for asynchronous calls made in scripting or Visual Basic.</span></span> <span data-ttu-id="ac7df-120">Per impostazione predefinita, questa chiave del registro di sistema è impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="ac7df-120">By default, this registry key is set to zero.</span></span> <span data-ttu-id="ac7df-121">Se la chiave del registro di sistema è zero, WMI non verifica i livelli di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ac7df-121">If the registry key is zero then WMI does not verify authentication levels.</span></span> <span data-ttu-id="ac7df-122">Per proteggere le chiamate asincrone nello scripting, impostare la chiave del registro di sistema su 1.</span><span class="sxs-lookup"><span data-stu-id="ac7df-122">To secure asynchronous calls in scripting, set the registry key to 1.</span></span> <span data-ttu-id="ac7df-123">I client C++ possono chiamare [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) per controllare l'accesso al sink.</span><span class="sxs-lookup"><span data-stu-id="ac7df-123">C++ clients can call [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) to control access to the sink.</span></span> <span data-ttu-id="ac7df-124">Per impostazione predefinita, il valore viene creato ovunque.</span><span class="sxs-lookup"><span data-stu-id="ac7df-124">The value is created anywhere by default.</span></span>

<span data-ttu-id="ac7df-125">Negli argomenti seguenti vengono forniti esempi di impostazione della sicurezza delle chiamate asincrone:</span><span class="sxs-lookup"><span data-stu-id="ac7df-125">The following topics provide examples of setting asynchronous call security:</span></span>

-   [<span data-ttu-id="ac7df-126">Impostazione della sicurezza per una chiamata asincrona in VBScript</span><span class="sxs-lookup"><span data-stu-id="ac7df-126">Setting Security on an Asynchronous Call in VBScript</span></span>](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   <span data-ttu-id="ac7df-127">Impostazione della sicurezza delle chiamate asincrone in C++</span><span class="sxs-lookup"><span data-stu-id="ac7df-127">Setting Asynchronous Call Security in C++</span></span>

## <a name="setting-asynchronous-call-security-in-c"></a><span data-ttu-id="ac7df-128">Impostazione della sicurezza delle chiamate asincrone in C++</span><span class="sxs-lookup"><span data-stu-id="ac7df-128">Setting Asynchronous Call Security in C++</span></span>

<span data-ttu-id="ac7df-129">Il metodo [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) è simile al metodo [**IUnsecuredApartment:: CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) e crea un sink in un processo separato, Unsecapp.exe, per ricevere i callback.</span><span class="sxs-lookup"><span data-stu-id="ac7df-129">The [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) method is similar to [**IUnsecuredApartment::CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) method and creates a sink in a separate process, Unsecapp.exe, to receive callbacks.</span></span> <span data-ttu-id="ac7df-130">Tuttavia, il metodo **CreateSinkStub** dispone di un parametro *dwFlag* che specifica il modo in cui il processo separato gestisce il controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="ac7df-130">However, the **CreateSinkStub** method has a *dwFlag* parameter that specifies how the separate process handles access control.</span></span>

<span data-ttu-id="ac7df-131">Il parametro *dwFlag* specifica una delle azioni seguenti per Unsecapp.exe:</span><span class="sxs-lookup"><span data-stu-id="ac7df-131">The *dwFlag* parameter specifies one of the following actions for Unsecapp.exe:</span></span>

-   <span data-ttu-id="ac7df-132">Utilizzare l'impostazione della chiave del registro di sistema per determinare se controllare o meno l'accesso.</span><span class="sxs-lookup"><span data-stu-id="ac7df-132">Use the registry key setting to determine whether or not to check access.</span></span>
-   <span data-ttu-id="ac7df-133">Ignorare la chiave del registro di sistema e controllare sempre l'accesso.</span><span class="sxs-lookup"><span data-stu-id="ac7df-133">Ignore the registry key and always check access.</span></span>
-   <span data-ttu-id="ac7df-134">Ignorare la chiave del registro di sistema e non controllare mai l'accesso.</span><span class="sxs-lookup"><span data-stu-id="ac7df-134">Ignore the registry key and never check access.</span></span>

<span data-ttu-id="ac7df-135">Per eseguire correttamente la compilazione, l'esempio di codice in questo argomento richiede la seguente \# istruzione include.</span><span class="sxs-lookup"><span data-stu-id="ac7df-135">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="ac7df-136">Nella procedura seguente viene descritto come eseguire una chiamata asincrona con [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="ac7df-136">The following procedure describes how to perform an asynchronous call with [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span></span>

<span data-ttu-id="ac7df-137">**Per eseguire una chiamata asincrona con IWbemUnsecuredApartment**</span><span class="sxs-lookup"><span data-stu-id="ac7df-137">**To perform an asynchronous call with IWbemUnsecuredApartment**</span></span>

1.  <span data-ttu-id="ac7df-138">Creare un processo dedicato con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="ac7df-138">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="ac7df-139">Nell'esempio di codice seguente viene chiamato [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un processo dedicato.</span><span class="sxs-lookup"><span data-stu-id="ac7df-139">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
                     (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="ac7df-140">Creare un'istanza dell'oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="ac7df-140">Instantiate the sink object.</span></span>

    <span data-ttu-id="ac7df-141">Nell'esempio di codice seguente viene creato un nuovo oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="ac7df-141">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="ac7df-142">Creare uno stub per il sink.</span><span class="sxs-lookup"><span data-stu-id="ac7df-142">Create a stub for the sink.</span></span>

    <span data-ttu-id="ac7df-143">Uno Stub è una funzione wrapper prodotta dal sink.</span><span class="sxs-lookup"><span data-stu-id="ac7df-143">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="ac7df-144">Nell'esempio di codice seguente viene creato uno stub per il sink.</span><span class="sxs-lookup"><span data-stu-id="ac7df-144">The following code example creates a stub for the sink.</span></span>

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  <span data-ttu-id="ac7df-145">Rilasciare il puntatore all'oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="ac7df-145">Release the sink object pointer.</span></span>

    <span data-ttu-id="ac7df-146">È possibile rilasciare il puntatore all'oggetto perché lo stub è ora proprietario del puntatore.</span><span class="sxs-lookup"><span data-stu-id="ac7df-146">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="ac7df-147">Nell'esempio di codice seguente viene rilasciato il puntatore all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ac7df-147">The following code example releases the object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

5.  <span data-ttu-id="ac7df-148">Utilizzare lo stub in qualsiasi chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="ac7df-148">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="ac7df-149">Al termine della chiamata, rilasciare il conteggio dei riferimenti locali.</span><span class="sxs-lookup"><span data-stu-id="ac7df-149">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="ac7df-150">Nell'esempio di codice seguente viene utilizzato lo stub in una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="ac7df-150">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="ac7df-151">In alcuni casi potrebbe essere necessario annullare una chiamata asincrona dopo aver effettuato la chiamata.</span><span class="sxs-lookup"><span data-stu-id="ac7df-151">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="ac7df-152">Se è necessario annullare la chiamata, annullare la chiamata con lo stesso puntatore che ha originariamente effettuato la chiamata.</span><span class="sxs-lookup"><span data-stu-id="ac7df-152">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="ac7df-153">Nell'esempio di codice riportato di seguito viene descritto come annullare una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="ac7df-153">The following code example describes how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  <span data-ttu-id="ac7df-154">Rilasciare il conteggio dei riferimenti locale al termine dell'utilizzo della chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="ac7df-154">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="ac7df-155">Assicurarsi di rilasciare il puntatore *pStubSink* solo dopo aver verificato che la chiamata asincrona non deve essere annullata.</span><span class="sxs-lookup"><span data-stu-id="ac7df-155">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not must be canceled.</span></span> <span data-ttu-id="ac7df-156">Inoltre, non rilasciare *pStubSink* dopo che WMI rilascia il puntatore di sink *pSink* .</span><span class="sxs-lookup"><span data-stu-id="ac7df-156">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="ac7df-157">Il rilascio di *pStubSink* dopo *pSink* crea un conteggio dei riferimenti circolari in cui sia il sink che lo stub rimarranno sempre in memoria.</span><span class="sxs-lookup"><span data-stu-id="ac7df-157">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="ac7df-158">Al contrario, una posizione possibile per rilasciare il puntatore si trova nella chiamata [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , eseguita da WMI per segnalare che la chiamata asincrona originale è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ac7df-158">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

7.  <span data-ttu-id="ac7df-159">Al termine, annullare l'inizializzazione di COM con una chiamata a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="ac7df-159">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="ac7df-160">Nell'esempio di codice seguente viene illustrato come chiamare [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore *pUnsecApp* .</span><span class="sxs-lookup"><span data-stu-id="ac7df-160">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

<span data-ttu-id="ac7df-161">Per ulteriori informazioni sulla funzione e sui parametri [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , vedere la documentazione [com](../cossdk/component-services-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ac7df-161">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation.</span></span>

 

 
