---
description: Programmazione di DirectX con COM.
title: Programmazione di DirectX con COM
ms.topic: article
ms.date: 01/29/2019
ms.openlocfilehash: 67fc7a35f42439e1a9eeef1b2895d88dc0dbf5d4
ms.sourcegitcommit: f712e5fed19d6afe2762a77ffcdf8b5977f85901
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "103968789"
---
# <a name="programming-directx-with-com"></a>Programmazione di DirectX con COM

Microsoft Component Object Model (COM) è un modello di programmazione orientato a oggetti usato da diverse tecnologie, inclusa la maggior parte della superficie dell'API DirectX. Per questo motivo, quando si programma DirectX è necessario che l'utente, come sviluppatore di DirectX, usi inevitabilmente COM.

> [!NOTE]
> L'argomento utilizzo di [componenti com con c++/WinRT](/windows/uwp/cpp-and-winrt-apis/consume-com) illustra come utilizzare le API DirectX (e qualsiasi API com) con [c++/WinRT](/windows/uwp/cpp-and-winrt-apis/). Questa è la tecnologia più comoda e consigliata da usare.

In alternativa, è possibile usare COM non elaborato e questo è il significato di questo argomento. Sarà necessaria una conoscenza di base dei principi e delle tecniche di programmazione necessari per l'utilizzo delle API COM. Sebbene COM abbia la reputazione di essere difficile e complesso, la programmazione COM richiesta dalla maggior parte delle applicazioni DirectX è molto semplice. In parte, questo è dovuto al fatto che verranno utilizzati gli oggetti COM forniti da DirectX. Non è necessario creare oggetti COM, in genere in cui si verifica la complessità.

## <a name="com-component-overview"></a>Panoramica sul componente COM

Un oggetto COM è essenzialmente un componente incapsulato di funzionalità che può essere utilizzato dalle applicazioni per eseguire una o più attività. Per la distribuzione, uno o più componenti COM vengono assemblati in un file binario denominato server COM; più spesso che non come una DLL.

Una DLL tradizionale Esporta funzioni gratuite. Un server COM può eseguire la stessa operazione. Tuttavia, i componenti COM all'interno del server COM espongono interfacce COM e metodi membro che appartengono a tali interfacce. L'applicazione crea istanze di componenti COM, recupera le interfacce da esse e chiama i metodi su tali interfacce per trarre vantaggio dalle funzionalità implementate nei componenti COM.

In pratica, questo comportamento è simile alla chiamata di metodi su un normale oggetto C++. Esistono tuttavia alcune differenze.

- Un oggetto COM impone un incapsulamento più restrittivo rispetto a quello di un oggetto C++. Non è possibile creare semplicemente l'oggetto e quindi chiamare un metodo pubblico. Al contrario, i metodi pubblici di un componente COM vengono raggruppati in una o più interfacce COM. Per chiamare un metodo, è necessario creare l'oggetto e recuperare dall'oggetto l'interfaccia che implementa il metodo. Un'interfaccia implementa in genere un set correlato di metodi che forniscono l'accesso a una particolare funzionalità dell'oggetto. Ad esempio, l'interfaccia [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) rappresenta una scheda grafica virtuale e contiene metodi che consentono di creare risorse, ad esempio, e molte altre attività relative agli adapter.
- Un oggetto COM non viene creato allo stesso modo di un oggetto C++. Esistono diversi modi per creare un oggetto COM, ma tutti coinvolgono tecniche specifiche di COM. L'API DirectX include un'ampia gamma di funzioni di supporto e metodi che semplificano la creazione della maggior parte degli oggetti DirectX COM.
- È necessario utilizzare tecniche specifiche di COM per controllare la durata di un oggetto COM.
- Non è necessario caricare in modo esplicito il server COM (in genere una DLL). Non è inoltre possibile collegarsi a una libreria statica per poter utilizzare un componente COM. Ogni componente COM dispone di un identificatore registrato univoco (un identificatore univoco globale o GUID) usato dall'applicazione per identificare l'oggetto COM. L'applicazione identifica il componente e il runtime COM carica automaticamente la DLL del server COM corretta.
- COM è una specifica binaria. Gli oggetti COM possono essere scritti e accessibili da un'ampia gamma di linguaggi. Non è necessario conoscere il codice sorgente dell'oggetto. Ad esempio, Visual Basic applicazioni utilizzano periodicamente oggetti COM scritti in C++.

## <a name="component-object-and-interface"></a>Componente, oggetto e interfaccia

È importante comprendere la differenza tra i componenti, gli oggetti e le interfacce. Nell'utilizzo occasionale, è possibile che si verifichi un componente o un oggetto a cui fa riferimento il nome dell'interfaccia principale. Ma i termini non sono intercambiabili. Un componente può implementare un numero qualsiasi di interfacce. e un oggetto è un'istanza di un componente. Ad esempio, mentre tutti i componenti devono implementare l' [**interfaccia IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), in genere implementano almeno un'interfaccia aggiuntiva e potrebbero implementare molti.

Per usare un particolare metodo di interfaccia, è necessario non solo creare un'istanza di un oggetto, ma è necessario ottenere anche l'interfaccia corretta.

Inoltre, più di un componente può implementare la stessa interfaccia. Un'interfaccia è un gruppo di metodi che eseguono un set di operazioni correlate logicamente. La definizione dell'interfaccia specifica solo la sintassi dei metodi e le relative funzionalità generali. Qualsiasi componente COM che deve supportare un determinato set di operazioni può eseguire questa operazione implementando un'interfaccia appropriata. Alcune interfacce sono altamente specializzate e vengono implementate solo da un singolo componente; altre sono utili in varie circostanze e sono implementate da molti componenti.

Se un componente implementa un'interfaccia, deve supportare tutti i metodi nella definizione dell'interfaccia. In altre parole, è necessario essere in grado di chiamare qualsiasi metodo e avere la certezza che esista. Tuttavia, i dettagli della modalità di implementazione di un particolare metodo possono variare da un componente a un altro. Ad esempio, diversi componenti possono utilizzare algoritmi diversi per ottenere il risultato finale. Non è inoltre garantito che un metodo sarà supportato in modo non semplice. In alcuni casi, un componente implementa un'interfaccia di uso comune, ma deve supportare solo un subset dei metodi. Sarà comunque possibile chiamare correttamente i metodi rimanenti, ma restituiranno un [**HRESULT**](#hresult-values) (ovvero un tipo com standard che rappresenta un codice risultato) che contiene il valore **E_NOTIMPL**. È necessario fare riferimento alla relativa documentazione per vedere come un'interfaccia viene implementata da un particolare componente.

Per lo standard COM è necessario che una definizione di interfaccia non venga modificata dopo la pubblicazione. L'autore, ad esempio, non può aggiungere un nuovo metodo a un'interfaccia esistente. L'autore deve invece creare una nuova interfaccia. Sebbene non esistano restrizioni sui metodi che devono trovarsi in tale interfaccia, una pratica comune è che l'interfaccia di nuova generazione includa tutti i metodi dell'interfaccia precedente, oltre a tutti i nuovi metodi.

Non è insolito che un'interfaccia abbia diverse generazioni. In genere, tutte le generazioni eseguono essenzialmente la stessa attività complessiva, ma sono diverse nelle specifiche. Spesso, un componente COM implementa ogni generazione corrente e precedente di una determinata derivazione di un'interfaccia. In questo modo le applicazioni meno recenti possono continuare a utilizzare le interfacce precedenti dell'oggetto, mentre le applicazioni più recenti possono sfruttare le funzionalità delle interfacce più recenti. In genere, un gruppo di ridiscendenza di interfacce hanno tutti lo stesso nome, più un numero intero che indica la generazione. Ad esempio, se l'interfaccia originale era denominata **IMyInterface** (che implica la generazione 1), le due generazioni successive sarebbero denominate **IMyInterface2** e **IMyInterface3**. Nel caso di interfacce DirectX, le generazioni successive vengono in genere denominate per il numero di versione di DirectX.

## <a name="guids"></a>GUID

I GUID sono una parte essenziale del modello di programmazione COM. Per la maggior parte di base, un GUID è una struttura a 128 bit. Tuttavia, i GUID vengono creati in modo da garantire che due GUID non siano uguali. COM utilizza i GUID in maniera estensiva per due scopi primari.

- Per identificare in modo univoco un particolare componente COM. Un GUID assegnato per identificare un componente COM è denominato identificatore di classe (CLSID) e si utilizza un CLSID quando si desidera creare un'istanza del componente COM associato.
- Per identificare in modo univoco una particolare interfaccia COM. Un GUID assegnato per identificare un'interfaccia COM è denominato IID (Interface Identifier) e si utilizza un IID quando si richiede una particolare interfaccia da un'istanza di un componente (un oggetto). L'IID di un'interfaccia sarà lo stesso, indipendentemente dal componente che implementa l'interfaccia.

Per praticità, la documentazione di DirectX si riferisce in genere a componenti e interfacce in base ai relativi nomi descrittivi (ad esempio, **ID3D12Device**) anziché ai relativi GUID. Nel contesto della documentazione di DirectX, non c'è ambiguità. È tecnicamente possibile che un altro autore possa creare un'interfaccia con il nome descrittivo **ID3D12Device** (è necessario avere un IID diverso per essere valido). Per maggiore chiarezza, tuttavia, non è consigliabile.

Quindi, l'unico modo non ambiguo per fare riferimento a un oggetto o a un'interfaccia particolare consiste nel GUID.

Sebbene un GUID sia una struttura, un GUID viene spesso espresso in un formato stringa equivalente. Il formato generale del formato stringa di un GUID è 32 cifre esadecimali, nel formato 8-4-4-4-12. Ovvero {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}, dove ogni x corrisponde a una cifra esadecimale. Ad esempio, il formato stringa dell'IID per l'interfaccia **ID3D12Device** è {189819F1-1DB6-4B57-BE54-1821339B85F7}.

Poiché il GUID effettivo è piuttosto goffo da usare e facile da digitare, viene in genere fornito anche un nome equivalente. Nel codice è possibile usare questo nome invece della struttura effettiva quando si chiamano le funzioni, ad esempio quando si passa un argomento per il `riid` parametro a [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice). La convenzione di denominazione personalizzata prevede l'anteporre IID_ o CLSID_ al nome descrittivo dell'interfaccia o dell'oggetto, rispettivamente. Ad esempio, il nome dell'IID dell'interfaccia **ID3D12Device** viene IID_ID3D12Device.

> [!NOTE]
> Le applicazioni DirectX devono essere collegate con ``dxguid.lib`` e ``uuid.lib`` per fornire le definizioni per i diversi GUID dell'interfaccia e della classe. Visual C++ e altri compilatori supportano l'estensione del linguaggio dell'operatore **__uuidof** , ma il collegamento esplicito di tipo C con queste librerie di collegamenti è supportato e completamente portatile.

## <a name="hresult-values"></a>Valori HRESULT

La maggior parte dei metodi COM restituisce un Integer a 32 bit denominato **HRESULT**. Con la maggior parte dei metodi, HRESULT è essenzialmente una struttura che contiene due informazioni primarie.
- Indica se il metodo ha avuto esito positivo o negativo.
- Informazioni più dettagliate sul risultato dell'operazione eseguita dal metodo.

Alcuni metodi restituiscono un valore **HRESULT** dal set standard definito in `Winerror.h` . Tuttavia, un metodo è libero di restituire un valore **HRESULT** personalizzato con informazioni più specializzate. Questi valori sono in genere documentati nella pagina di riferimento del metodo.

L'elenco dei valori **HRESULT** individuati nella pagina di riferimento di un metodo è spesso solo un subset dei valori possibili che possono essere restituiti. Nell'elenco vengono in genere trattati solo i valori specifici del metodo, nonché i valori standard che hanno un significato specifico del metodo. Si supponga che un metodo possa restituire una serie di valori **HRESULT** standard, anche se non sono documentati in modo esplicito.

Sebbene i valori **HRESULT** vengano spesso utilizzati per restituire informazioni sugli errori, è consigliabile non considerarli come codici di errore. Il fatto che il bit che indica l'esito positivo o negativo venga archiviato separatamente dai bit che contengono le informazioni dettagliate consente ai valori **HRESULT** di avere un numero qualsiasi di codici di esito positivo e negativo. Per convenzione, i nomi dei codici di esito positivo sono preceduti da S_ e codici di errore E_. Ad esempio, i due codici usati più di frequente sono S_OK e E_FAIL, che indicano rispettivamente un semplice esito positivo o negativo.

Il fatto che i metodi COM possano restituire una serie di codici di esito positivo o negativo significa che è necessario prestare attenzione alla modalità di test del valore **HRESULT** . Si consideri, ad esempio, un ipotetico metodo con valori restituiti documentati di S_OK, se ha esito positivo e E_FAIL in caso contrario Tuttavia, tenere presente che il metodo può restituire anche altri codici di errore o di esito positivo. Il frammento di codice seguente illustra il rischio di usare un semplice test, dove `hr` contiene il valore **HRESULT** restituito dal metodo.

```cpp
if (hr == E_FAIL)
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Se, nel caso di errore, questo metodo restituisce solo E_FAIL (e non altri codici di errore), il test funziona. Tuttavia, è più realistico che un determinato metodo venga implementato per restituire un set di codici di errore specifici, ad esempio E_NOTIMPL o E_INVALIDARG. Con il codice precedente, questi valori verrebbero erroneamente interpretati come esito positivo.

Se sono necessarie informazioni dettagliate sul risultato della chiamata al metodo, è necessario testare ogni valore **HRESULT** pertinente. Tuttavia, si potrebbe essere interessati solo se il metodo ha avuto esito positivo o negativo. Un modo efficace per verificare se un valore **HRESULT** indica esito positivo o negativo è quello di passare il valore a una delle macro seguenti, definite in Winerror. h.

- La `SUCCEEDED` macro restituisce true per un codice di esito positivo e false per un codice di errore.
- La `FAILED` macro restituisce true per un codice di errore e false per un codice di esito positivo.

È quindi possibile correggere il frammento di codice precedente usando la `FAILED` macro, come illustrato nel codice seguente.

```cpp
if (FAILED(hr))
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Questo frammento di codice corretto considera correttamente E_NOTIMPL e E_INVALIDARG come errori.

Sebbene la maggior parte dei metodi COM restituisca valori **HRESULT** strutturati, un numero ridotto utilizza **HRESULT** per restituire un intero semplice. In modo implicito, questi metodi hanno sempre esito positivo. Se si passa un valore **HRESULT** di questo tipo alla macro SUCCEEDED, la macro restituisce sempre true. Un esempio di metodo comunemente chiamato che non restituisce **HRESULT** è il metodo **IUnknown:: Release** , che restituisce un ULONG. Questo metodo decrementa il conteggio dei riferimenti di un oggetto e restituisce il conteggio dei riferimenti corrente. Per informazioni sul conteggio dei riferimenti, vedere [gestione della durata di un oggetto com](#managing-a-com-objects-lifetime) .

## <a name="the-address-of-a-pointer"></a>Indirizzo di un puntatore

Se si visualizzano alcune pagine di riferimento del metodo COM, è probabile che si verifichi un risultato simile al seguente.

```cpp
HRESULT D3D12CreateDevice(
  IUnknown          *pAdapter,
  D3D_FEATURE_LEVEL MinimumFeatureLevel,
  REFIID            riid,
  void              **ppDevice
);
```

Sebbene un puntatore normale sia abbastanza familiare per gli sviluppatori C/C++, COM spesso usa un livello di riferimento indiretto aggiuntivo. Questo secondo livello di riferimento indiretto è indicato da due asterischi, `**` , che seguono la dichiarazione del tipo e il nome della variabile ha in genere un prefisso `pp` . Per la funzione precedente, il `ppDevice` parametro viene in genere definito come l'indirizzo di un puntatore a un void. In pratica, in questo esempio, `ppDevice` è l'indirizzo di un puntatore a un'interfaccia **ID3D12Device** .

A differenza di un oggetto C++, non è possibile accedere direttamente ai metodi di un oggetto COM. Al contrario, è necessario ottenere un puntatore a un'interfaccia che espone il metodo. Per richiamare il metodo, è necessario usare essenzialmente la stessa sintassi usata per richiamare un puntatore a un metodo C++. Per richiamare il metodo **IMyInterface::D osomething** , ad esempio, usare la sintassi seguente.

```cpp
IMyInterface * pMyIface = nullptr;
...
pMyIface->DoSomething(...);
```

La necessità di un secondo livello di riferimento indiretto deriva dal fatto che i puntatori di interfaccia non vengono creati direttamente. È necessario chiamare uno dei diversi metodi, ad esempio il metodo **D3D12CreateDevice** illustrato in precedenza. Per usare questo metodo per ottenere un puntatore a interfaccia, dichiarare una variabile come puntatore all'interfaccia desiderata, quindi passare l'indirizzo della variabile al metodo. In altre parole, si passa l'indirizzo di un puntatore al metodo. Quando il metodo restituisce, la variabile punta all'interfaccia richiesta ed è possibile usare tale puntatore per chiamare uno dei metodi dell'interfaccia.

```cpp
IDXGIAdapter * pIDXGIAdapter = nullptr;
...
ID3D12Device * pD3D12Device = nullptr;
HRESULT hr = ::D3D12CreateDevice(
    pIDXGIAdapter,
    D3D_FEATURE_LEVEL_11_0,
    IID_ID3D12Device,
    &pD3D12Device);
if (FAILED(hr)) return E_FAIL;

// Now use pD3D12Device in the form pD3D12Device->MethodName(...);
```

## <a name="creating-a-com-object"></a>Creazione di un oggetto COM

Esistono diversi modi per creare un oggetto COM. Questi sono i due più comunemente usati nella programmazione DirectX.

- Indirettamente, chiamando un metodo o una funzione DirectX che crea automaticamente l'oggetto. Il metodo crea l'oggetto e restituisce un'interfaccia sull'oggetto. Quando si crea un oggetto in questo modo, talvolta è possibile specificare l'interfaccia da restituire, altre volte l'interfaccia è implicita. Nell'esempio di codice precedente viene illustrato come creare indirettamente un oggetto COM Direct3D 12 per dispositivi.
- Direttamente, passando il CLSID dell'oggetto alla [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). La funzione crea un'istanza dell'oggetto e restituisce un puntatore a un'interfaccia specificata.

Una volta, prima di creare qualsiasi oggetto COM, è necessario inizializzare COM chiamando la [**funzione CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Se gli oggetti vengono creati indirettamente, il metodo di creazione dell'oggetto gestisce questa attività. Tuttavia, se è necessario creare un oggetto con **CoCreateInstance**, è necessario chiamare **CoInitializeEx** in modo esplicito. Al termine, è necessario non inizializzare COM chiamando [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Se si effettua una chiamata a **CoInitializeEx** , è necessario associarla a una chiamata a **CoUninitialize**. In genere, le applicazioni che devono inizializzare in modo esplicito COM eseguono questa operazione nella routine di avvio e deinizializzano COM nella routine di pulizia.

Per creare una nuova istanza di un oggetto COM con **CoCreateInstance**, è necessario avere il CLSID dell'oggetto. Se il CLSID è disponibile pubblicamente, sarà possibile trovarlo nella documentazione di riferimento o nel file di intestazione appropriato. Se il CLSID non è disponibile pubblicamente, non è possibile creare l'oggetto direttamente.

La funzione **CoCreateInstance** ha cinque parametri. Per gli oggetti COM che verranno usati con DirectX, in genere è possibile impostare i parametri come indicato di seguito.

*rclsid* Impostare questa impostazione sul CLSID dell'oggetto che si desidera creare.

*pUnkOuter* Impostare su `nullptr` . Questo parametro viene utilizzato solo se si stanno aggregando oggetti. Una discussione sull'aggregazione COM esula dall'ambito di questo argomento.

*dwClsContext* Impostare su CLSCTX_INPROC_SERVER. Questa impostazione indica che l'oggetto viene implementato come DLL e viene eseguito come parte del processo dell'applicazione.

*riid* Impostare sull'IID dell'interfaccia che si desidera venga restituita. La funzione creerà l'oggetto e restituirà il puntatore a interfaccia richiesto nel parametro PPV.

*PPV* Impostare questo valore sull'indirizzo di un puntatore che verrà impostato sull'interfaccia specificata da `riid` quando la funzione restituisce. Questa variabile deve essere dichiarata come puntatore all'interfaccia richiesta e il riferimento al puntatore nell'elenco di parametri deve essere eseguito come (LPVOID *).

La creazione di un oggetto indirettamente è in genere molto più semplice, come illustrato nell'esempio di codice precedente. Si passa il metodo di creazione dell'oggetto all'indirizzo di un puntatore a interfaccia, quindi il metodo crea l'oggetto e restituisce un puntatore a interfaccia. Quando si crea un oggetto indirettamente, anche se non è possibile scegliere l'interfaccia restituita dal metodo, spesso è comunque possibile specificare una serie di elementi relativi alla modalità di creazione dell'oggetto.

Ad esempio, è possibile passare a **D3D12CreateDevice** un valore che specifica il livello di funzionalità D3D minimo che deve essere supportato dal dispositivo restituito, come illustrato nell'esempio di codice precedente.

## <a name="using-com-interfaces"></a>Uso di interfacce COM

Quando si crea un oggetto COM, il metodo di creazione restituisce un puntatore a interfaccia. È quindi possibile usare tale puntatore per accedere a uno dei metodi dell'interfaccia. La sintassi è identica a quella usata con un puntatore a un metodo C++.

## <a name="requesting-additional-interfaces"></a>Richiesta di interfacce aggiuntive

In molti casi, il puntatore a un'interfaccia che si riceve dal metodo di creazione può essere l'unico necessario. Di fatto, è relativamente comune che un oggetto esporti solo un'interfaccia diversa da **IUnknown**. Tuttavia, molti oggetti esportano più interfacce e potrebbero essere necessari puntatori a molti di essi. Se sono necessarie più interfacce di quelle restituite dal metodo di creazione, non è necessario creare un nuovo oggetto. È necessario invece richiedere un altro puntatore a interfaccia usando il [**metodo IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void))dell'oggetto.

Se si crea l'oggetto con **CoCreateInstance**, è possibile richiedere un puntatore all'interfaccia **IUnknown** e quindi chiamare **IUnknown:: QueryInterface** per richiedere ogni interfaccia necessaria. Tuttavia, questo approccio è scomodo se è necessaria una sola interfaccia e non funziona affatto se si usa un metodo di creazione di un oggetto che non consente di specificare quale puntatore a interfaccia deve essere restituito. In pratica, in genere non è necessario ottenere un puntatore **IUnknown** esplicito, perché tutte le interfacce com estendono l'interfaccia **IUnknown** .

L'estensione di un'interfaccia è concettualmente simile all'ereditarietà da una classe C++. L'interfaccia figlio espone tutti i metodi dell'interfaccia padre, oltre a uno o più dei relativi. In realtà, viene spesso visualizzato "eredita da" usato al posto di "extends". È necessario ricordare che l'ereditarietà è interna all'oggetto. L'applicazione non può ereditare o estendere l'interfaccia di un oggetto. Tuttavia, è possibile usare l'interfaccia figlio per chiamare qualsiasi metodo del figlio o dell'elemento padre.

Poiché tutte le interfacce sono elementi figlio di **IUnknown**, è possibile chiamare **QueryInterface** su qualsiasi puntatore di interfaccia già disponibile per l'oggetto. Quando si esegue questa operazione, è necessario fornire l'IID dell'interfaccia richiesta e l'indirizzo di un puntatore che conterrà il puntatore di interfaccia quando il metodo restituisce un risultato.

Nel frammento di codice seguente, ad esempio, viene chiamato **IDXGIFactory2:: CreateSwapChainForHwnd** per creare un oggetto catena di scambio primario. Questo oggetto espone diverse interfacce. Il metodo **CreateSwapChainForHwnd** restituisce un'interfaccia **IDXGISwapChain1** . Il codice successivo usa quindi l'interfaccia **IDXGISwapChain1** per chiamare **QueryInterface** per richiedere un'interfaccia **IDXGISwapChain3** .

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;
```

> [!NOTE]
> In C++ è possibile usare la ``IID_PPV_ARGS`` macro anziché l'IID esplicito e il puntatore del cast: ``pDXGISwapChain1->QueryInterface(IID_PPV_ARGS(&pDXGISwapChain3));`` .
> Viene spesso usato per i metodi di creazione e **QueryInterface**. Per ulteriori informazioni, vedere [combaseapi. h](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args) .

## <a name="managing-a-com-objects-lifetime"></a>Gestione della durata di un oggetto COM

Quando viene creato un oggetto, il sistema alloca le risorse di memoria necessarie. Quando un oggetto non è più necessario, deve essere eliminato definitivamente. Il sistema può utilizzare tale memoria per altri scopi. Con gli oggetti C++, è possibile controllare la durata dell'oggetto direttamente con `new` gli `delete` operatori e nei casi in cui si sta operando a tale livello o semplicemente utilizzando la durata dello stack e dell'ambito. COM non consente di creare o distruggere direttamente oggetti. Il motivo di questa progettazione è che lo stesso oggetto può essere utilizzato da più di una parte dell'applicazione o, in alcuni casi, da più di un'applicazione. Se uno di questi riferimenti era quello di eliminare l'oggetto, gli altri riferimenti diventeranno non validi. COM utilizza invece un sistema di conteggio dei riferimenti per controllare la durata di un oggetto.

Il conteggio dei riferimenti di un oggetto indica il numero di volte in cui è stata richiesta una delle relative interfacce. Ogni volta che viene richiesta un'interfaccia, il conteggio dei riferimenti viene incrementato. Un'applicazione rilascia un'interfaccia quando tale interfaccia non è più necessaria, decrementa il conteggio dei riferimenti. Fino a quando il conteggio dei riferimenti è maggiore di zero, l'oggetto rimane in memoria. Quando il conteggio dei riferimenti raggiunge zero, l'oggetto Elimina se stesso. Non è necessario conoscere il conteggio dei riferimenti di un oggetto. Fino a quando si ottengono e si rilasciano correttamente le interfacce di un oggetto, l'oggetto avrà la durata appropriata.

Una gestione corretta del conteggio dei riferimenti è una parte essenziale della programmazione COM. In caso contrario, è possibile creare facilmente una perdita di memoria o un arresto anomalo. Uno degli errori più comuni apportati dai programmatori COM non riesce a rilasciare un'interfaccia. In tal caso, il conteggio dei riferimenti non raggiunge mai zero e l'oggetto rimane in memoria per un periodo illimitato.

> [!NOTE]
> Direct3D 10 o versione successiva ha regole di durata leggermente modificate per gli oggetti. In particolare, gli oggetti derivati da **ID3DxxDeviceChild** non sopravvivono mai al dispositivo padre (ovvero se il **ID3DxxDevice** proprietario raggiunge un refcount 0, anche tutti gli oggetti figlio sono immediatamente non validi). Inoltre, quando si utilizzano i metodi **set** per associare oggetti alla pipeline di rendering, questi riferimenti non aumentano il conteggio dei riferimenti, ovvero sono riferimenti deboli. In pratica, questa operazione viene gestita in modo ottimale garantendo il rilascio completo di tutti gli oggetti figlio del dispositivo prima di rilasciare il dispositivo.

## <a name="incrementing-and-decrementing-the-reference-count"></a>Incremento e decremento del conteggio dei riferimenti

Ogni volta che si ottiene un nuovo puntatore di interfaccia, il conteggio dei riferimenti deve essere incrementato da una chiamata a [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref). Tuttavia, l'applicazione in genere non deve chiamare questo metodo. Se si ottiene un puntatore a interfaccia chiamando un metodo di creazione di un oggetto o chiamando **IUnknown:: QueryInterface**, l'oggetto incrementa automaticamente il conteggio dei riferimenti. Tuttavia, se si crea un puntatore di interfaccia in un altro modo, ad esempio la copia di un puntatore esistente, è necessario chiamare in modo esplicito **IUnknown:: AddRef**. In caso contrario, quando si rilascia il puntatore di interfaccia originale, è possibile che l'oggetto venga eliminato definitivamente anche se è ancora necessario utilizzare la copia del puntatore.

È necessario rilasciare tutti i puntatori a interfaccia, indipendentemente dal fatto che l'utente o l'oggetto abbia incrementato il conteggio dei riferimenti. Quando un puntatore di interfaccia non è più necessario, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) per decrementare il conteggio dei riferimenti. Una procedura comune consiste nell'inizializzare tutti i puntatori di interfaccia a `nullptr` e quindi per impostarli nuovamente `nullptr` quando vengono rilasciati. Tale convenzione consente di testare tutti i puntatori di interfaccia nel codice di pulizia. Quelli che non sono `nullptr` ancora attivi ed è necessario rilasciarli prima di terminare l'applicazione.

Il frammento di codice seguente estende l'esempio illustrato in precedenza per illustrare come gestire il conteggio dei riferimenti.

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3Copy = nullptr;

// Make a copy of the IDXGISwapChain3 interface pointer.
// Call AddRef to increment the reference count and to ensure that
// the object is not destroyed prematurely.
pDXGISwapChain3Copy = pDXGISwapChain3;
pDXGISwapChain3Copy->AddRef();
...
// Cleanup code. Check to see whether the pointers are still active.
// If they are, then call Release to release the interface.
if (pDXGISwapChain1 != nullptr)
{
    pDXGISwapChain1->Release();
    pDXGISwapChain1 = nullptr;
}
if (pDXGISwapChain3 != nullptr)
{
    pDXGISwapChain3->Release();
    pDXGISwapChain3 = nullptr;
}
if (pDXGISwapChain3Copy != nullptr)
{
    pDXGISwapChain3Copy->Release();
    pDXGISwapChain3Copy = nullptr;
}
```

## <a name="com-smart-pointers"></a>Puntatori intelligenti COM

Il codice finora ha chiamato in modo esplicito ``Release`` e ``AddRef`` per mantenere i conteggi dei riferimenti usando i metodi **IUnknown** . Questo modello richiede che il programmatore sia diligente nel ricordare di gestire correttamente il conteggio in tutti i possibili percorsi di codepath. Questo può comportare una complessa gestione degli errori e la gestione delle eccezioni C++ abilitata può essere particolarmente difficile da implementare. Una soluzione migliore con C++ consiste nell'usare un [puntatore intelligente](/cpp/cpp/smart-pointers-modern-cpp).

* **WinRT:: com_ptr** è un puntatore intelligente fornito dalle [proiezioni del linguaggio C++/WinRT](/uwp/cpp-ref-for-winrt/com-ptr). Si tratta del puntatore intelligente COM consigliato da usare per le app UWP. Si noti che C++/WinRT richiede C++ 17.

* **Microsoft:: WRL:: ComPtr** è un puntatore intelligente fornito dalla [libreria di modelli C++ Windows Runtime (WRL)](/cpp/cppcx/wrl/comptr-class). Questa libreria è "pure" C++, quindi può essere usata per Windows Runtime applicazioni (tramite C++/CX o C++/WinRT), nonché per le applicazioni desktop Win32 classiche. Questo puntatore intelligente funziona anche nelle versioni precedenti di Windows che non supportano le API Windows Runtime. Per le applicazioni desktop Win32, è possibile utilizzare ``#include <wrl/client.h>`` per includere solo questa classe e, facoltativamente, definire anche il simbolo del preprocessore ``__WRL_CLASSIC_COM_STRICT__`` . Per ulteriori informazioni, vedere la pagina relativa ai [puntatori intelligenti com rivisitati](/archive/msdn-magazine/2015/february/windows-with-c-com-smart-pointers-revisited).

* **CComPtr** è un puntatore intelligente fornito dal [Active Template Library (ATL)](/cpp/atl/reference/ccomptr-class). **Microsoft:: WRL:: ComPtr** è una versione più recente di questa implementazione che risolve diversi problemi di utilizzo, pertanto l'utilizzo di questo puntatore intelligente non è consigliato per i nuovi progetti. Per ulteriori informazioni, vedere [come creare e usare CComPtr e CComQIPtr](/cpp/cpp/how-to-create-and-use-ccomptr-and-ccomqiptr-instances).


## <a name="using-atl-with-directx-9"></a>Uso di ATL con DirectX 9

Per utilizzare il Active Template Library (ATL) con DirectX 9, è necessario ridefinire le interfacce per la compatibilità con ATL. Ciò consente di utilizzare correttamente la classe **CComQIPtr** per ottenere un puntatore a un'interfaccia.

Si saprà che se non si ridefiniscono le interfacce per ATL, verrà visualizzato il messaggio di errore seguente.

```
[...]\atlmfc\include\atlbase.h(4704) :   error C2787: 'IDirectXFileData' : no GUID has been associated with this object
```

Nell'esempio di codice seguente viene illustrato come definire l'interfaccia IDirectXFileData.

```cpp
// Explicit declaration
struct __declspec(uuid("{3D82AB44-62DA-11CF-AB39-0020AF71E433}")) IDirectXFileData;

// Macro method
#define RT_IID(iid_, name_) struct __declspec(uuid(iid_)) name_
RT_IID("{1DD9E8DA-1C77-4D40-B0CF-98FEFDFF9512}", IDirectXFileData);
```

Dopo aver ridefinito l'interfaccia, è necessario usare il metodo di **associazione** per collegare l'interfaccia al puntatore di interfaccia restituito da **::D irect3dcreate9**. In caso contrario, l'interfaccia **IDirect3D9** non verrà rilasciata correttamente dalla classe del puntatore intelligente.

La classe **CComPtr** chiama internamente **IUnknown:: AddRef** sul puntatore a interfaccia quando viene creato l'oggetto e quando un'interfaccia viene assegnata alla classe **CComPtr** . Per evitare la perdita del puntatore a interfaccia, non chiamare * * IUnknown:: AddRef sull'interfaccia restituita da **::D irect3dcreate9**.

Il codice seguente rilascia correttamente l'interfaccia senza chiamare **IUnknown:: AddRef**.

```cpp
CComPtr<IDirect3D9> d3d;
d3d.Attach(::Direct3DCreate9(D3D_SDK_VERSION));
```

Usare il codice precedente. Non usare il codice seguente, che chiama **IUnknown:: AddRef** seguito da **IUnknown:: Release** e non rilascia il riferimento aggiunto da **::D irect3dcreate9**.

```cpp
CComPtr<IDirect3D9> d3d = ::Direct3DCreate9(D3D_SDK_VERSION);
```

Si noti che questa è l'unica posizione in Direct3D 9 in cui è necessario usare il metodo di **associazione** in questo modo.

Per ulteriori informazioni sulle classi **CComPTR** e **CComQIPtr** , vedere le relative definizioni nel `Atlbase.h` file di intestazione.
