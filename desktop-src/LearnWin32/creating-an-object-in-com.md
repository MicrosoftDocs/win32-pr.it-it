---
title: Creazione di un oggetto in COM
description: Per usare un'interfaccia COM, il programma crea prima un'istanza di un oggetto che implementa tale interfaccia.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398935"
---
# <a name="creating-an-object-in-com"></a>Creazione di un oggetto in COM

Dopo l'inizializzazione della libreria COM da parte di un thread, è possibile che il thread utilizzi le interfacce COM in modo sicuro. Per usare un'interfaccia COM, il programma crea prima un'istanza di un oggetto che implementa tale interfaccia.

In generale, esistono due modi per creare un oggetto COM:

-   Il modulo che implementa l'oggetto potrebbe fornire una funzione progettata in modo specifico per creare istanze di tale oggetto.
-   In alternativa, COM fornisce una funzione di creazione generica denominata [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Ad esempio, prendere l'oggetto ipotetico `Shape` dall'argomento [che cos'è un'interfaccia com?](what-is-a-com-interface-.md). In questo esempio, l' `Shape` oggetto implementa un'interfaccia denominata `IDrawable` . La libreria grafica che implementa l' `Shape` oggetto potrebbe esportare una funzione con la firma seguente.


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



Il parametro *ppShape* è di tipo puntatore a puntatore a `IDrawable` . Se questo modello non è stato visto in precedenza, il doppio riferimento indiretto può essere sconcertante.

Considerare i requisiti della `CreateShape` funzione. La funzione deve restituire un `IDrawable` puntatore al chiamante. Tuttavia, il valore restituito della funzione è già usato per il codice di errore o di esito positivo. Pertanto, il puntatore deve essere restituito tramite un argomento alla funzione. Il chiamante passerà una variabile di tipo `IDrawable*` alla funzione e la funzione sovrascriverà questa variabile con un nuovo `IDrawable` puntatore. In C++ sono disponibili solo due modi per la sovrascrittura di un valore di parametro da una funzione: passa per riferimento o passa per indirizzo. COM utilizza la seconda opzione, pass-by-Address. E l'indirizzo di un puntatore è un puntatore a puntatore, quindi il tipo di parametro deve essere `IDrawable**` .

Ecco un diagramma che consente di visualizzare gli elementi in corso.

![diagramma che mostra un riferimento indiretto a doppio puntatore](images/com03.png)

La `CreateShape` funzione usa l'indirizzo di *pShape* ( `&pShape` ) per scrivere un nuovo valore del puntatore in *pShape*.

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>CoCreateInstance: metodo generico per la creazione di oggetti

La funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fornisce un meccanismo generico per la creazione di oggetti. Per comprendere **CoCreateInstance**, tenere presente che due oggetti com possono implementare la stessa interfaccia e un oggetto può implementare due o più interfacce. Pertanto, una funzione generica che crea oggetti richiede due tipi di informazioni.

-   Oggetto da creare.
-   Interfaccia da ottenere dall'oggetto.

Ma come è possibile indicare queste informazioni quando si chiama la funzione? In COM, un oggetto o un'interfaccia viene identificato tramite l'assegnazione di un numero a 128 bit, denominato *identificatore univoco globale* (Guid). I GUID vengono generati in modo da renderli effettivamente univoci. I GUID rappresentano una soluzione al problema di come creare identificatori univoci senza un'autorità di registrazione centrale. I GUID sono talvolta denominati *identificatori universalmente univoci* (UUID). Prima di COM, venivano usati in DCE/RPC (Distributed Computing Environment/Remote Procedure Call). Sono disponibili diversi algoritmi per la creazione di nuovi GUID. Non tutti questi algoritmi assicurano esclusivamente l'univocità, ma la probabilità di creare accidentalmente lo stesso valore GUID è molto ridotta, in effetti zero. I GUID possono essere usati per identificare qualsiasi tipo di entità, non solo per oggetti e interfacce. Tuttavia, questo è l'unico utilizzo che ci interessa in questo modulo.

Ad esempio, la `Shapes` libreria può dichiarare due costanti GUID:


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



Si può presupporre che i valori numerici a 128 bit effettivi per queste costanti siano definiti altrove. La **\_ forma** di costante CLSID identifica l' `Shape` oggetto, mentre la costante **IID \_ IDrawable** identifica l' `IDrawable` interfaccia. Il prefisso "CLSID" sta per l' *identificatore di classe* e l' *IID* di prefisso sta per l'identificatore di *interfaccia*. Si tratta di convenzioni di denominazione standard in COM.

Dato questi valori, è necessario creare una nuova `Shape` istanza nel modo seguente:


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



La funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha cinque parametri. Il primo e il quarto parametro sono l'identificatore di classe e l'identificatore di interfaccia. Questi parametri indicano in effetti che la funzione "crea l'oggetto forma e fornisce un puntatore all'interfaccia IDrawable".

Impostare il secondo parametro su **null**. Per ulteriori informazioni sul significato di questo parametro, vedere l'argomento [aggregazione](/windows/desktop/com/aggregation) nella documentazione com. Il terzo parametro accetta un set di flag il cui scopo principale è quello di specificare il *contesto di esecuzione* per l'oggetto. Il contesto di esecuzione specifica se l'oggetto viene eseguito nello stesso processo dell'applicazione; in un processo diverso nello stesso computer; o in un computer remoto. La tabella seguente mostra i valori più comuni per questo parametro.



| Flag                       | Descrizione                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_server inproc \_ CLSCTX** | Stesso processo.                                                                                                                                                      |
| **\_server locale \_ CLSCTX**  | Processo diverso, stesso computer.                                                                                                                                  |
| **\_server remoto \_ CLSCTX** | Computer diverso.                                                                                                                                                |
| **CLSCTX \_ tutto**            | Utilizzare l'opzione più efficiente supportata dall'oggetto. (La classificazione, dal più efficiente al meno efficiente, è: in-process, out-of-process e tra computer). |



 

La documentazione relativa a un particolare componente potrebbe indicare il contesto di esecuzione supportato dall'oggetto. In caso contrario, utilizzare **CLSCTX \_ All**. Se si richiede un contesto di esecuzione non supportato dall'oggetto, la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) restituisce il codice di errore **REGDB \_ E \_ CLASSNOTREG**. Questo codice di errore può anche indicare che il CLSID non corrisponde ad alcun componente registrato nel computer dell'utente.

Il quinto parametro per [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) riceve un puntatore all'interfaccia. Poiché **CoCreateInstance** è un meccanismo generico, questo parametro non può essere fortemente tipizzato. Il tipo di dati è invece **void \* \*** e il chiamante deve forzare l'indirizzo del puntatore a un tipo **void \* \*** . Questo è lo scopo del **\_ cast di reinterpretazione** nell'esempio precedente.

È fondamentale controllare il valore restituito di [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Se la funzione restituisce un codice di errore, il puntatore all'interfaccia COM non è valido e il tentativo di dereferenziarlo può causare l'arresto anomalo del programma.

Internamente, la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilizza varie tecniche per creare un oggetto. Nel caso più semplice, Cerca l'identificatore di classe nel registro di sistema. La voce del registro di sistema punta a una DLL o a un file EXE che implementa l'oggetto. **CoCreateInstance** può inoltre utilizzare le informazioni di un catalogo com+ o di un manifesto side-by-Side (SxS). Indipendentemente, i dettagli sono trasparenti per il chiamante. Per ulteriori informazioni sui dettagli interni di **CoCreateInstance**, vedere [client e server com](/windows/desktop/com/com-clients-and-servers).

L' `Shapes` esempio usato è stato escogitato in qualche modo, ora passiamo a un esempio reale di com in azione: la visualizzazione della finestra di dialogo **Apri** in cui l'utente può selezionare un file.

## <a name="next"></a>Prossima

[Esempio: finestra di dialogo Apri](example--the-open-dialog-box.md)

 

 