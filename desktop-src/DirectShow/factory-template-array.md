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
# <a name="factory-template-array"></a><span data-ttu-id="c9450-103">Matrice modello Factory</span><span class="sxs-lookup"><span data-stu-id="c9450-103">Factory Template Array</span></span>

<span data-ttu-id="c9450-104">Il modello Factory contiene le variabili membro pubbliche seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9450-104">The factory template contains the following public member variables:</span></span>

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

<span data-ttu-id="c9450-105">I due puntatori a funzione, [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) e [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md), usano le definizioni dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9450-105">The two function pointers, [**m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) and [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md), use the following type definitions:</span></span>

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

<span data-ttu-id="c9450-106">Il primo è la funzione di creazione di istanze per il componente.</span><span class="sxs-lookup"><span data-stu-id="c9450-106">The first is the instantiation function for the component.</span></span> <span data-ttu-id="c9450-107">Il secondo è una funzione di inizializzazione facoltativa.</span><span class="sxs-lookup"><span data-stu-id="c9450-107">The second is an optional initialization function.</span></span> <span data-ttu-id="c9450-108">Se si specifica una funzione di inizializzazione, questa viene chiamata dall'interno della funzione del punto di ingresso della DLL.</span><span class="sxs-lookup"><span data-stu-id="c9450-108">If you provide an initialization function, it is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="c9450-109">La funzione del punto di ingresso della DLL viene discussa più avanti in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="c9450-109">(The DLL entry-point function is discussed later in this article.)</span></span>

<span data-ttu-id="c9450-110">Si supponga di creare una DLL contenente un componente denominato CMyComponent, che eredita da [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c9450-110">Suppose you are creating a DLL that contains a component named CMyComponent, which inherits from [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="c9450-111">Nella DLL è necessario specificare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9450-111">You must provide the following items in your DLL:</span></span>

-   <span data-ttu-id="c9450-112">Funzione di inizializzazione, un metodo pubblico che restituisce una nuova istanza di CMyComponent.</span><span class="sxs-lookup"><span data-stu-id="c9450-112">The initialization function, a public method that returns a new instance of CMyComponent.</span></span>
-   <span data-ttu-id="c9450-113">Una matrice globale di modelli Factory, denominati *g \_ Templates.*</span><span class="sxs-lookup"><span data-stu-id="c9450-113">A global array of factory templates, named *g\_Templates.*</span></span> <span data-ttu-id="c9450-114">Questa matrice contiene il modello factory per CMyComponent.</span><span class="sxs-lookup"><span data-stu-id="c9450-114">This array contains the factory template for CMyComponent.</span></span>
-   <span data-ttu-id="c9450-115">Una variabile globale denominata *g \_ cTemplates* che specifica la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="c9450-115">A global variable named *g\_cTemplates* that specifies the size of the array.</span></span>

<span data-ttu-id="c9450-116">Nell'esempio seguente viene illustrato come dichiarare questi elementi:</span><span class="sxs-lookup"><span data-stu-id="c9450-116">The following example shows how to declare these items:</span></span>


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



<span data-ttu-id="c9450-117">Il `CreateInstance` metodo chiama il costruttore della classe e restituisce un puntatore alla nuova istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="c9450-117">The `CreateInstance` method calls the class constructor and returns a pointer to the new class instance.</span></span> <span data-ttu-id="c9450-118">Il parametro *punk* è un puntatore all' [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="c9450-118">The parameter *pUnk* is a pointer to the aggregating [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="c9450-119">È possibile passare semplicemente questo parametro al costruttore della classe.</span><span class="sxs-lookup"><span data-stu-id="c9450-119">You can simply pass this parameter to the class constructor.</span></span> <span data-ttu-id="c9450-120">Il parametro *pHr* è un puntatore a un valore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c9450-120">The parameter *pHr* is a pointer to an HRESULT value.</span></span> <span data-ttu-id="c9450-121">Il costruttore della classe imposta questa classe su un valore appropriato, ma se il costruttore non riesce, impostare il valore su E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="c9450-121">The class constructor sets this to an appropriate value, but if the constructor fails, set the value to E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="c9450-122">La macro del [**nome**](name.md) genera una stringa nelle compilazioni di debug, ma viene risolta in **null** nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="c9450-122">The [**NAME**](name.md) macro generates a string in debug builds but resolves to **NULL** in retail builds.</span></span> <span data-ttu-id="c9450-123">Viene usato in questo esempio per fornire al componente un nome visualizzato nei log di debug, ma non occupa la memoria nella versione finale.</span><span class="sxs-lookup"><span data-stu-id="c9450-123">It is used in this example to give the component a name that appears in debug logs but does not occupy memory in the final version.</span></span>

<span data-ttu-id="c9450-124">Il `CreateInstance` metodo può avere qualsiasi nome, perché il class factory fa riferimento al puntatore a funzione nel modello Factory.</span><span class="sxs-lookup"><span data-stu-id="c9450-124">The `CreateInstance` method can have any name, because the class factory refers to the function pointer in the factory template.</span></span> <span data-ttu-id="c9450-125">Tuttavia, *i \_ modelli g* e *g \_ cTemplates* sono variabili globali che l'class factory prevede di trovare, quindi devono avere esattamente tali nomi.</span><span class="sxs-lookup"><span data-stu-id="c9450-125">However, *g\_Templates* and *g\_cTemplates* are global variables that the class factory expects to find, so they must have exactly those names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9450-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9450-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9450-127">Come creare una DLL di filtro DirectShow</span><span class="sxs-lookup"><span data-stu-id="c9450-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
