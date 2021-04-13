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
# <a name="writing-a-custom-surrogate"></a>Scrittura di un surrogato personalizzato

Sebbene il surrogato fornito dal sistema sia più adatto per la maggior parte delle situazioni, in alcuni casi è opportuno scrivere un surrogato personalizzato. Ecco alcuni esempi:

-   Un surrogato personalizzato potrebbe fornire alcune ottimizzazioni o semantiche non presenti nel surrogato di sistema.
-   Se una DLL in-Process contiene codice che dipende dal fatto che si trovi nello stesso processo del client, il server DLL non funzionerà correttamente se è in esecuzione nel surrogato di sistema. Un surrogato personalizzato può essere adattato a una DLL specifica per gestire questo problema.
-   Il surrogato di sistema supporta un modello di threading misto, in modo che sia possibile caricare le dll del modello libero e dell'Apartment. Un surrogato personalizzato potrebbe essere personalizzato per caricare solo le DLL di Apartment per motivi di efficienza o per accettare un argomento della riga di comando per il tipo di DLL che è autorizzato a caricare.
-   Un surrogato personalizzato potrebbe richiedere parametri della riga di comando aggiuntivi che non sono conformi al surrogato di sistema.
-   Il surrogato di sistema chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e indica di usare le impostazioni di sicurezza esistenti presenti nella chiave [AppID](appid-key.md) nel registro di sistema. Un surrogato personalizzato può utilizzare un altro contesto di sicurezza.
-   Le interfacce che non sono utilizzabili in remoto (ad esempio quelle per ocx recenti) non funzioneranno con il surrogato di sistema. Un surrogato personalizzato può eseguire il wrapping delle interfacce della DLL con la propria implementazione e usare DLL proxy/stub con una definizione IDL utilizzabile in remoto che consentirebbe l'interfaccia in modalità remota.

Il thread surrogato principale deve in genere eseguire i passaggi di configurazione seguenti:

1.  Chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare il thread e impostare il modello di Threading.
2.  Se si desidera che i server DLL che devono essere eseguiti nel server siano in grado di utilizzare le impostazioni di sicurezza nella chiave del registro di sistema **AppID** , chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la \_ funzionalità AppID di EOAC. In caso contrario, verranno usate le impostazioni di sicurezza legacy.
3.  Chiamare [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) per registrare l'interfaccia surrogata in com.
4.  Chiamare [**ISurrogate:: LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) per il CLSID richiesto.
5.  Inserire il thread principale in un ciclo per chiamare periodicamente [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) .
6.  Quando COM chiama [**ISurrogate:: FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revocare tutte le class factory ed uscire.

Un processo surrogato deve implementare l'interfaccia [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) . Questa interfaccia deve essere registrata quando viene avviato un nuovo surrogato e dopo la chiamata a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Come indicato nei passaggi precedenti, l'interfaccia **ISurrogate** dispone di due metodi che com chiama: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)per caricare dinamicamente i nuovi server DLL in surrogati esistenti; e [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), per liberare il surrogato.

L'implementazione di [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), che chiama com con una richiesta di caricamento, deve prima creare un oggetto class factory che supporti [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)e quindi chiamare [**COREGISTERCLASSOBJECT**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) per registrare l'oggetto come class factory per il CLSID richiesto.

Il class factory registrato dal processo surrogato non è il class factory effettivo implementato dal server DLL, ma è un class factory generico implementato dal processo surrogato che supporta [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). Poiché si tratta del class factory del surrogato, anziché di quello del server DLL registrato, il class factory del surrogato dovrà utilizzare il class factory reale per creare un'istanza dell'oggetto per il CLSID registrato. Il surrogato di [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) dovrebbe avere un aspetto simile all'esempio seguente:


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



Il class factory del surrogato deve supportare anche [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , perché una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) può richiedere qualsiasi interfaccia dal class factory registrato, non solo [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Poiché il class factory generico supporta solo [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e **IClassFactory**, le richieste di altre interfacce devono essere indirizzate all'oggetto reale. Deve quindi essere presente un metodo [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) che dovrebbe essere simile al seguente:


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



Il surrogato che ospita un server DLL deve pubblicare gli oggetti classe del server DLL con una chiamata a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject). Tutte le class factory per i surrogati DLL devono essere registrate come \_ surrogato di REGCLS. REGCLS \_ SINGLUSE e REGCLS \_ MULTIPLEUSE non devono essere utilizzati per i server DLL caricati in surrogati.

Seguendo queste linee guida per la creazione di un processo surrogato quando è necessario eseguire questa operazione, è necessario garantire un comportamento appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Surrogati DLL](dll-surrogates.md)
</dt> </dl>

 

 