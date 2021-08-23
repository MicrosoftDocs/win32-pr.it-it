---
description: Programmazione di DirectX con COM.
title: Programmazione di DirectX con COM
ms.topic: article
ms.date: 01/29/2019
ms.openlocfilehash: 660f030e56d0b84325f7b90a9e2cc8e3864587660dd452611f41c78241220f54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600201"
---
# <a name="programming-directx-with-com"></a>Programmazione di DirectX con COM

Microsoft Component Object Model (COM) è un modello di programmazione orientato a oggetti usato da diverse tecnologie, inclusa la maggior parte della superficie dell'API DirectX. Per questo motivo, gli sviluppatori DirectX usano inevitabilmente COM quando si programma DirectX.

> [!NOTE]
> L'argomento Utilizzare componenti COM con [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/consume-com) illustra come usare le API DirectX (e qualsiasi API COM, in questo caso) usando [C++/WinRT.](/windows/uwp/cpp-and-winrt-apis/) Questa è di gran lunga la tecnologia più comoda e consigliata da usare.

In alternativa, è possibile usare COM non elaborato e questo è il tema di questo argomento. Sarà necessaria una conoscenza di base dei principi e delle tecniche di programmazione coinvolti nell'utilizzo delle API COM. Sebbene COM abbia la reputazione di essere difficile e complesso, la programmazione COM richiesta dalla maggior parte delle applicazioni DirectX è semplice. In parte, ciò è dovuto al fatto che si utilizzano gli oggetti COM forniti da DirectX. Non è necessario creare oggetti COM personalizzati, che in genere è il punto in cui si verifica la complessità.

## <a name="com-component-overview"></a>Panoramica del componente COM

Un oggetto COM è essenzialmente un componente incapsulato di funzionalità che può essere usato dalle applicazioni per eseguire una o più attività. Per la distribuzione, uno o più componenti COM vengono suddivisi in un pacchetto binario denominato server COM. più spesso di una DLL.

Una DLL tradizionale esporta funzioni gratuite. Un server COM può eseguire la stessa operazione. Tuttavia, i componenti COM all'interno del server COM espongono interfacce COM e metodi membro appartenenti a tali interfacce. L'applicazione crea istanze di componenti COM, recupera le interfacce da tali componenti e chiama metodi su tali interfacce per trarre vantaggio dalle funzionalità implementate nei componenti COM.

In pratica, sembra simile alla chiamata di metodi su un normale oggetto C++. Esistono tuttavia alcune differenze.

- Un oggetto COM impone un incapsulamento più rigoroso rispetto a un oggetto C++. Non è sufficiente creare l'oggetto e quindi chiamare qualsiasi metodo pubblico. Al contrario, i metodi pubblici di un componente COM sono raggruppati in una o più interfacce COM. Per chiamare un metodo, creare l'oggetto e recuperare dall'oggetto l'interfaccia che implementa il metodo . Un'interfaccia implementa in genere un set correlato di metodi che forniscono l'accesso a una particolare funzionalità dell'oggetto. Ad esempio, [**l'interfaccia ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) rappresenta una scheda grafica virtuale e contiene metodi che consentono di creare risorse, ad esempio, e molte altre attività correlate alla scheda.
- Un oggetto COM non viene creato nello stesso modo di un oggetto C++. Esistono diversi modi per creare un oggetto COM, ma tutti prevedono tecniche specifiche di COM. L'API DirectX include un'ampia gamma di funzioni helper e metodi che semplificano la creazione della maggior parte degli oggetti COM DirectX.
- È necessario utilizzare tecniche specifiche di COM per controllare la durata di un oggetto COM.
- Il server COM (in genere una DLL) non deve essere caricato in modo esplicito. Né si collega a una libreria statica per usare un componente COM. Ogni componente COM ha un identificatore registrato univoco (identificatore univoco globale o GUID) che l'applicazione usa per identificare l'oggetto COM. L'applicazione identifica il componente e il runtime COM carica automaticamente la DLL del server COM corretta.
- COM è una specifica binaria. È possibile scrivere oggetti COM e accedervi da un'ampia gamma di linguaggi. Non è necessario conoscere il codice sorgente dell'oggetto. Ad esempio, Visual Basic usano regolarmente oggetti COM scritti in C++.

## <a name="component-object-and-interface"></a>Componente, oggetto e interfaccia

È importante comprendere la distinzione tra componenti, oggetti e interfacce. In caso di utilizzo casuale, è possibile che si senta un componente o un oggetto a cui si fa riferimento con il nome dell'interfaccia principale. Ma i termini non sono intercambiabili. Un componente può implementare un numero qualsiasi di interfacce. e un oggetto è un'istanza di un componente. Ad esempio, anche se tutti i componenti devono implementare [**l'interfaccia IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), in genere implementano almeno un'interfaccia aggiuntiva e potrebbero implementarne molte.

Per usare un metodo di interfaccia specifico, non solo è necessario creare un'istanza di un oggetto, ma anche ottenere l'interfaccia corretta.

Inoltre, più di un componente potrebbe implementare la stessa interfaccia. Un'interfaccia è un gruppo di metodi che eseguono un set di operazioni correlate logicamente. La definizione dell'interfaccia specifica solo la sintassi dei metodi e le relative funzionalità generali. Qualsiasi componente COM che deve supportare un particolare set di operazioni può eseguire questa operazione implementando un'interfaccia appropriata. Alcune interfacce sono altamente specializzate e vengono implementate solo da un singolo componente. altri sono utili in diverse circostanze e vengono implementati da molti componenti.

Se un componente implementa un'interfaccia, deve supportare ogni metodo nella definizione dell'interfaccia. In altre parole, è necessario essere in grado di chiamare qualsiasi metodo e di essere certi che esista. Tuttavia, i dettagli della modalità di implementazione di un determinato metodo possono variare da un componente a un altro. Ad esempio, componenti diversi possono usare algoritmi diversi per arrivare al risultato finale. Non esiste inoltre alcuna garanzia che un metodo sia supportato in modo non generico. In alcuni casi, un componente implementa un'interfaccia di uso comune, ma deve supportare solo un subset dei metodi. Sarà comunque possibile chiamare correttamente i metodi rimanenti, ma restituiranno un [**HRESULT**](#hresult-values) (ovvero un tipo COM standard che rappresenta un codice di risultato) contenente il valore **E_NOTIMPL**. È consigliabile fare riferimento alla relativa documentazione per vedere come un'interfaccia viene implementata da un componente specifico.

Lo standard COM richiede che una definizione di interfaccia non cambi dopo la pubblicazione. L'autore non può, ad esempio, aggiungere un nuovo metodo a un'interfaccia esistente. L'autore deve invece creare una nuova interfaccia. Anche se non esistono restrizioni sui metodi che devono essere presenti in tale interfaccia, una pratica comune consiste nel fare in modo che l'interfaccia di nuova generazione includa tutti i metodi dell'interfaccia precedente, oltre a tutti i nuovi metodi.

Non è insolito che un'interfaccia abbia diverse generazioni. In genere, tutte le generazioni eseguono essenzialmente la stessa attività complessiva, ma sono diverse in specifiche. Spesso, un componente COM implementa ogni generazione corrente e precedente della derivazione di una determinata interfaccia. In questo modo le applicazioni meno recenti possono continuare a usare le interfacce precedenti dell'oggetto, mentre le applicazioni più recenti possono sfruttare le funzionalità delle interfacce più recenti. In genere, un gruppo di interfacce di discesa ha lo stesso nome, più un numero intero che indica la generazione. Ad esempio, se l'interfaccia originale fosse denominata **IMyInterface** (che implica la generazione 1), le due generazioni successive saranno denominate **IMyInterface2** e **IMyInterface3**. Nel caso delle interfacce DirectX, le generazioni successive vengono in genere denominate in base al numero di versione di DirectX.

## <a name="guids"></a>GUID

I GUID sono una parte fondamentale del modello di programmazione COM. Nella sua forma più semplice, un GUID è una struttura a 128 bit. Tuttavia, i GUID vengono creati in modo da garantire che due GUID non siano uguali. COM usa i GUID ampiamente per due scopi principali.

- Per identificare in modo univoco un particolare componente COM. Un GUID assegnato per identificare un componente COM è denominato identificatore di classe (CLSID) e si utilizza un CLSID quando si desidera creare un'istanza del componente COM associato.
- Per identificare in modo univoco una determinata interfaccia COM. Un GUID assegnato per identificare un'interfaccia COM è detto identificatore di interfaccia (IID) e si usa un IID quando si richiede una particolare interfaccia da un'istanza di un componente (un oggetto ). L'IID di un'interfaccia sarà lo stesso, indipendentemente dal componente che implementa l'interfaccia.

Per praticità, la documentazione di DirectX si riferisce in genere ai componenti e alle interfacce in base ai nomi descrittivi (ad esempio **ID3D12Device)** anziché ai relativi GUID. Nel contesto della documentazione di DirectX non vi è ambiguità. Tecnicamente, è possibile che una terza parte autore un'interfaccia con il nome descrittivo **ID3D12Device** (per essere valida deve avere un IID diverso). Per maggiore chiarezza, tuttavia, non è consigliabile.

Pertanto, l'unico modo non ambiguo per fare riferimento a un oggetto o a un'interfaccia specifica è tramite il RELATIVO GUID.

Anche se un GUID è una struttura, un GUID viene spesso espresso in forma di stringa equivalente. Il formato generale del formato stringa di un GUID è di 32 cifre esadecimali, nel formato 8-4-4-4-12. In altri casi, {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}, dove ogni x corrisponde a una cifra esadecimale. Ad esempio, il formato stringa dell'IID per l'interfaccia **ID3D12Device** è {189819F1-1DB6-4B57-BE54-1821339B85F7}.

Poiché il GUID effettivo è piuttosto difficile da usare e facile da digitare in modo non corretto, viene in genere fornito anche un nome equivalente. Nel codice è possibile usare questo nome anziché la struttura effettiva quando si chiamano le funzioni, ad esempio quando si passa un argomento per il parametro a `riid` [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice). La convenzione di denominazione standard è anteporre IID_ o CLSID_ al nome descrittivo dell'interfaccia o dell'oggetto, rispettivamente. Ad esempio, il nome dell'IID **dell'interfaccia ID3D12Device** è IID_ID3D12Device.

> [!NOTE]
> Le applicazioni DirectX devono collegarsi ``dxguid.lib`` a e per fornire ``uuid.lib`` definizioni per i vari GUID di interfaccia e classe. Visual C++ e altri compilatori supportano l'estensione del linguaggio dell'operatore **__uuidof,** ma il collegamento esplicito in stile C con queste librerie di collegamento è supportato e completamente portabile.

## <a name="hresult-values"></a>Valori HRESULT

La maggior parte dei metodi COM restituisce un intero a 32 bit denominato **HRESULT.** Con la maggior parte dei metodi, HRESULT è essenzialmente una struttura che contiene due informazioni principali.
- Indica se il metodo ha avuto esito positivo o negativo.
- Informazioni più dettagliate sul risultato dell'operazione eseguita dal metodo .

Alcuni metodi restituiscono **un valore HRESULT** dal set standard definito in `Winerror.h` . Tuttavia, un metodo è libero di restituire un valore **HRESULT** personalizzato con informazioni più specializzate. Questi valori sono in genere documentati nella pagina di riferimento del metodo.

L'elenco **di valori HRESULT** disponibili nella pagina di riferimento di un metodo è spesso solo un subset dei valori possibili che possono essere restituiti. L'elenco in genere copre solo i valori specifici del metodo, nonché i valori standard che hanno un significato specifico del metodo. Si presuppone che un metodo possa restituire un'ampia gamma di valori **HRESULT** standard, anche se non sono documentati in modo esplicito.

Anche **se i valori HRESULT** vengono spesso usati per restituire informazioni sugli errori, non è consigliabile pensarli come codici di errore. Il fatto che il bit che indica l'esito positivo o negativo sia archiviato separatamente dai bit che contengono le informazioni dettagliate consente ai valori **HRESULT** di avere un numero qualsiasi di codici di esito positivo e negativo. Per convenzione, i nomi dei codici di esito positivo sono preceduti da S_ e dai codici di errore E_. Ad esempio, i due codici usati più di frequente sono S_OK e E_FAIL, che indicano rispettivamente un esito positivo o negativo semplice.

Il fatto che i metodi COM possano restituire un'ampia gamma di codici di esito positivo o negativo significa che è necessario prestare attenzione alla modalità di test **del valore HRESULT.** Si consideri ad esempio un metodo ipotetico con valori restituiti documentati di S_OK in caso di esito positivo e E_FAIL in caso contrario. Tenere tuttavia presente che il metodo può restituire anche altri codici di errore o di esito positivo. Il frammento di codice seguente illustra il rischio di usare un test semplice, in cui `hr` contiene il **valore HRESULT** restituito dal metodo .

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

Se, nel caso di errore, questo metodo restituisce solo E_FAIL (e non un altro codice di errore), questo test funziona. Tuttavia, è più realistico che un determinato metodo sia implementato per restituire un set di codici di errore specifici, ad esempio E_NOTIMPL o E_INVALIDARG. Con il codice precedente, questi valori verrebbero interpretati erroneamente come un esito positivo.

Se sono necessarie informazioni dettagliate sul risultato della chiamata al metodo, è necessario testare ogni valore **HRESULT** pertinente. Tuttavia, può essere interessato solo se il metodo ha avuto esito positivo o negativo. Un modo efficace per verificare se un valore **HRESULT** indica esito positivo o negativo è passare il valore a una delle macro seguenti, definite in Winerror.h.

- La `SUCCEEDED` macro restituisce TRUE per un codice di esito positivo e FALSE per un codice di errore.
- La `FAILED` macro restituisce TRUE per un codice di errore e FALSE per un codice di esito positivo.

È quindi possibile correggere il frammento di codice precedente usando la `FAILED` macro , come illustrato nel codice seguente.

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

Anche se la maggior parte dei metodi COM restituiscono valori **HRESULT** strutturati, un numero ridotto usa **HRESULT** per restituire un numero intero semplice. In modo implicito, questi metodi hanno sempre esito positivo. Se si passa **un HRESULT** di questo tipo alla macro SUCCEEDED, la macro restituisce sempre TRUE. Un esempio di metodo comunemente chiamato che non restituisce **un HRESULT** è il metodo **IUnknown::Release,** che restituisce un ULONG. Questo metodo decrementa di uno il conteggio dei riferimenti di un oggetto e restituisce il conteggio dei riferimenti corrente. Per [informazioni sul conteggio dei](#managing-a-com-objects-lifetime) riferimenti, vedere Gestione della durata di un oggetto COM.

## <a name="the-address-of-a-pointer"></a>Indirizzo di un puntatore

Se si visualizzano alcune pagine di riferimento al metodo COM, è probabile che si eseere in un modo simile al seguente.

```cpp
HRESULT D3D12CreateDevice(
  IUnknown          *pAdapter,
  D3D_FEATURE_LEVEL MinimumFeatureLevel,
  REFIID            riid,
  void              **ppDevice
);
```

Anche se un puntatore normale è abbastanza noto a qualsiasi sviluppatore C/C++, COM usa spesso un livello aggiuntivo di riferimento indiretto. Questo secondo livello di riferimento indiretto è indicato da due asterischi, , dopo la dichiarazione del tipo e il nome della variabile ha in genere `**` un prefisso `pp` . Per la funzione precedente, il parametro viene in genere `ppDevice` definito come l'indirizzo di un puntatore a un void. In pratica, in questo esempio, `ppDevice` è l'indirizzo di un puntatore a **un'interfaccia ID3D12Device.**

A differenza di un oggetto C++, non si accede direttamente ai metodi di un oggetto COM. È invece necessario ottenere un puntatore a un'interfaccia che espone il metodo . Per richiamare il metodo, usare essenzialmente la stessa sintassi utilizzata per richiamare un puntatore a un metodo C++. Ad esempio, per richiamare il **metodo IMyInterface::D oSomething,** usare la sintassi seguente.

```cpp
IMyInterface * pMyIface = nullptr;
...
pMyIface->DoSomething(...);
```

La necessità di un secondo livello di riferimento indiretto deriva dal fatto che non si creano direttamente puntatori a interfaccia. È necessario chiamare uno dei diversi metodi, ad esempio il metodo **D3D12CreateDevice** illustrato in precedenza. Per usare tale metodo per ottenere un puntatore a interfaccia, dichiarare una variabile come puntatore all'interfaccia desiderata e quindi passare l'indirizzo di tale variabile al metodo . In altre parole, si passa l'indirizzo di un puntatore al metodo . Quando il metodo viene restituito, la variabile punta all'interfaccia richiesta ed è possibile usare tale puntatore per chiamare uno dei metodi dell'interfaccia.

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

- Indirettamente, chiamando un metodo o una funzione DirectX che crea automaticamente l'oggetto. Il metodo crea l'oggetto e restituisce un'interfaccia sull'oggetto . Quando si crea un oggetto in questo modo, talvolta è possibile specificare l'interfaccia da restituire, altre volte l'interfaccia è implicita. L'esempio di codice precedente illustra come creare indirettamente un oggetto COM del dispositivo Direct3D 12.
- Direttamente, passando il CLSID dell'oggetto alla [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). La funzione crea un'istanza dell'oggetto e restituisce un puntatore a un'interfaccia specificata.

Una volta, prima di creare qualsiasi oggetto COM, è necessario inizializzare COM chiamando la [**funzione CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Se si creano oggetti indirettamente, il metodo di creazione dell'oggetto gestisce questa attività. Tuttavia, se è necessario creare un oggetto con **CoCreateInstance**, è necessario chiamare **CoInitializeEx in** modo esplicito. Al termine, COM deve essere non inizializzato chiamando [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Se si effettua una chiamata a **CoInitializeEx,** è necessario associarla a una chiamata a **CoUninitialize**. In genere, le applicazioni che devono inizializzare COM in modo esplicito lo fanno nella routine di avvio e annullano l'inizializzazione com nella routine di pulizia.

Per creare una nuova istanza di un oggetto COM con **CoCreateInstance,** è necessario disporre del CLSID dell'oggetto. Se questo CLSID è disponibile pubblicamente, è disponibile nella documentazione di riferimento o nel file di intestazione appropriato. Se il CLSID non è disponibile pubblicamente, non è possibile creare direttamente l'oggetto.

La **funzione CoCreateInstance** ha cinque parametri. Per gli oggetti COM che verranno utilizzati con DirectX, è in genere possibile impostare i parametri come indicato di seguito.

*rclsid* Impostare questo valore sul CLSID dell'oggetto che si vuole creare.

*pUnkOuter* Impostare su `nullptr` . Questo parametro viene usato solo se si aggregano oggetti. Una descrizione dell'aggregazione COM non rientra nell'ambito di questo argomento.

*dwClsContext* Impostare su CLSCTX_INPROC_SERVER. Questa impostazione indica che l'oggetto viene implementato come DLL ed eseguito come parte del processo dell'applicazione.

*riid* Impostare sull'IID dell'interfaccia che si vuole restituire. La funzione creerà l'oggetto e restituirà il puntatore a interfaccia richiesto nel parametro ppv.

*ppv* Impostare questa proprietà sull'indirizzo di un puntatore che verrà impostato sull'interfaccia specificata da `riid` quando la funzione restituisce . Questa variabile deve essere dichiarata come puntatore all'interfaccia richiesta e il riferimento al puntatore nell'elenco di parametri deve essere eseguito come (LPVOID *).

La creazione indiretta di un oggetto è in genere molto più semplice, come illustrato nell'esempio di codice precedente. Passare al metodo di creazione dell'oggetto l'indirizzo di un puntatore a interfaccia, quindi il metodo crea l'oggetto e restituisce un puntatore a interfaccia. Quando si crea un oggetto indirettamente, anche se non è possibile scegliere l'interfaccia restituita dal metodo, spesso è comunque possibile specificare una serie di elementi relativi alla modalità di creazione dell'oggetto.

Ad esempio, è possibile passare a **D3D12CreateDevice** un valore che specifica il livello minimo di funzionalità D3D che il dispositivo restituito deve supportare, come illustrato nell'esempio di codice precedente.

## <a name="using-com-interfaces"></a>Uso delle interfacce COM

Quando si crea un oggetto COM, il metodo di creazione restituisce un puntatore a interfaccia. È quindi possibile usare tale puntatore per accedere a qualsiasi metodo dell'interfaccia. La sintassi è identica a quella usata con un puntatore a un metodo C++.

## <a name="requesting-additional-interfaces"></a>Richiesta di interfacce aggiuntive

In molti casi, il puntatore a interfaccia ricevuto dal metodo di creazione può essere l'unico necessario. In realtà, è relativamente comune per un oggetto esportare solo un'interfaccia diversa **da IUnknown**. Tuttavia, molti oggetti esportano più interfacce e potrebbero essere necessari puntatori a diverse di esse. Se sono necessarie più interfacce di quelle restituite dal metodo di creazione, non è necessario creare un nuovo oggetto. Richiedere invece un altro puntatore a interfaccia usando il metodo [**IUnknown::QueryInterface dell'oggetto**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)).

Se si crea l'oggetto con **CoCreateInstance,** è possibile richiedere un puntatore a interfaccia **IUnknown** e quindi chiamare **IUnknown::QueryInterface** per richiedere ogni interfaccia necessaria. Tuttavia, questo approccio è poco pratico se è necessaria una sola interfaccia e non funziona affatto se si usa un metodo di creazione di oggetti che non consente di specificare quale puntatore a interfaccia deve essere restituito. In pratica, in genere non è necessario ottenere un puntatore **IUnknown** esplicito, perché tutte le interfacce COM estendono **l'interfaccia IUnknown.**

L'estensione di un'interfaccia è concettualmente simile all'ereditarietà da una classe C++. L'interfaccia figlio espone tutti i metodi dell'interfaccia padre, oltre a uno o più dei propri metodi. In realtà, spesso si vede "eredita da" usato invece di "extends". È necessario ricordare che l'ereditarietà è interna all'oggetto. L'applicazione non può ereditare da o estendere l'interfaccia di un oggetto. Tuttavia, è possibile usare l'interfaccia figlio per chiamare uno dei metodi dell'elemento figlio o dell'elemento padre.

Poiché tutte le interfacce sono elementi figlio di **IUnknown**, è possibile chiamare **QueryInterface** su uno dei puntatori a interfaccia già disponibili per l'oggetto. In questo caso, è necessario specificare l'IID dell'interfaccia richiesta e l'indirizzo di un puntatore che conterrà il puntatore a interfaccia quando il metodo restituisce .

Ad esempio, il frammento di codice seguente chiama **IDXGIFactory2::CreateSwapChainForHwnd** per creare un oggetto della catena di scambio primario. Questo oggetto espone diverse interfacce. Il **metodo CreateSwapChainForHwnd** restituisce **un'interfaccia IDXGISwapChain1.** Il codice successivo usa quindi **l'interfaccia IDXGISwapChain1** per chiamare **QueryInterface** per richiedere **un'interfaccia IDXGISwapChain3.**

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
> In C++ è possibile usare la macro anziché l'IID esplicito e il ``IID_PPV_ARGS`` puntatore di cast: ``pDXGISwapChain1->QueryInterface(IID_PPV_ARGS(&pDXGISwapChain3));`` .
> Viene spesso usato per i metodi di creazione, nonché **per QueryInterface.** Per [altre informazioni, vedere combaseapi.h.](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)

## <a name="managing-a-com-objects-lifetime"></a>Gestione della durata di un oggetto COM

Quando viene creato un oggetto, il sistema alloca le risorse di memoria necessarie. Quando un oggetto non è più necessario, deve essere eliminato. Il sistema può usare tale memoria per altri scopi. Con gli oggetti C++ è possibile controllare la durata dell'oggetto direttamente con gli operatori e nei casi in cui si opera a tale livello o semplicemente usando la durata dello stack e `new` `delete` dell'ambito. COM non consente di creare o eliminare direttamente oggetti. Il motivo di questa progettazione è che lo stesso oggetto può essere usato da più parti dell'applicazione o, in alcuni casi, da più applicazioni. Se uno di questi riferimenti eliminasse l'oggetto, gli altri riferimenti diventeranno non validi. COM usa invece un sistema di conteggio dei riferimenti per controllare la durata di un oggetto.

Il conteggio dei riferimenti di un oggetto è il numero di volte in cui è stata richiesta una delle relative interfacce. Ogni volta che viene richiesta un'interfaccia, il conteggio dei riferimenti viene incrementato. Un'applicazione rilascia un'interfaccia quando tale interfaccia non è più necessaria, decrementando il conteggio dei riferimenti. Finché il conteggio dei riferimenti è maggiore di zero, l'oggetto rimane in memoria. Quando il conteggio dei riferimenti raggiunge lo zero, l'oggetto viene eliminato automaticamente. Non è necessario conoscere il conteggio dei riferimenti di un oggetto. Se si ottengono e rilasciano correttamente le interfacce di un oggetto, l'oggetto avrà la durata appropriata.

La corretta gestione del conteggio dei riferimenti è una parte fondamentale della programmazione COM. In caso negativo, è possibile creare facilmente una perdita di memoria o un arresto anomalo. Uno degli errori più comuni commersi dai programmatori COM è il mancato rilascio di un'interfaccia. In questo caso, il conteggio dei riferimenti non raggiunge mai zero e l'oggetto rimane in memoria per un periodo illimitato.

> [!NOTE]
> Direct3D 10 o versioni successive ha regole di durata leggermente modificate per gli oggetti. In particolare, gli oggetti derivati da **ID3DxxDeviceChild** non hanno mai una durata superiore al dispositivo padre, ovvero se il dispositivo **ID3DxxDevice** proprietario raggiunge un conteggio 0, anche tutti gli oggetti figlio non sono immediatamente validi. Inoltre, quando si usano i metodi **Set** per associare oggetti alla pipeline di rendering, questi riferimenti non aumentano il conteggio dei riferimenti, ovvero sono riferimenti deboli. In pratica, questa operazione viene gestita in modo ottimale assicurandosi di rilasciare completamente tutti gli oggetti figlio del dispositivo prima di rilasciare il dispositivo.

## <a name="incrementing-and-decrementing-the-reference-count"></a>Incremento e decremento del conteggio dei riferimenti

Ogni volta che si ottiene un nuovo puntatore a interfaccia, il conteggio dei riferimenti deve essere incrementato da una chiamata a [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref). Tuttavia, l'applicazione in genere non deve chiamare questo metodo. Se si ottiene un puntatore a interfaccia chiamando un metodo di creazione di oggetti o **chiamando IUnknown::QueryInterface,** l'oggetto incrementa automaticamente il conteggio dei riferimenti. Tuttavia, se si crea un puntatore a interfaccia in un altro modo, ad esempio copiando un puntatore esistente, è necessario chiamare in modo esplicito **IUnknown::AddRef**. In caso contrario, quando si rilascia il puntatore di interfaccia originale, l'oggetto potrebbe essere eliminato anche se potrebbe essere comunque necessario usare la copia del puntatore.

È necessario rilasciare tutti i puntatori a interfaccia, indipendentemente dal fatto che l'utente o l'oggetto incrementi il conteggio dei riferimenti. Quando non è più necessario un puntatore a interfaccia, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) per decrementare il conteggio dei riferimenti. Una procedura comune consiste nell'inizializzare tutti i puntatori di interfaccia a e quindi impostarli nuovamente `nullptr` su quando vengono `nullptr` rilasciati. Questa convenzione consente di testare tutti i puntatori a interfaccia nel codice di pulizia. Quelli che non sono ancora attivi ed è necessario rilasciarli `nullptr` prima di terminare l'applicazione.

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

Il codice finora ha chiamato in modo esplicito e per mantenere i conteggi ``Release`` dei riferimenti usando i metodi ``AddRef`` **IUnknown.** Questo modello richiede al programmatore di ricordarsi di mantenere correttamente il conteggio in tutti i possibili percorsi di codice. Ciò può comportare una gestione degli errori complessa e con la gestione delle eccezioni C++ abilitata può essere particolarmente difficile da implementare. Una soluzione migliore con C++ consiste nell'usare un [puntatore intelligente](/cpp/cpp/smart-pointers-modern-cpp).

* **winrt::com_ptr** è un puntatore intelligente fornito dalle proiezioni del linguaggio [C++/WinRT.](/uwp/cpp-ref-for-winrt/com-ptr) Questo è il puntatore intelligente COM consigliato da usare per le app UWP. Si noti che C++/WinRT richiede C++17.

* **Microsoft::WRL::ComPtr** è un puntatore intelligente fornito da [Windows runtime C++ Template Library (WRL).](/cpp/cppcx/wrl/comptr-class) Questa libreria è C++ "pura", quindi può essere utilizzata per le applicazioni Windows Runtime (tramite C++/CX o C++/WinRT) e per le applicazioni desktop Win32 classiche. Questo puntatore intelligente funziona anche nelle versioni precedenti di Windows che non supportano le API Windows Runtime. Per le applicazioni desktop Win32, è possibile usare per includere solo questa classe e, facoltativamente, definire anche il simbolo ``#include <wrl/client.h>`` del ``__WRL_CLASSIC_COM_STRICT__`` preprocessore. Per altre informazioni, vedere [Puntatori intelligenti COM rivisitato.](/archive/msdn-magazine/2015/february/windows-with-c-com-smart-pointers-revisited)

* **CComPtr** è un puntatore intelligente fornito [da Active Template Library (ATL).](/cpp/atl/reference/ccomptr-class) **Microsoft::WRL::ComPtr** è una versione più recente di questa implementazione che risolve una serie di piccoli problemi di utilizzo, quindi l'uso di questo puntatore intelligente non è consigliato per i nuovi progetti. Per altre informazioni, [vedere Come creare e usare CComPtr e CComQIPtr.](/cpp/cpp/how-to-create-and-use-ccomptr-and-ccomqiptr-instances)


## <a name="using-atl-with-directx-9"></a>Uso di ATL con DirectX 9

Per usare il Active Template Library (ATL) con DirectX 9, è necessario ridefinire le interfacce per la compatibilità ATL. In questo modo è possibile usare correttamente la **classe CComQIPtr** per ottenere un puntatore a un'interfaccia.

Se non si ridefiniranno le interfacce per ATL, verrà visualizzato il messaggio di errore seguente.

```
[...]\atlmfc\include\atlbase.h(4704) :   error C2787: 'IDirectXFileData' : no GUID has been associated with this object
```

L'esempio di codice seguente illustra come definire l'interfaccia IDirectXFileData.

```cpp
// Explicit declaration
struct __declspec(uuid("{3D82AB44-62DA-11CF-AB39-0020AF71E433}")) IDirectXFileData;

// Macro method
#define RT_IID(iid_, name_) struct __declspec(uuid(iid_)) name_
RT_IID("{1DD9E8DA-1C77-4D40-B0CF-98FEFDFF9512}", IDirectXFileData);
```

Dopo aver ridefinito l'interfaccia, è necessario usare il metodo **Attach** per associare l'interfaccia al puntatore di interfaccia restituito da **::D irect3DCreate9.** In caso contrario, **l'interfaccia IDirect3D9** non verrà rilasciata correttamente dalla classe del puntatore intelligente.

La **classe CComPtr** chiama internamente **IUnknown::AddRef** sul puntatore a interfaccia quando viene creato l'oggetto e quando viene assegnata un'interfaccia **alla classe CComPtr.** Per evitare la perdita del puntatore a interfaccia, non chiamare **IUnknown::AddRef sull'interfaccia restituita da **::D irect3DCreate9**.

Il codice seguente rilascia correttamente l'interfaccia senza **chiamare IUnknown::AddRef**.

```cpp
CComPtr<IDirect3D9> d3d;
d3d.Attach(::Direct3DCreate9(D3D_SDK_VERSION));
```

Usare il codice precedente. Non usare il codice seguente, che chiama **IUnknown::AddRef** seguito da **IUnknown::Release** e non rilascia il riferimento aggiunto da **::D irect3DCreate9.**

```cpp
CComPtr<IDirect3D9> d3d = ::Direct3DCreate9(D3D_SDK_VERSION);
```

Si noti che questa è l'unica posizione in Direct3D 9 in cui sarà necessario usare il **metodo Attach** in questo modo.

Per altre informazioni sulle classi **CComPTR** e **CComQIPtr,** vedere le relative definizioni nel `Atlbase.h` file di intestazione.
