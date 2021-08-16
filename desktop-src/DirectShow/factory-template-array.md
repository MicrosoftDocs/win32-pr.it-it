---
description: Factory Template Array
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Factory Template Array
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1888a2a054473865c713d96cdfa5706c35229dc938f23513a95066176ab138c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401846"
---
# <a name="factory-template-array"></a>Factory Template Array

Il modello factory contiene le variabili membro pubbliche seguenti:

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

I due puntatori a funzione, [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) e [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md), usano le definizioni di tipo seguenti:

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

Il primo è la funzione di creazione di istanze per il componente. Il secondo è una funzione di inizializzazione facoltativa. Se si fornisce una funzione di inizializzazione, viene chiamata dall'interno della funzione del punto di ingresso della DLL. La funzione del punto di ingresso della DLL viene illustrata più avanti in questo articolo.

Si supponga di creare una DLL che contiene un componente denominato CMyComponent, che eredita da [**CUnknown.**](cunknown.md) È necessario specificare gli elementi seguenti nella DLL:

-   Funzione di inizializzazione, un metodo pubblico che restituisce una nuova istanza di CMyComponent.
-   Matrice globale di modelli factory, denominata *g \_ Templates.* Questa matrice contiene il modello factory per CMyComponent.
-   Variabile globale denominata *g \_ cTemplates* che specifica le dimensioni della matrice.

L'esempio seguente illustra come dichiarare questi elementi:


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



Il `CreateInstance` metodo chiama il costruttore della classe e restituisce un puntatore alla nuova istanza della classe. Il parametro *pUnk è* un puntatore all'oggetto [**IUnknown aggregato.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) È sufficiente passare questo parametro al costruttore della classe. Il parametro *pHr è* un puntatore a un valore HRESULT. Il costruttore della classe imposta questa proprietà su un valore appropriato, ma se il costruttore ha esito negativo, impostare il valore su E \_ OUTOFMEMORY.

La macro [**NAME**](name.md) genera una stringa nelle build di debug, ma viene risolta in **NULL** nelle build per la vendita al dettaglio. Viene usato in questo esempio per assegnare al componente un nome che viene visualizzato nei log di debug ma non occupa memoria nella versione finale.

Il `CreateInstance` metodo può avere qualsiasi nome, perché il class factory fa riferimento al puntatore a funzione nel modello factory. Tuttavia, *\_ i modelli g* e *g \_ cTemplates* sono variabili globali che l'class factory si aspetta di trovare, quindi devono avere esattamente questi nomi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una DLL DirectShow filtro](how-to-create-a-dll.md)
</dt> </dl>

 

 
