---
title: Registrare proprietà, eventi e pattern di controllo personalizzati
description: Prima di poter usare una proprietà personalizzata, un evento o un pattern di controllo, sia il provider che il client devono registrare la proprietà, l'evento o il pattern di controllo in fase di esecuzione.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Automazione interfaccia utente, proprietà personalizzate
- Automazione interfaccia utente, panoramica degli eventi
- Automazione interfaccia utente, Cenni preliminari sui pattern di controllo
- Automazione interfaccia utente, registrazione di proprietà personalizzate
- Automazione interfaccia utente, registrazione di eventi
- Automazione interfaccia utente, registrazione di pattern di controllo
- Proprietà personalizzate, registrazione
- eventi, registrazione
- pattern di controllo, registrazione
- registrazione, proprietà personalizzate
- registrazione, eventi
- registrazione, pattern di controllo
- pattern di controllo, personalizzati
- pattern di controllo, implementazione personalizzata
- implementazione di pattern di controllo personalizzati
- pattern di controllo personalizzati
- wrapper client
- gestori di modelli
- implementazione di gestori di modelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047184"
---
# <a name="register-custom-properties-events-and-control-patterns"></a>Registrare proprietà, eventi e pattern di controllo personalizzati

Prima di poter usare una proprietà personalizzata, un evento o un pattern di controllo, sia il provider che il client devono registrare la proprietà, l'evento o il pattern di controllo in fase di esecuzione. La registrazione è efficace a livello globale all'interno di un processo dell'applicazione e rimane effettiva fino alla chiusura del processo o all'ultima rilasciata all'interno del processo l'ultimo oggetto dell'elemento di automazione interfaccia utente Microsoft ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) o [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)).

Per la registrazione è necessario passare un GUID all'automazione interfaccia utente, insieme a informazioni dettagliate sulla proprietà personalizzata, sull'evento o sul pattern di controllo. Il tentativo di registrare lo stesso GUID una seconda volta con le stesse informazioni avrà esito positivo, ma il tentativo di registrare lo stesso GUID una seconda volta ma con informazioni diverse, ad esempio una proprietà personalizzata di un tipo diverso, avrà esito negativo. In futuro, se la specifica personalizzata viene accettata e integrata nel core di automazione interfaccia utente, l'automazione dell'interfaccia utente convaliderà le informazioni di registrazione personalizzate e utilizzerà il codice già registrato anziché l'implementazione del Framework "ufficiale", riducendo al minimo i problemi di compatibilità delle applicazioni. Non è possibile rimuovere proprietà, eventi o pattern di controllo che sono già registrati.

In questo argomento sono incluse le sezioni seguenti:

-   [Registrazione di proprietà ed eventi personalizzati](#registering-custom-properties-and-events)
-   [Implementazione di pattern di controllo personalizzati](#implementing-custom-control-patterns)
    -   [Il wrapper client e il gestore pattern](#the-client-wrapper-and-the-pattern-handler)
    -   [Implementazione del wrapper client](#implementing-the-client-wrapper)
    -   [Implementazione del gestore pattern](#implementing-the-pattern-handler)
    -   [Registrazione di un pattern di controllo personalizzato](#registering-a-custom-control-pattern)
    -   [Implementazione di esempio di un pattern di controllo personalizzato](#example-implementation-of-a-custom-control-pattern)
-   [Argomenti correlati](#related-topics)

## <a name="registering-custom-properties-and-events"></a>Registrazione di proprietà ed eventi personalizzati

La registrazione di un evento o di una proprietà personalizzata consente al provider e al client di ottenere un ID per la proprietà o l'evento, che può quindi essere passato a vari metodi API che accettano gli ID come parametri.

Per registrare una proprietà o un evento:

1.  Definire un GUID per la proprietà o l'evento personalizzato.
2.  Compilare una struttura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) o [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) con le informazioni sulla proprietà o sull'evento, inclusi il GUID e una stringa non localizzabile che contiene il nome della proprietà o dell'evento personalizzato. Per le proprietà personalizzate è inoltre necessario specificare il tipo di dati della proprietà, ad esempio se la proprietà include un Integer o una stringa. Il tipo di dati deve essere uno dei seguenti tipi specificati dall'enumerazione [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) . Non sono supportati altri tipi di dati per le proprietà personalizzate.
    -   **\_Bool UIAutomationType**
    -   **UIAutomationType \_ Double**
    -   **\_Elemento UIAutomationType**
    -   **\_Int UIAutomationType**
    -   **Punto di UIAutomationType \_**
    -   **\_Stringa UIAutomationType**
3.  Utilizzare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'oggetto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) e recuperare un puntatore all'interfaccia [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) dell'oggetto.
4.  Chiamare il metodo [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) o [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) e passare l'indirizzo della struttura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) o della struttura [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .

Il metodo [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) o [**REGISTEREVENT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) restituisce un ID di proprietà o un ID evento che un'applicazione può passare a qualsiasi metodo di automazione interfaccia utente che accetta tale identificatore come parametro. Ad esempio, è possibile passare un ID di proprietà registrato al metodo [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) o al metodo [**IUIAutomation:: CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .

Nell'esempio seguente viene illustrato come registrare una proprietà personalizzata.


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



Gli identificatori di proprietà e di evento recuperati dai metodi [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) e [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) sono validi solo nel contesto dell'applicazione che li recupera e solo per la durata della durata dell'applicazione. I metodi di registrazione possono restituire valori integer diversi per lo stesso GUID quando viene chiamato su istanze di runtime diverse della stessa applicazione.

Non esiste alcun metodo che annulla la registrazione di una proprietà o di un evento personalizzato. Viene invece annullata la registrazione in modo implicito quando viene rilasciato l'ultimo oggetto di automazione interfaccia utente.

> [!IMPORTANT]
> Se il codice è un client Microsoft Active Accessibility (MSAA), è necessario chiamare la funzione [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) quando si modifica il valore di una proprietà personalizzata.

 

## <a name="implementing-custom-control-patterns"></a>Implementazione di pattern di controllo personalizzati

Un pattern di controllo personalizzato non è incluso nell'API di automazione interfaccia utente, ma viene fornito da terze parti in fase di esecuzione. Gli sviluppatori di applicazioni client e provider devono collaborare per definire un pattern di controllo personalizzato, inclusi i metodi, le proprietà e gli eventi che il pattern di controllo supporterà. Dopo aver definito il pattern di controllo, sia il client che il provider devono implementare oggetti di supporto Component Object Model (COM), insieme al codice per registrare il pattern di controllo in fase di esecuzione. Un pattern di controllo personalizzato richiede l'implementazione di due oggetti COM: un wrapper client e un gestore di pattern.

> [!Note]  
> Gli esempi negli argomenti seguenti illustrano come implementare un pattern di controllo personalizzato che duplica la funzionalità del pattern di controllo [value](uiauto-implementingvalue.md) esistente. Questi esempi sono solo a scopo informativo. Un pattern di controllo personalizzato effettivo deve fornire funzionalità non disponibili nei modelli di controllo di automazione interfaccia utente standard.

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a>Il wrapper client e il gestore pattern

Il wrapper client implementa l'API usata dal client per recuperare le proprietà e chiamare i metodi esposti dal pattern di controllo personalizzato. L'API viene implementata come interfaccia COM che passa tutte le richieste di proprietà e le chiamate al metodo al core di automazione interfaccia utente, che quindi esegue il marshalling delle richieste e delle chiamate al provider.

Il codice che registra un pattern di controllo personalizzato deve fornire un class factory che l'automazione interfaccia utente possa usare per creare istanze dell'oggetto wrapper client. Quando un pattern di controllo personalizzato viene registrato correttamente, l'automazione interfaccia utente restituisce un puntatore a interfaccia [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) che viene usato dal client per l'invio delle richieste di proprietà e delle chiamate ai metodi al core di automazione interfaccia utente.

Sul lato del provider, il nucleo di automazione interfaccia utente acquisisce le richieste di proprietà e le chiamate ai metodi dal client e le passa all'oggetto del gestore di pattern. Il gestore pattern chiama quindi i metodi appropriati nell'interfaccia del provider per il pattern di controllo personalizzato.

Il codice che registra un pattern di controllo personalizzato crea l'oggetto del gestore pattern e, quando si registra il pattern di controllo, fornisce l'automazione dell'interfaccia utente con un puntatore all'interfaccia [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) dell'oggetto.

Il diagramma seguente illustra il flusso di una richiesta di proprietà client o di una chiamata al metodo dal wrapper client, tramite i componenti di base di automazione interfaccia utente al gestore pattern e quindi all'interfaccia del provider.

![diagramma che mostra il flusso dal wrapper client al gestore pattern e il provider](images/custompatternsupport.jpg)

Gli oggetti che implementano le interfacce del gestore del modello e del wrapper client devono essere a thread libero. Inoltre, il nucleo di automazione interfaccia utente deve essere in grado di chiamare direttamente gli oggetti senza alcun codice di marshalling intermedio.

### <a name="implementing-the-client-wrapper"></a>Implementazione del wrapper client

Il wrapper client è un oggetto che espone un'interfaccia IXxxPattern che il client usa per richiedere proprietà e chiamare metodi supportati dal pattern di controllo personalizzato. L'interfaccia è costituita da una coppia di metodi "getter" per ogni proprietà supportata (Get \_ CurrentXxx e Get \_ CachedXxx Method) e un metodo "Caller" per ogni metodo supportato. Quando viene creata un'istanza dell'oggetto, il costruttore dell'oggetto riceve un puntatore all'interfaccia [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , implementata dal core di automazione interfaccia utente. I metodi dell'interfaccia IXxxPattern usano i metodi [**IUIAutomationPatternInstance:: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) e [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) per inviare le richieste di proprietà e le chiamate al metodo al core di automazione interfaccia utente.

Nell'esempio seguente viene illustrato come implementare un oggetto wrapper client per un semplice pattern di controllo personalizzato che supporta una singola proprietà. Per un esempio più complesso, vedere [implementazione di esempio di un pattern di controllo personalizzato](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a>Implementazione del gestore pattern

Il gestore dei criteri è un oggetto che implementa l'interfaccia [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) . Questa interfaccia dispone di due metodi: [**IUIAutomationPatternHandler:: CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) e [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch). Il metodo **CreateClientWrapper** viene chiamato dal core di automazione interfaccia utente e riceve un puntatore all'interfaccia [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) . **CreateClientWrapper** risponde creando un'istanza dell'oggetto wrapper client e passando il puntatore all'interfaccia **IUIAutomationPatternInstance** al costruttore del wrapper client.

Il metodo [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) viene usato dal core di automazione interfaccia utente per passare le richieste di proprietà e le chiamate ai metodi all'interfaccia del provider per il pattern di controllo personalizzato. I parametri includono un puntatore all'interfaccia del provider, l'indice in base zero del metodo di richiamo della proprietà o del metodo chiamato e una matrice di strutture [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) che contengono i parametri da passare al provider. Il gestore di pattern risponde controllando il parametro index per determinare il metodo del provider da chiamare e quindi chiama l'interfaccia del provider, passando i parametri contenuti nelle strutture **UIAutomationParameter** .

Viene creata un'istanza dell'oggetto pattern handler dallo stesso codice che registra il pattern di controllo personalizzato, prima che il pattern di controllo venga registrato. Il codice deve passare il puntatore all'interfaccia [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) dell'oggetto gestore pattern al core di automazione interfaccia utente al momento della registrazione.

Nell'esempio seguente viene illustrato come implementare un oggetto gestore di pattern per un semplice pattern di controllo personalizzato che supporta una singola proprietà. Per un esempio più complesso, vedere [implementazione di esempio di un pattern di controllo personalizzato](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a>Registrazione di un pattern di controllo personalizzato

Prima di poter essere usato, un pattern di controllo personalizzato deve essere registrato sia dal provider che dal client. La registrazione fornisce al core di automazione interfaccia utente informazioni dettagliate sul pattern di controllo e fornisce il provider o il client con l'ID del pattern di controllo e gli ID per le proprietà e gli eventi supportati dal pattern di controllo. Sul lato del provider, il pattern di controllo personalizzato deve essere registrato prima che il controllo associato gestisca il messaggio [**WM \_ GetObject**](wm-getobject.md) o nello stesso momento.

Quando si registra un pattern di controllo personalizzato, il provider o il client fornisce le informazioni seguenti:

-   GUID del pattern di controllo personalizzato.
-   Stringa non localizzabile che contiene il nome del pattern di controllo personalizzato.
-   GUID dell'interfaccia del provider che supporta il pattern di controllo personalizzato.
-   GUID dell'interfaccia client che supporta il pattern di controllo personalizzato.
-   Matrice di strutture [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) che descrivono le proprietà supportate dal pattern di controllo personalizzato. Per ogni proprietà è necessario specificare il GUID, il nome della proprietà e il tipo di dati.
-   Matrice di strutture [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) che descrivono i metodi supportati dal pattern di controllo personalizzato. Per ogni metodo, la struttura include le informazioni seguenti: il nome del metodo, il conteggio dei parametri, un elenco di tipi di dati dei parametri e un elenco dei nomi di parametro.
-   Matrice di strutture [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) che descrivono gli eventi generati dal pattern di controllo personalizzato. Per ogni evento, è necessario specificare il GUID e il nome dell'evento.
-   Indirizzo dell'interfaccia [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) dell'oggetto gestore di pattern che rende disponibile il pattern di controllo personalizzato ai client.

Per registrare il pattern di controllo personalizzato, il codice client o il provider deve eseguire i passaggi seguenti:

1.  Riempire una struttura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) con le informazioni precedenti.
2.  Utilizzare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'oggetto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) e recuperare un puntatore all'interfaccia [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) dell'oggetto.
3.  Chiamare il metodo [**IUIAutomationRegistrar:: RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) , passando l'indirizzo della struttura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) .

Il metodo [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) restituisce un ID pattern di controllo, insieme a un elenco di ID di proprietà e ID evento. Un'applicazione può passare questi ID a qualsiasi metodo di automazione interfaccia utente che accetta tale identificatore come parametro. Ad esempio, è possibile passare un ID modello registrato al metodo [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) per recuperare un puntatore all'interfaccia del provider per il pattern di controllo.

Non esiste alcun metodo che annulla la registrazione di un pattern di controllo personalizzato. Viene invece annullata la registrazione in modo implicito quando viene rilasciato l'ultimo oggetto di automazione interfaccia utente.

Per un esempio in cui viene illustrato come registrare un pattern di controllo personalizzato, vedere la sezione seguente.

### <a name="example-implementation-of-a-custom-control-pattern"></a>Implementazione di esempio di un pattern di controllo personalizzato

Questa sezione contiene codice di esempio che illustra come implementare gli oggetti wrapper client e gestore pattern per un pattern di controllo personalizzato. Nell'esempio viene implementato un pattern di controllo personalizzato basato sul pattern di controllo [value](uiauto-implementingvalue.md) .


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Progettazione di proprietà, eventi e pattern di controllo personalizzati](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 