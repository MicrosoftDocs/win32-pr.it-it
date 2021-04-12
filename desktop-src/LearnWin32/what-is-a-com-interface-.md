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
# <a name="what-is-a-com-interface"></a><span data-ttu-id="2ce50-103">Che cos'è un'interfaccia COM?</span><span class="sxs-lookup"><span data-stu-id="2ce50-103">What Is a COM Interface?</span></span>

<span data-ttu-id="2ce50-104">Se si conosce C# o Java, le interfacce devono essere un concetto familiare.</span><span class="sxs-lookup"><span data-stu-id="2ce50-104">If you know C# or Java, interfaces should be a familiar concept.</span></span> <span data-ttu-id="2ce50-105">Un' *interfaccia* definisce un set di metodi che possono essere supportati da un oggetto, senza che venga dettata alcuna parte dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2ce50-105">An *interface* defines a set of methods that an object can support, without dictating anything about the implementation.</span></span> <span data-ttu-id="2ce50-106">L'interfaccia contrassegna un limite chiaro tra il codice che chiama un metodo e il codice che implementa il metodo.</span><span class="sxs-lookup"><span data-stu-id="2ce50-106">The interface marks a clear boundary between code that calls a method and the code that implements the method.</span></span> <span data-ttu-id="2ce50-107">In termini di informatica, il chiamante viene *separato* dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="2ce50-107">In computer science terms, the caller is *decoupled* from the implementation.</span></span>

![illustrazione che mostra il limite dell'interfaccia tra un oggetto e un'applicazione](images/com01.png)

<span data-ttu-id="2ce50-109">In C++, l'equivalente più vicino a un'interfaccia è una classe virtuale pura, ovvero una classe che contiene solo metodi virtuali puri e nessun altro membro.</span><span class="sxs-lookup"><span data-stu-id="2ce50-109">In C++, the nearest equivalent to an interface is a pure virtual class—that is, a class that contains only pure virtual methods and no other members.</span></span> <span data-ttu-id="2ce50-110">Di seguito è riportato un esempio ipotetico di un'interfaccia:</span><span class="sxs-lookup"><span data-stu-id="2ce50-110">Here is a hypothetical example of an interface:</span></span>

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

<span data-ttu-id="2ce50-111">L'idea di questo esempio è che un set di oggetti in una raccolta grafica è disegnato.</span><span class="sxs-lookup"><span data-stu-id="2ce50-111">The idea of this example is that a set of objects in some graphics library are drawable.</span></span> <span data-ttu-id="2ce50-112">L' `IDrawable` interfaccia definisce le operazioni che qualsiasi oggetto disegnatore deve supportare.</span><span class="sxs-lookup"><span data-stu-id="2ce50-112">The `IDrawable` interface defines the operations that any drawable object must support.</span></span> <span data-ttu-id="2ce50-113">(Per convenzione, i nomi di interfaccia iniziano con "I"). In questo esempio, l' `IDrawable` interfaccia definisce una singola operazione: `Draw` .</span><span class="sxs-lookup"><span data-stu-id="2ce50-113">(By convention, interface names start with "I".) In this example, the `IDrawable` interface defines a single operation: `Draw`.</span></span>

<span data-ttu-id="2ce50-114">Tutte le interfacce sono *astratte*, quindi un programma non è stato in grado di creare un'istanza di un `IDrawable` oggetto.</span><span class="sxs-lookup"><span data-stu-id="2ce50-114">All interfaces are *abstract*, so a program could not create an instance of an `IDrawable` object as such.</span></span> <span data-ttu-id="2ce50-115">Il codice seguente, ad esempio, non verrà compilato.</span><span class="sxs-lookup"><span data-stu-id="2ce50-115">For example, the following code would not compile.</span></span>

```C++
IDrawable draw;
draw.Draw();
```

<span data-ttu-id="2ce50-116">La libreria grafica fornisce invece oggetti che *implementano* l' `IDrawable` interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2ce50-116">Instead, the graphics library provides objects that *implement* the `IDrawable` interface.</span></span> <span data-ttu-id="2ce50-117">È ad esempio possibile che la libreria fornisca un oggetto Shape per disegnare forme e un oggetto bitmap per il disegno di immagini.</span><span class="sxs-lookup"><span data-stu-id="2ce50-117">For example, the library might provide a shape object for drawing shapes and a bitmap object for drawing images.</span></span> <span data-ttu-id="2ce50-118">In C++ questa operazione viene eseguita ereditando da una classe base astratta comune:</span><span class="sxs-lookup"><span data-stu-id="2ce50-118">In C++, this is done by inheriting from a common abstract base class:</span></span>

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

<span data-ttu-id="2ce50-119">Le `Shape` `Bitmap` classi e definiscono due tipi distinti di oggetto disegnatore.</span><span class="sxs-lookup"><span data-stu-id="2ce50-119">The `Shape` and `Bitmap` classes define two distinct types of drawable object.</span></span> <span data-ttu-id="2ce50-120">Ogni classe eredita da `IDrawable` e fornisce la propria implementazione del `Draw` metodo.</span><span class="sxs-lookup"><span data-stu-id="2ce50-120">Each class inherits from `IDrawable` and provides its own implementation of the `Draw` method.</span></span> <span data-ttu-id="2ce50-121">Naturalmente, le due implementazioni potrebbero differire considerevolmente.</span><span class="sxs-lookup"><span data-stu-id="2ce50-121">Naturally, the two implementations might differ considerably.</span></span> <span data-ttu-id="2ce50-122">Ad esempio, il `Shape::Draw` metodo può rasterizzare un set di righe, mentre `Bitmap::Draw` blit una matrice di pixel.</span><span class="sxs-lookup"><span data-stu-id="2ce50-122">For example, the `Shape::Draw` method might rasterize a set of lines, while `Bitmap::Draw` would blit an array of pixels.</span></span>

<span data-ttu-id="2ce50-123">Un programma che usa questa libreria grafica gestirebbe `Shape` `Bitmap` oggetti e tramite `IDrawable` puntatori, anziché usare `Shape` direttamente i `Bitmap` puntatori o.</span><span class="sxs-lookup"><span data-stu-id="2ce50-123">A program using this graphics library would manipulate `Shape` and `Bitmap` objects through `IDrawable` pointers, rather than using `Shape` or `Bitmap` pointers directly.</span></span>

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

<span data-ttu-id="2ce50-124">Di seguito è riportato un esempio che esegue il ciclo su una matrice di `IDrawable` puntatori.</span><span class="sxs-lookup"><span data-stu-id="2ce50-124">Here is an example that loops over an array of `IDrawable` pointers.</span></span> <span data-ttu-id="2ce50-125">La matrice potrebbe contenere un insieme eterogeneo di forme, bitmap e altri oggetti grafici, a condizione che ogni oggetto nella matrice erediti `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="2ce50-125">The array might contain a heterogeneous assortment of shapes, bitmaps, and other graphics objects, as long as each object in the array inherits `IDrawable`.</span></span>

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

<span data-ttu-id="2ce50-126">Un punto chiave di COM è che il codice chiamante non vede mai il tipo della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="2ce50-126">A key point about COM is that the calling code never sees the type of the derived class.</span></span> <span data-ttu-id="2ce50-127">In altre parole, non si dichiarerà mai una variabile di tipo `Shape` o `Bitmap` nel codice.</span><span class="sxs-lookup"><span data-stu-id="2ce50-127">In other words, you would never declare a variable of type `Shape` or `Bitmap` in your code.</span></span> <span data-ttu-id="2ce50-128">Tutte le operazioni sulle forme e le bitmap vengono eseguite utilizzando i `IDrawable` puntatori.</span><span class="sxs-lookup"><span data-stu-id="2ce50-128">All operations on shapes and bitmaps are performed using `IDrawable` pointers.</span></span> <span data-ttu-id="2ce50-129">In questo modo, COM mantiene una stretta separazione tra l'interfaccia e l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2ce50-129">In this way, COM maintains a strict separation between interface and implementation.</span></span> <span data-ttu-id="2ce50-130">I dettagli di implementazione delle `Shape` `Bitmap` classi e possono cambiare, ad esempio per correggere i bug o aggiungere nuove funzionalità, senza apportare modifiche al codice chiamante.</span><span class="sxs-lookup"><span data-stu-id="2ce50-130">The implementation details of the `Shape` and `Bitmap` classes can change—for example, to fix bugs or add new capabilities—with no changes to the calling code.</span></span>

<span data-ttu-id="2ce50-131">In un'implementazione C++, le interfacce vengono dichiarate usando una classe o una struttura.</span><span class="sxs-lookup"><span data-stu-id="2ce50-131">In a C++ implementation, interfaces are declared using a class or structure.</span></span>

> [!Note]  
> <span data-ttu-id="2ce50-132">Gli esempi di codice in questo argomento hanno lo scopo di fornire concetti generali, non procedure reali.</span><span class="sxs-lookup"><span data-stu-id="2ce50-132">The code examples in this topic are meant to convey general concepts, not real-world practice.</span></span> <span data-ttu-id="2ce50-133">La definizione di nuove interfacce COM esula dall'ambito di questa serie, ma non si definisce un'interfaccia direttamente in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="2ce50-133">Defining new COM interfaces is beyond the scope of this series, but you would not define an interface directly in a header file.</span></span> <span data-ttu-id="2ce50-134">Un'interfaccia COM viene invece definita utilizzando un linguaggio denominato IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="2ce50-134">Instead, a COM interface is defined using a language called Interface Definition Language (IDL).</span></span> <span data-ttu-id="2ce50-135">Il file IDL viene elaborato da un compilatore IDL, che genera un file di intestazione C++.</span><span class="sxs-lookup"><span data-stu-id="2ce50-135">The IDL file is processed by an IDL compiler, which generates a C++ header file.</span></span>

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

<span data-ttu-id="2ce50-136">Quando si utilizza COM, è importante ricordare che le interfacce non sono oggetti.</span><span class="sxs-lookup"><span data-stu-id="2ce50-136">When you work with COM, it is important to remember that interfaces are not objects.</span></span> <span data-ttu-id="2ce50-137">Sono raccolte di metodi che devono essere implementati dagli oggetti.</span><span class="sxs-lookup"><span data-stu-id="2ce50-137">They are collections of methods that objects must implement.</span></span> <span data-ttu-id="2ce50-138">Diversi oggetti possono implementare la stessa interfaccia, come illustrato con gli `Shape` `Bitmap` esempi e.</span><span class="sxs-lookup"><span data-stu-id="2ce50-138">Several objects can implement the same interface, as shown with the `Shape` and `Bitmap` examples.</span></span> <span data-ttu-id="2ce50-139">Inoltre, un oggetto può implementare più interfacce.</span><span class="sxs-lookup"><span data-stu-id="2ce50-139">Moreover, one object can implement several interfaces.</span></span> <span data-ttu-id="2ce50-140">Ad esempio, la libreria grafica potrebbe definire un'interfaccia denominata `ISerializable` che supporta il salvataggio e il caricamento di oggetti grafici.</span><span class="sxs-lookup"><span data-stu-id="2ce50-140">For example, the graphics library might define an interface named `ISerializable` that supports saving and loading graphics objects.</span></span> <span data-ttu-id="2ce50-141">Si considerino ora le dichiarazioni di classe seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ce50-141">Now consider the following class declarations:</span></span>

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

<span data-ttu-id="2ce50-142">In questo esempio, la `Bitmap` classe implementa `ISerializable` .</span><span class="sxs-lookup"><span data-stu-id="2ce50-142">In this example, the `Bitmap` class implements `ISerializable`.</span></span> <span data-ttu-id="2ce50-143">Il programma può utilizzare questo metodo per salvare o caricare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="2ce50-143">The program could use this method to save or load the bitmap.</span></span> <span data-ttu-id="2ce50-144">Tuttavia, la `Shape` classe non implementa `ISerializable` , quindi non espone tale funzionalità.</span><span class="sxs-lookup"><span data-stu-id="2ce50-144">However, the `Shape` class does not implement `ISerializable`, so it does not expose that functionality.</span></span> <span data-ttu-id="2ce50-145">Nel diagramma seguente vengono illustrate le relazioni di ereditarietà in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="2ce50-145">The following diagram shows the inheritance relations in this example.</span></span>

![illustrazione che mostra l'ereditarietà dell'interfaccia, con le classi Shape e bitmap che puntano a IDrawable, ma solo bitmap che punta a ISerializable](images/com02.png)

<span data-ttu-id="2ce50-147">In questa sezione è stata esaminata la base concettuale delle interfacce, ma finora non è stato visto il codice COM effettivo.</span><span class="sxs-lookup"><span data-stu-id="2ce50-147">This section has examined the conceptual basis of interfaces, but so far we have not seen actual COM code.</span></span> <span data-ttu-id="2ce50-148">Si inizierà con la prima cosa che qualsiasi applicazione COM deve eseguire: inizializzare la libreria COM.</span><span class="sxs-lookup"><span data-stu-id="2ce50-148">We'll start with the first thing that any COM application must do: Initialize the COM library.</span></span>

## <a name="next"></a><span data-ttu-id="2ce50-149">Prossima</span><span class="sxs-lookup"><span data-stu-id="2ce50-149">Next</span></span>

[<span data-ttu-id="2ce50-150">Inizializzazione della libreria COM</span><span class="sxs-lookup"><span data-stu-id="2ce50-150">Initializing the COM Library</span></span>](initializing-the-com-library.md)