---
title: Creazione di un oggetto in COM
description: Per usare un'interfaccia COM, il programma crea innanzitutto un'istanza di un oggetto che implementa tale interfaccia.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e15874e1d4dcb6bc29fad90f40f90b478c805ccc7b0d0085f560a8b56e2247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913767"
---
# <a name="creating-an-object-in-com"></a>Creazione di un oggetto in COM

Dopo che un thread ha inizializzato la libreria COM, è sicuro che il thread usi le interfacce COM. Per usare un'interfaccia COM, il programma crea innanzitutto un'istanza di un oggetto che implementa tale interfaccia.

In generale, esistono due modi per creare un oggetto COM:

-   Il modulo che implementa l'oggetto potrebbe fornire una funzione appositamente progettata per creare istanze di tale oggetto.
-   In alternativa, COM fornisce una funzione di creazione generica denominata [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

Ad esempio, prendere l'oggetto ipotetico `Shape` dall'argomento [Che cos'è un'interfaccia COM?](what-is-a-com-interface-.md). In questo esempio, `Shape` l'oggetto implementa un'interfaccia denominata `IDrawable` . La libreria grafica che implementa `Shape` l'oggetto potrebbe esportare una funzione con la firma seguente.


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



Data questa funzione, è possibile creare un nuovo `Shape` oggetto come indicato di seguito.


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



Il *parametro ppShape* è di tipo pointer-to-pointer-to-. `IDrawable` Se questo modello non è stato visto in precedenza, il riferimento indiretto doppio potrebbe risultare sconcertante.

Considerare i requisiti della `CreateShape` funzione. La funzione deve fornire un `IDrawable` puntatore al chiamante. Tuttavia, il valore restituito della funzione è già usato per il codice di errore/esito positivo. Pertanto, il puntatore deve essere restituito tramite un argomento alla funzione . Il chiamante passerà una variabile di tipo alla funzione e la funzione sovrascriverà `IDrawable*` questa variabile con un nuovo `IDrawable` puntatore. In C++ esistono solo due modi per una funzione di sovrascrivere un valore di parametro: passare per riferimento o passare per indirizzo. COM usa il secondo, pass-by-address. L'indirizzo di un puntatore è un puntatore a un puntatore, quindi il tipo di parametro deve essere `IDrawable**` .

Di seguito è riportato un diagramma che consente di visualizzare le attività in corso.

![Diagramma che mostra il riferimento indiretto a puntatore doppio](images/com03.png)

La `CreateShape` funzione usa l'indirizzo di *pShape* ( `&pShape` ) per scrivere un nuovo valore del puntatore in *pShape.*

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>CoCreateInstance: un modo generico per creare oggetti

La [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fornisce un meccanismo generico per la creazione di oggetti. Per comprendere **CoCreateInstance,** tenere presente che due oggetti COM possono implementare la stessa interfaccia e un oggetto può implementare due o più interfacce. Pertanto, una funzione generica che crea oggetti richiede due tipi di informazioni.

-   Oggetto da creare.
-   Interfaccia da ottenere dall'oggetto .

Ma come si indicano queste informazioni quando si chiama la funzione ? In COM un oggetto o un'interfaccia viene identificato assegnando all'oggetto un numero a 128 bit, denominato identificatore *univoco* globale (GUID). I GUID vengono generati in modo da essere univoci in modo efficace. I GUID sono una soluzione al problema della creazione di identificatori univoci senza un'autorità di registrazione centrale. I GUID sono talvolta *denominati identificatori univoci universali* (UUID). Prima di COM, venivano usati in DCE/RPC (Distributed Computing Environment/Remote Procedure Call). Esistono diversi algoritmi per la creazione di nuovi GUID. Non tutti questi algoritmi garantiscono rigorosamente l'univocità, ma la probabilità di creare accidentalmente lo stesso valore GUID due volte è estremamente piccola, ovvero zero. I GUID possono essere usati per identificare qualsiasi tipo di entità, non solo oggetti e interfacce. Tuttavia, questo è l'unico uso che ci riguarda in questo modulo.

Ad esempio, la `Shapes` libreria potrebbe dichiarare due costanti GUID:


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



Si può presupporre che i valori numerici effettivi a 128 bit per queste costanti siano definiti altrove. La costante **CLSID \_ Shape identifica** l'oggetto, `Shape` mentre la costante **IID \_ IDrawable** identifica l'interfaccia. `IDrawable` Il prefisso "CLSID" è l'acronimo di *identificatore di* classe e il prefisso *IID* è l'identificatore *di interfaccia*. Si tratta di convenzioni di denominazione standard in COM.

Dati questi valori, si creerà una nuova `Shape` istanza come indicato di seguito:


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



La [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha cinque parametri. Il primo e il quarto parametro sono l'identificatore di classe e l'identificatore di interfaccia. In effetti, questi parametri forniscono alla funzione "Crea l'oggetto Shape e assegnami un puntatore all'interfaccia IDrawable".

Impostare il secondo parametro su **NULL.** Per altre informazioni sul significato di questo parametro, vedere l'argomento [Aggregazione](/windows/desktop/com/aggregation) nella documentazione COM. Il terzo parametro accetta un set di flag il cui scopo principale è specificare il *contesto di esecuzione* per l'oggetto. Il contesto di esecuzione specifica se l'oggetto viene eseguito nello stesso processo dell'applicazione. in un processo diverso nello stesso computer; o in un computer remoto. Nella tabella seguente vengono illustrati i valori più comuni per questo parametro.



| Flag                       | Descrizione                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSCTX \_ INPROC \_ SERVER** | Stesso processo.                                                                                                                                                      |
| **CLSCTX \_ LOCAL \_ SERVER**  | Processo diverso, stesso computer.                                                                                                                                  |
| **CLSCTX \_ REMOTE \_ SERVER** | Computer diverso.                                                                                                                                                |
| **CLSCTX \_ ALL**            | Usare l'opzione più efficiente che l'oggetto supporta. La classificazione, dalla più efficiente alla meno efficiente, è: in-process, out-of-process e cross-computer. |



 

La documentazione per un determinato componente potrebbe indicare il contesto di esecuzione che l'oggetto supporta. In caso contrario, usare **CLSCTX \_ ALL.** Se si richiede un contesto di esecuzione che l'oggetto non supporta, la [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) restituisce il codice di errore **REGDB \_ E \_ CLASSNOTREG**. Questo codice di errore può anche indicare che il CLSID non corrisponde ad alcun componente registrato nel computer dell'utente.

Il quinto parametro di [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) riceve un puntatore all'interfaccia . Poiché **CoCreateInstance è** un meccanismo generico, questo parametro non può essere fortemente tipizzato. Il tipo di dati è **invece void \* \*** e il chiamante deve forzare l'indirizzo del puntatore a un tipo **void. \* \*** Questo è lo scopo del **\_ cast reinterpretato** nell'esempio precedente.

È fondamentale controllare il valore restituito di [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Se la funzione restituisce un codice di errore, il puntatore a interfaccia COM non è valido e il tentativo di dereferenziarlo può causare l'arresto anomalo del programma.

Internamente, la [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa varie tecniche per creare un oggetto. Nel caso più semplice, cerca l'identificatore di classe nel Registro di sistema. La voce del Registro di sistema punta a una DLL o a un file EXE che implementa l'oggetto . **CoCreateInstance** può anche usare le informazioni di un catalogo COM+ o di un manifesto side-by-side (SxS). Indipendentemente dal fatto che i dettagli siano trasparenti per il chiamante. Per altre informazioni sui dettagli interni di **CoCreateInstance,** vedere [Client e server COM.](/windows/desktop/com/com-clients-and-servers)

L'esempio che è stato utilizzato è piuttosto complicato, quindi ora si passi a un esempio reale di COM in azione: la visualizzazione della finestra di dialogo Apri per consentire all'utente di selezionare un `Shapes` file. 

## <a name="next"></a>Prossima

[Esempio: finestra di dialogo Apri](example--the-open-dialog-box.md)

 

 