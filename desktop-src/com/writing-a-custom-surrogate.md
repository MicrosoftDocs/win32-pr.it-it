---
title: Scrittura di un surrogato personalizzato
description: Scrittura di un surrogato personalizzato
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339311"
---
# <a name="writing-a-custom-surrogate"></a><span data-ttu-id="a22f7-103">Scrittura di un surrogato personalizzato</span><span class="sxs-lookup"><span data-stu-id="a22f7-103">Writing a Custom Surrogate</span></span>

<span data-ttu-id="a22f7-104">Sebbene il surrogato fornito dal sistema sia più adatto per la maggior parte delle situazioni, in alcuni casi è opportuno scrivere un surrogato personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a22f7-104">While the system-supplied surrogate will be more than adequate for most situations, there are some cases where writing a custom surrogate could be worthwhile.</span></span> <span data-ttu-id="a22f7-105">Ecco alcuni esempi:</span><span class="sxs-lookup"><span data-stu-id="a22f7-105">Following are some examples:</span></span>

-   <span data-ttu-id="a22f7-106">Un surrogato personalizzato potrebbe fornire alcune ottimizzazioni o semantiche non presenti nel surrogato di sistema.</span><span class="sxs-lookup"><span data-stu-id="a22f7-106">A custom surrogate could provide some optimizations or semantics not present in the system surrogate.</span></span>
-   <span data-ttu-id="a22f7-107">Se una DLL in-Process contiene codice che dipende dal fatto che si trovi nello stesso processo del client, il server DLL non funzionerà correttamente se è in esecuzione nel surrogato di sistema.</span><span class="sxs-lookup"><span data-stu-id="a22f7-107">If an in-process DLL contains code that depends on being in the same process as the client, the DLL server will not function correctly if it is running in the system surrogate.</span></span> <span data-ttu-id="a22f7-108">Un surrogato personalizzato può essere adattato a una DLL specifica per gestire questo problema.</span><span class="sxs-lookup"><span data-stu-id="a22f7-108">A custom surrogate could be tailored to a specific DLL to deal with this.</span></span>
-   <span data-ttu-id="a22f7-109">Il surrogato di sistema supporta un modello di threading misto, in modo che sia possibile caricare le dll del modello libero e dell'Apartment.</span><span class="sxs-lookup"><span data-stu-id="a22f7-109">The system surrogate supports a mixed-threading model so that it can load both free and apartment model DLLs.</span></span> <span data-ttu-id="a22f7-110">Un surrogato personalizzato potrebbe essere personalizzato per caricare solo le DLL di Apartment per motivi di efficienza o per accettare un argomento della riga di comando per il tipo di DLL che è autorizzato a caricare.</span><span class="sxs-lookup"><span data-stu-id="a22f7-110">A custom surrogate might be tailored to load only apartment DLLs for reasons of efficiency or to accept a command-line argument for the type of DLL it is allowed to load.</span></span>
-   <span data-ttu-id="a22f7-111">Un surrogato personalizzato potrebbe richiedere parametri della riga di comando aggiuntivi che non sono conformi al surrogato di sistema.</span><span class="sxs-lookup"><span data-stu-id="a22f7-111">A custom surrogate could take extra command-line parameters that the system surrogate does not.</span></span>
-   <span data-ttu-id="a22f7-112">Il surrogato di sistema chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e indica di usare le impostazioni di sicurezza esistenti presenti nella chiave [AppID](appid-key.md) nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a22f7-112">The system surrogate calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and tells it to use any existing security settings found under the [AppID](appid-key.md) key in the registry.</span></span> <span data-ttu-id="a22f7-113">Un surrogato personalizzato può utilizzare un altro contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a22f7-113">A custom surrogate could use another security context.</span></span>
-   <span data-ttu-id="a22f7-114">Le interfacce che non sono utilizzabili in remoto (ad esempio quelle per ocx recenti) non funzioneranno con il surrogato di sistema.</span><span class="sxs-lookup"><span data-stu-id="a22f7-114">Interfaces that aren't remotable (such as those for recent OCXs) will not work with the system surrogate.</span></span> <span data-ttu-id="a22f7-115">Un surrogato personalizzato può eseguire il wrapping delle interfacce della DLL con la propria implementazione e usare DLL proxy/stub con una definizione IDL utilizzabile in remoto che consentirebbe l'interfaccia in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="a22f7-115">A custom surrogate could wrap the DLL's interfaces with its own implementation and use proxy/stub DLLs with a remotable IDL definition that would allow the interface to be remoted.</span></span>

<span data-ttu-id="a22f7-116">Il thread surrogato principale deve in genere eseguire i passaggi di configurazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="a22f7-116">The main surrogate thread should typically perform the following setup steps:</span></span>

1.  <span data-ttu-id="a22f7-117">Chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare il thread e impostare il modello di Threading.</span><span class="sxs-lookup"><span data-stu-id="a22f7-117">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the thread and set the threading model.</span></span>
2.  <span data-ttu-id="a22f7-118">Se si desidera che i server DLL che devono essere eseguiti nel server siano in grado di utilizzare le impostazioni di sicurezza nella chiave del registro di sistema **AppID** , chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la \_ funzionalità AppID di EOAC.</span><span class="sxs-lookup"><span data-stu-id="a22f7-118">If you want the DLL servers that are to run in the server to be able to use the security settings in the **AppID** registry key, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) with the EOAC\_APPID capability.</span></span> <span data-ttu-id="a22f7-119">In caso contrario, verranno usate le impostazioni di sicurezza legacy.</span><span class="sxs-lookup"><span data-stu-id="a22f7-119">Otherwise, legacy security settings will be used.</span></span>
3.  <span data-ttu-id="a22f7-120">Chiamare [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) per registrare l'interfaccia surrogata in com.</span><span class="sxs-lookup"><span data-stu-id="a22f7-120">Call [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) to register the surrogate interface to COM.</span></span>
4.  <span data-ttu-id="a22f7-121">Chiamare [**ISurrogate:: LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) per il CLSID richiesto.</span><span class="sxs-lookup"><span data-stu-id="a22f7-121">Call [**ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) for the requested CLSID.</span></span>
5.  <span data-ttu-id="a22f7-122">Inserire il thread principale in un ciclo per chiamare periodicamente [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) .</span><span class="sxs-lookup"><span data-stu-id="a22f7-122">Put main thread in a loop to call [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodically.</span></span>
6.  <span data-ttu-id="a22f7-123">Quando COM chiama [**ISurrogate:: FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revocare tutte le class factory ed uscire.</span><span class="sxs-lookup"><span data-stu-id="a22f7-123">When COM calls [**ISurrogate::FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revoke all class factories and exit.</span></span>

<span data-ttu-id="a22f7-124">Un processo surrogato deve implementare l'interfaccia [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) .</span><span class="sxs-lookup"><span data-stu-id="a22f7-124">A surrogate process must implement the [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) interface.</span></span> <span data-ttu-id="a22f7-125">Questa interfaccia deve essere registrata quando viene avviato un nuovo surrogato e dopo la chiamata a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="a22f7-125">This interface should be registered when a new surrogate is started and after calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span> <span data-ttu-id="a22f7-126">Come indicato nei passaggi precedenti, l'interfaccia **ISurrogate** dispone di due metodi che com chiama: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)per caricare dinamicamente i nuovi server DLL in surrogati esistenti; e [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), per liberare il surrogato.</span><span class="sxs-lookup"><span data-stu-id="a22f7-126">As indicated in the preceding steps, the **ISurrogate** interface has two methods that COM calls: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), to dynamically load new DLL servers into existing surrogates; and [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), to free the surrogate.</span></span>

<span data-ttu-id="a22f7-127">L'implementazione di [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), che chiama com con una richiesta di caricamento, deve prima creare un oggetto class factory che supporti [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)e quindi chiamare [**COREGISTERCLASSOBJECT**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) per registrare l'oggetto come class factory per il CLSID richiesto.</span><span class="sxs-lookup"><span data-stu-id="a22f7-127">The implementation of [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), which COM calls with a load request, must first create a class factory object that supports [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), and then call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) to register the object as the class factory for the requested CLSID.</span></span>

<span data-ttu-id="a22f7-128">Il class factory registrato dal processo surrogato non è il class factory effettivo implementato dal server DLL, ma è un class factory generico implementato dal processo surrogato che supporta [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span><span class="sxs-lookup"><span data-stu-id="a22f7-128">The class factory registered by the surrogate process is not the actual class factory implemented by the DLL server but is a generic class factory implemented by the surrogate process that supports [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span></span> <span data-ttu-id="a22f7-129">Poiché si tratta del class factory del surrogato, anziché di quello del server DLL registrato, il class factory del surrogato dovrà utilizzare il class factory reale per creare un'istanza dell'oggetto per il CLSID registrato.</span><span class="sxs-lookup"><span data-stu-id="a22f7-129">Because it is the surrogate's class factory, rather than that of the DLL server that is being registered, the surrogate's class factory will need to use the real class factory to create an instance of the object for the registered CLSID.</span></span> <span data-ttu-id="a22f7-130">Il surrogato di [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) dovrebbe avere un aspetto simile all'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="a22f7-130">The surrogate's [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) should look something like the following example:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::CreateInstance(
  IUnknown* pUnkOuter, 
  REFIID iid, 
  void** ppv)
{
    void* pcf;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, IID_IClassFactory, &pcf);
    if ( FAILED(hr) )
        return hr;
    hr = ((IClassFactory*)pcf)->CreateInstance(pUnkOuter, iid, ppv);
    ((IClassFactory*)pcf)->Release();
    return hr;
}
 
```



<span data-ttu-id="a22f7-131">Il class factory del surrogato deve supportare anche [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , perché una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) può richiedere qualsiasi interfaccia dal class factory registrato, non solo [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="a22f7-131">The surrogate's class factory must also support [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) because a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) can request any interface from the registered class factory, not just [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="a22f7-132">Poiché il class factory generico supporta solo [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e **IClassFactory**, le richieste di altre interfacce devono essere indirizzate all'oggetto reale.</span><span class="sxs-lookup"><span data-stu-id="a22f7-132">Further, since the generic class factory supports only [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and **IClassFactory**, requests for other interfaces must be directed to the real object.</span></span> <span data-ttu-id="a22f7-133">Deve quindi essere presente un metodo [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) che dovrebbe essere simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="a22f7-133">Thus, there should be a [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) method which should be similar to the following:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::MarshalInterface(
  IStream *pStm,  
  REFIID riid, void *pv, 
  WORD dwDestContext, 
  void *pvDestContext, 
  DWORD mshlflags )
{   
    void * pCF = NULL;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, riid, &pCF);
    if ( FAILED(hr) )
        return hr;   
    hr = CoMarshalInterface(pStm, riid, (IUnknown*)pCF, dwDestContext, pvDestContext,  mshlflags);
    ((IUnknown*)pCF)->Release();
    return S_OK;
 
```



<span data-ttu-id="a22f7-134">Il surrogato che ospita un server DLL deve pubblicare gli oggetti classe del server DLL con una chiamata a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span><span class="sxs-lookup"><span data-stu-id="a22f7-134">The surrogate that houses a DLL server must publish the DLL server's class object(s) with a call to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span></span> <span data-ttu-id="a22f7-135">Tutte le class factory per i surrogati DLL devono essere registrate come \_ surrogato di REGCLS.</span><span class="sxs-lookup"><span data-stu-id="a22f7-135">All class factories for DLL surrogates should be registered as REGCLS\_SURROGATE.</span></span> <span data-ttu-id="a22f7-136">REGCLS \_ SINGLUSE e REGCLS \_ MULTIPLEUSE non devono essere utilizzati per i server DLL caricati in surrogati.</span><span class="sxs-lookup"><span data-stu-id="a22f7-136">REGCLS\_SINGLUSE and REGCLS\_MULTIPLEUSE should not be used for DLL servers loaded into surrogates.</span></span>

<span data-ttu-id="a22f7-137">Seguendo queste linee guida per la creazione di un processo surrogato quando è necessario eseguire questa operazione, è necessario garantire un comportamento appropriato.</span><span class="sxs-lookup"><span data-stu-id="a22f7-137">Following these guidelines for creating a surrogate process when it is necessary to do so should ensure proper behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a22f7-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a22f7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a22f7-139">Surrogati DLL</span><span class="sxs-lookup"><span data-stu-id="a22f7-139">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 