---
title: Scrittura di un surrogato personalizzato
description: Scrittura di un surrogato personalizzato
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c6098f4d0e9d99be86956bacce413e7e8a4b864a91212d6c2a1a257d9c1db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047659"
---
# <a name="writing-a-custom-surrogate"></a>Scrittura di un surrogato personalizzato

Anche se il surrogato fornito dal sistema sarà più che adeguato per la maggior parte delle situazioni, in alcuni casi può essere utile scrivere un surrogato personalizzato. Ecco alcuni esempi:

-   Un surrogato personalizzato può fornire alcune ottimizzazioni o semantiche non presenti nel surrogato di sistema.
-   Se una DLL in-process contiene codice che dipende dall'essere nello stesso processo del client, il server DLL non funzionerà correttamente se è in esecuzione nel surrogato di sistema. Un surrogato personalizzato può essere adattato a una DLL specifica per gestire questo problema.
-   Il surrogato di sistema supporta un modello di threading misto in modo che possa caricare dll del modello sia di tipo free che apartment. Un surrogato personalizzato può essere personalizzato per caricare solo DLL di apartment per motivi di efficienza o per accettare un argomento della riga di comando per il tipo di DLL che può caricare.
-   Un surrogato personalizzato potrebbe richiedere parametri aggiuntivi della riga di comando non forniti dal surrogato di sistema.
-   Il surrogato di sistema [**chiama CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e indica di usare le impostazioni di sicurezza esistenti presenti nella chiave [AppID](appid-key.md) del Registro di sistema. Un surrogato personalizzato potrebbe usare un altro contesto di sicurezza.
-   Le interfacce che non sono utilizzabili in remoto (ad esempio quelle per OCX recenti) non funzionano con il surrogato di sistema. Un surrogato personalizzato potrebbe eseguire il wrapping delle interfacce della DLL con la propria implementazione e usare DLL proxy/stub con una definizione IDL remotabile che consentirebbe la connessione remota dell'interfaccia.

Il thread surrogato principale deve in genere eseguire i passaggi di configurazione seguenti:

1.  Chiamare [**CoInitializeEx per**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) inizializzare il thread e impostare il modello di threading.
2.  Se si vuole che i server DLL che devono essere eseguiti nel server siano in grado di usare le impostazioni di sicurezza nella chiave del Registro di sistema **AppID,** chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la funzionalità \_ APPID EOAC. In caso contrario, verranno usate le impostazioni di sicurezza legacy.
3.  Chiamare [**CoRegisterSurrogate per**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) registrare l'interfaccia surrogata in COM.
4.  Chiamare [**ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) per il CLSID richiesto.
5.  Inserire il thread principale in un ciclo per [**chiamare periodicamente CoFreeUnusedLibraries.**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries)
6.  Quando COM chiama [**ISurrogate::FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revocare tutte le class factory e uscire.

Un processo surrogato deve implementare [**l'interfaccia ISurrogate.**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) Questa interfaccia deve essere registrata all'avvio di un nuovo surrogato e dopo la [**chiamata a CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) Come indicato nei passaggi precedenti, l'interfaccia **ISurrogate** ha due metodi che COM chiama: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), per caricare dinamicamente i nuovi server DLL nei surrogati esistenti. e [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), per liberare il surrogato.

L'implementazione di [**LoadDllServer,**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)che COM chiama con una richiesta di caricamento, deve prima creare un oggetto class factory che supporta [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)e [**IMarshal,**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)quindi chiamare [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) per registrare l'oggetto come class factory per il CLSID richiesto.

Il class factory registrato dal processo surrogato non è il class factory effettivo implementato dal server DLL, ma è un class factory generico implementato dal processo surrogato che supporta [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e [**IMarshal.**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) Poiché è il class factory del surrogato, anziché quello del server DLL registrato, il class factory del surrogato dovrà usare il class factory reale per creare un'istanza dell'oggetto per il CLSID registrato. L'oggetto [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) del surrogato dovrebbe essere simile all'esempio seguente:


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



L'interfaccia class factory surrogato deve supportare [**anche IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) perché una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) può richiedere qualsiasi interfaccia dal class factory registrato, non solo [**da IClassFactory.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) Inoltre, poiché il class factory generico supporta solo [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e **IClassFactory,** le richieste per altre interfacce devono essere indirizzate all'oggetto reale. Di conseguenza, deve essere presente [**un metodo MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) che dovrebbe essere simile al seguente:


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



Il surrogato che ospita un server DLL deve pubblicare gli oggetti classe del server DLL con una chiamata a [**CoRegisterClassObject.**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) Tutte le class factory per i surrogati DLL devono essere registrate come \_ REGCLS SURROGATE. REGCLS SINGLUSE e REGCLS MULTIPLEUSE non devono essere usati per \_ i server DLL caricati in \_ surrogati.

Seguendo queste linee guida per la creazione di un processo surrogato quando è necessario, è necessario garantire il comportamento corretto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Surrogati DLL](dll-surrogates.md)
</dt> </dl>

 

 