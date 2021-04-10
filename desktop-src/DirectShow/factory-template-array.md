---
description: Matrice modello Factory
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Matrice modello Factory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125598"
---
# <a name="factory-template-array"></a>Matrice modello Factory

Il modello Factory contiene le variabili membro pubbliche seguenti:

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

I due puntatori a funzione, [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) e [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md), usano le definizioni dei tipi seguenti:

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

Il primo è la funzione di creazione di istanze per il componente. Il secondo è una funzione di inizializzazione facoltativa. Se si specifica una funzione di inizializzazione, questa viene chiamata dall'interno della funzione del punto di ingresso della DLL. La funzione del punto di ingresso della DLL viene discussa più avanti in questo articolo.

Si supponga di creare una DLL contenente un componente denominato CMyComponent, che eredita da [**CUnknown**](cunknown.md). Nella DLL è necessario specificare gli elementi seguenti:

-   Funzione di inizializzazione, un metodo pubblico che restituisce una nuova istanza di CMyComponent.
-   Una matrice globale di modelli Factory, denominati *g \_ Templates.* Questa matrice contiene il modello factory per CMyComponent.
-   Una variabile globale denominata *g \_ cTemplates* che specifica la dimensione della matrice.

Nell'esempio seguente viene illustrato come dichiarare questi elementi:


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



Il `CreateInstance` metodo chiama il costruttore della classe e restituisce un puntatore alla nuova istanza della classe. Il parametro *punk* è un puntatore all' [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)di aggregazione. È possibile passare semplicemente questo parametro al costruttore della classe. Il parametro *pHr* è un puntatore a un valore HRESULT. Il costruttore della classe imposta questa classe su un valore appropriato, ma se il costruttore non riesce, impostare il valore su E \_ OutOfMemory.

La macro del [**nome**](name.md) genera una stringa nelle compilazioni di debug, ma viene risolta in **null** nelle compilazioni al dettaglio. Viene usato in questo esempio per fornire al componente un nome visualizzato nei log di debug, ma non occupa la memoria nella versione finale.

Il `CreateInstance` metodo può avere qualsiasi nome, perché il class factory fa riferimento al puntatore a funzione nel modello Factory. Tuttavia, *i \_ modelli g* e *g \_ cTemplates* sono variabili globali che l'class factory prevede di trovare, quindi devono avere esattamente tali nomi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una DLL di filtro DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
