---
description: Il sistema di proprietà contiene una proprietà denominata System.Kind, che divide gli elementi in tipi in base all'estensione di file e con cui gli utenti finali possono identificarsi facilmente.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Uso dei nomi dei tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca36d7c1de587efd8d96f0c18aaca9457721714
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481876"
---
# <a name="using-kind-names"></a><span data-ttu-id="778d5-103">Uso dei nomi dei tipi</span><span class="sxs-lookup"><span data-stu-id="778d5-103">Using Kind Names</span></span>

<span data-ttu-id="778d5-104">Il sistema di proprietà contiene una proprietà denominata , che divide gli elementi in tipi in base all'estensione di file e con cui gli utenti finali `System.Kind` possono identificarsi facilmente.</span><span class="sxs-lookup"><span data-stu-id="778d5-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="778d5-105">Questo argomento è organizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="778d5-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="778d5-106">Informazioni sulla proprietà System.Kind</span><span class="sxs-lookup"><span data-stu-id="778d5-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="778d5-107">Gerarchia dei valori di tipo e registrazione</span><span class="sxs-lookup"><span data-stu-id="778d5-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="778d5-108">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="778d5-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="778d5-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="778d5-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="778d5-110">Informazioni sulla proprietà System.Kind</span><span class="sxs-lookup"><span data-stu-id="778d5-110">About the System.Kind Property</span></span>

<span data-ttu-id="778d5-111">Kind è stato introdotto in Windows Vista per esprimere una nozione più semplice del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="778d5-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="778d5-112">La proprietà divide gli elementi in tipi e fornisce un nome tipo che gli utenti finali possono identificare, ad esempio `System.Kind` Documenti, Musica, Immagini e così via.</span><span class="sxs-lookup"><span data-stu-id="778d5-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="778d5-113">Di conseguenza, i nomi dei tipi sono noti come descrittivi.</span><span class="sxs-lookup"><span data-stu-id="778d5-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="778d5-114">Poiché la proprietà è impostata sullo stesso valore per gli elementi dello stesso tipo di file e associa elementi con caratteristiche simili a una proprietà comune, il sistema e l'utente possono agire sull'intero `System.Kind` gruppo.</span><span class="sxs-lookup"><span data-stu-id="778d5-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="778d5-115">Ad esempio, la proprietà può essere usata per limitare una ricerca agli elementi di un tipo specifico, visualizzare le proprietà più rilevanti per un elemento nella visualizzazione Contenuto o raggruppare `System.Kind` elementi simili.</span><span class="sxs-lookup"><span data-stu-id="778d5-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="778d5-116">Poiché Kind è una proprietà stringa multivalore, è possibile avere un `audio;video` valore o `link;document` Kind.</span><span class="sxs-lookup"><span data-stu-id="778d5-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="778d5-117">Un `System.Kind` valore è un elenco ordinato di valori stringa.</span><span class="sxs-lookup"><span data-stu-id="778d5-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="778d5-118">In alcuni casi, potrebbe essere presente un solo elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="778d5-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="778d5-119">In altri casi, un elemento può appartenere a più di un tipo.</span><span class="sxs-lookup"><span data-stu-id="778d5-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="778d5-120">Per un esempio di un elemento appartenente a più di un tipo, vedere l'esempio di chiave del Registro di sistema in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="778d5-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="778d5-121">I valori stringa derivano da un set predefinito di valori noti.</span><span class="sxs-lookup"><span data-stu-id="778d5-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="778d5-122">I valori vengono confrontati usando funzioni di confronto tra stringhe senza distinzione tra maiuscole e minuscole e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="778d5-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="778d5-123">Queste stringhe non sono localizzate.</span><span class="sxs-lookup"><span data-stu-id="778d5-123">These strings are not localized.</span></span>

<span data-ttu-id="778d5-124">Alcuni nomi di tipo sono già associati a proprietà e modelli di layout.</span><span class="sxs-lookup"><span data-stu-id="778d5-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="778d5-125">Ad esempio, gli elementi associati a e gli elementi associati a visualizzano proprietà diverse anche quando sono nella stessa visualizzazione, a causa delle proprietà e dei modelli di layout già associati a questi due `Kind.Picture` `Kind.Document` nomi Kind.</span><span class="sxs-lookup"><span data-stu-id="778d5-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="778d5-126">Ogni tipo di elemento può essere associato a uno dei quattro modelli di layout univoci che definiscono il numero di proprietà visualizzate per ogni elemento e il relativo layout.</span><span class="sxs-lookup"><span data-stu-id="778d5-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="778d5-127">Per altre informazioni, vedere [Visualizzazione contenuto basata sull'associazione tipo di file o tipo](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="778d5-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="778d5-128">Gerarchia dei valori di tipo e registrazione</span><span class="sxs-lookup"><span data-stu-id="778d5-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="778d5-129">Un `Kind` valore deve rappresentare uno dei valori nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="778d5-129">A `Kind` value must represent one of the values in the following list.</span></span>

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

<span data-ttu-id="778d5-130">I gestori delle proprietà possono dichiarare la proprietà in modo statico tramite il Registro di sistema oppure possono fornire il valore in modo dinamico tramite il codice come con `System.Kind` una proprietà standard.</span><span class="sxs-lookup"><span data-stu-id="778d5-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="778d5-131">Per definire in modo statico la proprietà, viene aggiunta una voce di valore `Kind` **REG \_ SZ** nella chiave del Registro di sistema **KindMap,** come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="778d5-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

<span data-ttu-id="778d5-132">Si noti che `Kind` può essere un singolo valore o più valori in una stringa delimitata da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="778d5-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="778d5-133">Quando si specificano più valori, il valore `Kind` più specifico viene elencato per primo con il valore meno specifico seguente.</span><span class="sxs-lookup"><span data-stu-id="778d5-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="778d5-134">Nell'esempio il nome Contact viene assegnato per primo perché è gerarchicamente più specifico di Communications.</span><span class="sxs-lookup"><span data-stu-id="778d5-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="778d5-135">Il valore **Item** viene assunto e non deve essere specificato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="778d5-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="778d5-136">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="778d5-136">Additional Resources</span></span>

-   <span data-ttu-id="778d5-137">Per la documentazione di riferimento sulle proprietà, [vedere System.Kind](./props-system-kind.md) e [System.KindText](./props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="778d5-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="778d5-138">Per altre informazioni sulla creazione di nuovi o sull'uso di tipi di file esistenti, vedere [Tipi di file](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="778d5-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="778d5-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="778d5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="778d5-140">Informazioni sui gestori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="778d5-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="778d5-141">Uso degli elenchi di proprietà</span><span class="sxs-lookup"><span data-stu-id="778d5-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="778d5-142">Inizializzazione dei gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="778d5-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="778d5-143">Registrazione e distribuzione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="778d5-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="778d5-144">Procedure consigliate e domande frequenti sul gestore delle proprietà</span><span class="sxs-lookup"><span data-stu-id="778d5-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
