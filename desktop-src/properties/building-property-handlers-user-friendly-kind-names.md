---
description: Il sistema di proprietà contiene una proprietà denominata System. Kind, che divide gli elementi in tipi in base all'estensione del nome di file e che gli utenti finali possono identificare facilmente con.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Uso dei nomi dei tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f358306deaeb04d4ea30b10b0665cdc8323b4d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344816"
---
# <a name="using-kind-names"></a><span data-ttu-id="e57ba-103">Uso dei nomi dei tipi</span><span class="sxs-lookup"><span data-stu-id="e57ba-103">Using Kind Names</span></span>

<span data-ttu-id="e57ba-104">Il sistema di proprietà contiene una proprietà denominata `System.Kind` , che divide gli elementi in tipi in base all'estensione del nome file e con cui gli utenti finali possono identificare facilmente.</span><span class="sxs-lookup"><span data-stu-id="e57ba-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="e57ba-105">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e57ba-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e57ba-106">Informazioni sulla proprietà System. Kind</span><span class="sxs-lookup"><span data-stu-id="e57ba-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="e57ba-107">Gerarchia e registrazione del valore Kind</span><span class="sxs-lookup"><span data-stu-id="e57ba-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="e57ba-108">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="e57ba-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="e57ba-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e57ba-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="e57ba-110">Informazioni sulla proprietà System. Kind</span><span class="sxs-lookup"><span data-stu-id="e57ba-110">About the System.Kind Property</span></span>

<span data-ttu-id="e57ba-111">La tipologia è stata introdotta in Windows Vista per esprimere una nozione di tipo file più intuitiva.</span><span class="sxs-lookup"><span data-stu-id="e57ba-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="e57ba-112">La `System.Kind` Proprietà divide gli elementi in tipi e fornisce un nome di tipo che gli utenti finali possono identificare, ad esempio documenti, musica, immagini e così via.</span><span class="sxs-lookup"><span data-stu-id="e57ba-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="e57ba-113">Di conseguenza, i nomi dei tipi sono noti come intuitivi.</span><span class="sxs-lookup"><span data-stu-id="e57ba-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="e57ba-114">Poiché la `System.Kind` proprietà è impostata sullo stesso valore per gli elementi dello stesso tipo di file e associa elementi con caratteristiche simili a una proprietà comune, il sistema e l'utente possono agire sul gruppo nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="e57ba-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="e57ba-115">La proprietà, ad esempio, `System.Kind` può essere utilizzata per limitare la ricerca agli elementi di un tipo specifico, visualizzare le proprietà più rilevanti per un elemento nella visualizzazione contenuto oppure raggruppare elementi simili.</span><span class="sxs-lookup"><span data-stu-id="e57ba-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="e57ba-116">Poiché Kind è una proprietà di stringa multivalore, è possibile avere un `audio;video` `link;document` valore di tipo o.</span><span class="sxs-lookup"><span data-stu-id="e57ba-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="e57ba-117">Un `System.Kind` valore è un elenco ordinato di valori stringa.</span><span class="sxs-lookup"><span data-stu-id="e57ba-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="e57ba-118">In alcuni casi, potrebbe essere presente un solo elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="e57ba-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="e57ba-119">In altri casi, un elemento può appartenere a più di un tipo.</span><span class="sxs-lookup"><span data-stu-id="e57ba-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="e57ba-120">Per un esempio di elemento che appartiene a più di un tipo, vedere l'esempio di chiave del registro di sistema in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e57ba-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="e57ba-121">I valori di stringa sono da un set predefinito di valori noti.</span><span class="sxs-lookup"><span data-stu-id="e57ba-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="e57ba-122">I valori vengono confrontati utilizzando le funzioni di confronto tra stringhe senza distinzione tra maiuscole e minuscole e indipendenti dalle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="e57ba-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="e57ba-123">Queste stringhe non sono localizzate.</span><span class="sxs-lookup"><span data-stu-id="e57ba-123">These strings are not localized.</span></span>

<span data-ttu-id="e57ba-124">Alcuni nomi di tipi sono già associati a proprietà e modelli di layout.</span><span class="sxs-lookup"><span data-stu-id="e57ba-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="e57ba-125">Ad esempio, gli elementi associati agli `Kind.Picture` elementi e associati a `Kind.Document` visualizzano proprietà diverse anche quando si trovano nella stessa vista, a causa delle proprietà e dei modelli di layout già associati a questi due nomi di tipo.</span><span class="sxs-lookup"><span data-stu-id="e57ba-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="e57ba-126">Ogni tipo di elemento può essere associato a uno dei quattro modelli di layout univoci che definiscono il numero di proprietà visualizzate per ogni elemento e il relativo layout.</span><span class="sxs-lookup"><span data-stu-id="e57ba-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="e57ba-127">Per altre informazioni, vedere [visualizzazione contenuto in base al tipo di file o all'associazione di tipo](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e57ba-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="e57ba-128">Gerarchia e registrazione del valore Kind</span><span class="sxs-lookup"><span data-stu-id="e57ba-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="e57ba-129">Un `Kind` valore deve rappresentare uno dei valori nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="e57ba-129">A `Kind` value must represent one of the values in the following list.</span></span>

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

<span data-ttu-id="e57ba-130">I gestori di proprietà possono dichiarare la `System.Kind` Proprietà in modo statico tramite il registro di sistema oppure possono fornire il valore in modo dinamico tramite il codice come se si trattasse di una proprietà standard.</span><span class="sxs-lookup"><span data-stu-id="e57ba-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="e57ba-131">Per definire in modo statico la `Kind` proprietà, viene aggiunta una voce di valore **reg \_ SZ** sotto la chiave del registro di sistema **KindMap** , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="e57ba-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

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

<span data-ttu-id="e57ba-132">Si noti che `Kind` può essere un singolo valore o più valori in una stringa delimitata da punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="e57ba-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="e57ba-133">Quando si specificano più valori, il `Kind` valore più specifico viene elencato per primo con quanto segue il meno specifico.</span><span class="sxs-lookup"><span data-stu-id="e57ba-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="e57ba-134">Nell'esempio, Contact viene denominato First perché è gerarchicamente più specifico delle comunicazioni.</span><span class="sxs-lookup"><span data-stu-id="e57ba-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="e57ba-135">L' **elemento** value viene utilizzato e non deve essere specificato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="e57ba-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e57ba-136">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="e57ba-136">Additional Resources</span></span>

-   <span data-ttu-id="e57ba-137">Per la documentazione di riferimento sulle proprietà, vedere [System. Kind](./props-system-kind.md) e [System. KindText](./props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="e57ba-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="e57ba-138">Per ulteriori informazioni sulla creazione di nuovi tipi di file o sull'utilizzo di tipi di file esistenti, vedere [tipi di file](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e57ba-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e57ba-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e57ba-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e57ba-140">Informazioni sui gestori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="e57ba-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="e57ba-141">Uso degli elenchi di proprietà</span><span class="sxs-lookup"><span data-stu-id="e57ba-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="e57ba-142">Inizializzazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="e57ba-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="e57ba-143">Registrazione e distribuzione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="e57ba-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="e57ba-144">Procedure consigliate e domande frequenti sul gestore delle proprietà</span><span class="sxs-lookup"><span data-stu-id="e57ba-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
