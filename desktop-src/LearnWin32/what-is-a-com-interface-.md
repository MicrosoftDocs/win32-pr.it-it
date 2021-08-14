---
title: Che cos'è un'interfaccia COM
description: Che cos'è un'interfaccia COM
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a6eac63fb6395e04f36c89826a392046c906a70105e19bb6b9514975d89197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387606"
---
# <a name="what-is-a-com-interface"></a>Che cos'è un'interfaccia COM?

Se si conosce C# o Java, le interfacce devono essere un concetto familiare. *Un'interfaccia* definisce un set di metodi che un oggetto può supportare, senza dettare nulla sull'implementazione. L'interfaccia contrassegna un limite chiaro tra il codice che chiama un metodo e il codice che implementa il metodo . In termini di informatica, il chiamante è *disaccoccodato* dall'implementazione.

![illustrazione che mostra il limite dell'interfaccia tra un oggetto e un'applicazione](images/com01.png)

In C++ l'equivalente più vicino a un'interfaccia è una classe virtuale pura, ovvero una classe che contiene solo metodi virtuali puri e nessun altro membro. Ecco un esempio ipotetico di un'interfaccia:

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

L'idea di questo esempio è che un set di oggetti in alcune librerie grafiche sia disegnabile. `IDrawable`L'interfaccia definisce le operazioni che qualsiasi oggetto drawable deve supportare. Per convenzione, i nomi delle interfacce iniziano con "I". In questo esempio `IDrawable` l'interfaccia definisce una singola operazione: `Draw` .

Tutte le interfacce sono *astratte,* pertanto un programma non è stato in grado di creare un'istanza di `IDrawable` un oggetto come tale. Ad esempio, il codice seguente non viene compilato.

```C++
IDrawable draw;
draw.Draw();
```

La libreria grafica fornisce invece oggetti che *implementano l'interfaccia* `IDrawable` . Ad esempio, la libreria potrebbe fornire un oggetto forma per il disegno di forme e un oggetto bitmap per il disegno di immagini. In C++ questa operazione viene eseguita ereditando da una classe di base astratta comune:

```C++
class Shape : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};

class Bitmap : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};
```

Le `Shape` classi e definiscono due tipi distinti di oggetto `Bitmap` drawable. Ogni classe eredita da `IDrawable` e fornisce la propria implementazione del metodo `Draw` . Naturalmente, le due implementazioni potrebbero differire notevolmente. Ad esempio, il `Shape::Draw` metodo potrebbe rasterizzare un set di righe, mentre sarebbe `Bitmap::Draw` b blit una matrice di pixel.

Un programma che usa questa libreria grafica manipola gli oggetti e tramite i `Shape` puntatori, anziché usare direttamente i `Bitmap` `IDrawable` `Shape` `Bitmap` puntatori o .

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

Di seguito è riportato un esempio che esegue il ciclo su una matrice `IDrawable` di puntatori. La matrice può contenere un'ampia gamma eterogenea di forme, bitmap e altri oggetti grafici, purché ogni oggetto nella matrice erediti `IDrawable` .

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

Un punto chiave di COM è che il codice chiamante non vede mai il tipo della classe derivata. In altre parole, non si dichiara mai una variabile di `Shape` tipo o `Bitmap` nel codice. Tutte le operazioni su forme e bitmap vengono eseguite usando `IDrawable` i puntatori. In questo modo, COM mantiene una netta separazione tra interfaccia e implementazione. I dettagli di implementazione delle classi e possono cambiare, ad esempio per correggere bug o aggiungere nuove funzionalità, senza apportare `Shape` `Bitmap` modifiche al codice chiamante.

In un'implementazione C++ le interfacce vengono dichiarate usando una classe o una struttura.

> [!Note]  
> Gli esempi di codice in questo argomento hanno lo scopo di illustrare i concetti generali, non la pratica reale. La definizione di nuove interfacce COM non è nell'ambito di questa serie, ma non è necessario definire un'interfaccia direttamente in un file di intestazione. Al contrario, un'interfaccia COM viene definita usando un linguaggio denominato Interface Definition Language (IDL). Il file IDL viene elaborato da un compilatore IDL che genera un file di intestazione C++.

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

Quando si utilizza COM, è importante ricordare che le interfacce non sono oggetti. Si tratta di raccolte di metodi che gli oggetti devono implementare. Diversi oggetti possono implementare la stessa interfaccia, come illustrato con `Shape` gli esempi `Bitmap` e . Inoltre, un oggetto può implementare diverse interfacce. Ad esempio, la libreria grafica potrebbe definire un'interfaccia denominata `ISerializable` che supporta il salvataggio e il caricamento di oggetti grafici. Si considerino ora le dichiarazioni di classe seguenti:

```C++
// An interface for serialization.
class ISerializable
{
public:
    virtual void Load(PCWSTR filename) = 0;    // Load from file.
    virtual void Save(PCWSTR filename) = 0;    // Save to file.
};

// Declarations of drawable object types.

class Shape : public IDrawable
{
    ...
};

class Bitmap : public IDrawable, public ISerializable
{
    ...
};
```

In questo esempio la `Bitmap` classe implementa `ISerializable` . Il programma può usare questo metodo per salvare o caricare la bitmap. Tuttavia, la `Shape` classe non implementa , pertanto non espone tale `ISerializable` funzionalità. Il diagramma seguente illustra le relazioni di ereditarietà in questo esempio.

![illustrazione che mostra l'ereditarietà dell'interfaccia, con le classi shape e bitmap che puntano a idrawable, ma solo bitmap che punta a iserializable](images/com02.png)

In questa sezione è stata esaminata la base concettuale delle interfacce, ma finora non è stato visto il codice COM effettivo. Si inizierà con la prima operazione che qualsiasi applicazione COM deve eseguire: inizializzare la libreria COM.

## <a name="next"></a>Prossima

[Inizializzazione della libreria COM](initializing-the-com-library.md)