---
title: Che cos'è un'interfaccia COM
description: Che cos'è un'interfaccia COM
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da703569beae7a9aa2fc41bcea0214cc9aa488ad
ms.sourcegitcommit: 8eac40ea4d87a85e036ed5bbffec7b7a3dab39ec
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/04/2019
ms.locfileid: "104397023"
---
# <a name="what-is-a-com-interface"></a>Che cos'è un'interfaccia COM?

Se si conosce C# o Java, le interfacce devono essere un concetto familiare. Un' *interfaccia* definisce un set di metodi che possono essere supportati da un oggetto, senza che venga dettata alcuna parte dell'implementazione. L'interfaccia contrassegna un limite chiaro tra il codice che chiama un metodo e il codice che implementa il metodo. In termini di informatica, il chiamante viene *separato* dall'implementazione di.

![illustrazione che mostra il limite dell'interfaccia tra un oggetto e un'applicazione](images/com01.png)

In C++, l'equivalente più vicino a un'interfaccia è una classe virtuale pura, ovvero una classe che contiene solo metodi virtuali puri e nessun altro membro. Di seguito è riportato un esempio ipotetico di un'interfaccia:

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

L'idea di questo esempio è che un set di oggetti in una raccolta grafica è disegnato. L' `IDrawable` interfaccia definisce le operazioni che qualsiasi oggetto disegnatore deve supportare. (Per convenzione, i nomi di interfaccia iniziano con "I"). In questo esempio, l' `IDrawable` interfaccia definisce una singola operazione: `Draw` .

Tutte le interfacce sono *astratte*, quindi un programma non è stato in grado di creare un'istanza di un `IDrawable` oggetto. Il codice seguente, ad esempio, non verrà compilato.

```C++
IDrawable draw;
draw.Draw();
```

La libreria grafica fornisce invece oggetti che *implementano* l' `IDrawable` interfaccia. È ad esempio possibile che la libreria fornisca un oggetto Shape per disegnare forme e un oggetto bitmap per il disegno di immagini. In C++ questa operazione viene eseguita ereditando da una classe base astratta comune:

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

Le `Shape` `Bitmap` classi e definiscono due tipi distinti di oggetto disegnatore. Ogni classe eredita da `IDrawable` e fornisce la propria implementazione del `Draw` metodo. Naturalmente, le due implementazioni potrebbero differire considerevolmente. Ad esempio, il `Shape::Draw` metodo può rasterizzare un set di righe, mentre `Bitmap::Draw` blit una matrice di pixel.

Un programma che usa questa libreria grafica gestirebbe `Shape` `Bitmap` oggetti e tramite `IDrawable` puntatori, anziché usare `Shape` direttamente i `Bitmap` puntatori o.

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

Di seguito è riportato un esempio che esegue il ciclo su una matrice di `IDrawable` puntatori. La matrice potrebbe contenere un insieme eterogeneo di forme, bitmap e altri oggetti grafici, a condizione che ogni oggetto nella matrice erediti `IDrawable` .

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

Un punto chiave di COM è che il codice chiamante non vede mai il tipo della classe derivata. In altre parole, non si dichiarerà mai una variabile di tipo `Shape` o `Bitmap` nel codice. Tutte le operazioni sulle forme e le bitmap vengono eseguite utilizzando i `IDrawable` puntatori. In questo modo, COM mantiene una stretta separazione tra l'interfaccia e l'implementazione. I dettagli di implementazione delle `Shape` `Bitmap` classi e possono cambiare, ad esempio per correggere i bug o aggiungere nuove funzionalità, senza apportare modifiche al codice chiamante.

In un'implementazione C++, le interfacce vengono dichiarate usando una classe o una struttura.

> [!Note]  
> Gli esempi di codice in questo argomento hanno lo scopo di fornire concetti generali, non procedure reali. La definizione di nuove interfacce COM esula dall'ambito di questa serie, ma non si definisce un'interfaccia direttamente in un file di intestazione. Un'interfaccia COM viene invece definita utilizzando un linguaggio denominato IDL (Interface Definition Language). Il file IDL viene elaborato da un compilatore IDL, che genera un file di intestazione C++.

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

Quando si utilizza COM, è importante ricordare che le interfacce non sono oggetti. Sono raccolte di metodi che devono essere implementati dagli oggetti. Diversi oggetti possono implementare la stessa interfaccia, come illustrato con gli `Shape` `Bitmap` esempi e. Inoltre, un oggetto può implementare più interfacce. Ad esempio, la libreria grafica potrebbe definire un'interfaccia denominata `ISerializable` che supporta il salvataggio e il caricamento di oggetti grafici. Si considerino ora le dichiarazioni di classe seguenti:

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

In questo esempio, la `Bitmap` classe implementa `ISerializable` . Il programma può utilizzare questo metodo per salvare o caricare la bitmap. Tuttavia, la `Shape` classe non implementa `ISerializable` , quindi non espone tale funzionalità. Nel diagramma seguente vengono illustrate le relazioni di ereditarietà in questo esempio.

![illustrazione che mostra l'ereditarietà dell'interfaccia, con le classi Shape e bitmap che puntano a IDrawable, ma solo bitmap che punta a ISerializable](images/com02.png)

In questa sezione è stata esaminata la base concettuale delle interfacce, ma finora non è stato visto il codice COM effettivo. Si inizierà con la prima cosa che qualsiasi applicazione COM deve eseguire: inizializzare la libreria COM.

## <a name="next"></a>Prossima

[Inizializzazione della libreria COM](initializing-the-com-library.md)