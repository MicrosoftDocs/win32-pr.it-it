---
description: La clausola ORDER IN GROUP viene utilizzata insieme all'istruzione GROUP ON, che restituisce set di risultati in gruppi.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: Clausola ORDER IN GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342951"
---
# <a name="order-in-group-clause"></a><span data-ttu-id="e1cf9-103">Clausola ORDER IN GROUP</span><span class="sxs-lookup"><span data-stu-id="e1cf9-103">ORDER IN GROUP Clause</span></span>

<span data-ttu-id="e1cf9-104">La clausola ORDER IN GROUP viene utilizzata insieme all'istruzione [Group on](-search-sql-group-on-over.md) , che restituisce set di risultati in gruppi.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-104">The ORDER IN GROUP clause is used in conjunction with the [GROUP ON](-search-sql-group-on-over.md) statement, which returns result sets in groups.</span></span> <span data-ttu-id="e1cf9-105">La clausola ORDER IN GROUP consente di ordinare ogni gruppo restituito in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-105">The ORDER IN GROUP clause enables you to sort each returned group in a different way.</span></span> <span data-ttu-id="e1cf9-106">Se si esegue il raggruppamento in System. Kind, ad esempio, è possibile ordinare tutti i documenti in base System.Document. LastAuthor, tutti i file musicali per System. Music. AlbumArtist e tutti i messaggi di posta elettronica da System. Message. FromName.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-106">If you group on System.Kind, for example, you can then sort all documents by System.Document.LastAuthor, all music files by System.Music.AlbumArtist, and all emails by System.Message.FromName.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1cf9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1cf9-107">Syntax</span></span>

<span data-ttu-id="e1cf9-108">Di seguito è riportata la sintassi della clausola ORDER IN GROUP:</span><span class="sxs-lookup"><span data-stu-id="e1cf9-108">The following is the syntax of the ORDER IN GROUP clause:</span></span>


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



<span data-ttu-id="e1cf9-109">L'identificatore del nome del gruppo è un intervallo o un valore noto della colonna di gruppo, come specificato nell'istruzione GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-109">The group name specifier is a range or known value from the group column, as specified in the GROUP ON statement.</span></span> <span data-ttu-id="e1cf9-110">Ad esempio, i valori noti per System. Photo. ISOSpeed includono ' ISO-100',' ISO-200' e così via.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-110">For example, known values for System.Photo.ISOSpeed would include 'ISO-100', 'ISO-200', and so on.</span></span> <span data-ttu-id="e1cf9-111">Un intervallo per System. Photo. DateTaken includerà' 2006-1-1' è 2007-1-1' per un'istruzione come GROUP in System. ItemDate \[ ' 2006-1-1',' 2007-1-1' \] .</span><span class="sxs-lookup"><span data-stu-id="e1cf9-111">A range for System.Photo.DateTaken would include '2006-1-1' and '2007-1-1' for a statement like GROUP ON System.ItemDate \['2006-1-1', '2007-1-1'\].</span></span>

<span data-ttu-id="e1cf9-112">L'identificatore di colonna deve essere una colonna valida specificata nell'istruzione GROUP ON o SELECT.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-112">The column specifier must be a valid column specified in either the GROUP ON or the SELECT statement.</span></span> <span data-ttu-id="e1cf9-113">È possibile includere più di una colonna, separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-113">You can include more than one column, separated by commas.</span></span> <span data-ttu-id="e1cf9-114">Se, ad esempio, si esegue il raggruppamento in System. Photo. ISOSpeed, è possibile ordinare tutte le foto ISO-100, prima in base a System. Photo. ShutterSpeed e quindi a System. Photo. aperture.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-114">For example, if you group on System.Photo.ISOSpeed, you can sort all ISO-100 photos, first by System.Photo.ShutterSpeed, and then by System.Photo.Aperture.</span></span>

<span data-ttu-id="e1cf9-115">L'identificatore di direzione facoltativo può essere ASC per l'ordine crescente (da basso a alto) o DESC per la decrescente (da alto a basso).</span><span class="sxs-lookup"><span data-stu-id="e1cf9-115">The optional direction specifier can be either ASC for ascending (low to high) or DESC for descending (high to low).</span></span> <span data-ttu-id="e1cf9-116">Se non si specifica un identificatore di direzione, viene usato il valore predefinito Ascending.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-116">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="e1cf9-117">Se si specifica più di una colonna, ma non si specificano tutte le direzioni, la direzione specificata per ultima viene applicata a ogni colonna successiva fino a quando non si modifica in modo esplicito la direzione.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-117">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each successive column until you explicitly change the direction.</span></span>

<span data-ttu-id="e1cf9-118">Gli intervalli o i valori non specificati in modo esplicito in una clausola ORDER GROUP IN sono ordinati in ordine crescente in base ai valori della colonna GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-118">Ranges or values that are not explicitly specified in an ORDER GROUP IN clause are sorted in ascending order by the values in the GROUP ON column.</span></span>

## <a name="examples"></a><span data-ttu-id="e1cf9-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="e1cf9-119">Examples</span></span>

<span data-ttu-id="e1cf9-120">Nell'esempio seguente vengono raggruppati i risultati in base alla proprietà System. Kind.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-120">The following example groups results by the System.Kind property.</span></span> <span data-ttu-id="e1cf9-121">La query ordina il gruppo ' Program ' in base al nome dell'applicazione e al gruppo ' Music ' in base al titolo dell'album e al numero di traccia.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-121">The query would order the 'program' group by the application name and the 'music' group by album title and track number.</span></span> <span data-ttu-id="e1cf9-122">Il gruppo **null** verrebbe ordinato in base al nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-122">The **NULL** group would be ordered by the item name.</span></span> <span data-ttu-id="e1cf9-123">Tutti gli altri gruppi verranno ordinati in base alla data dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-123">All other groups would by ordered by the item date.</span></span>


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



<span data-ttu-id="e1cf9-124">Nell'esempio seguente vengono raggruppati i risultati in base alla proprietà System. ItemDate, quindi viene ordinata l'URL, il tipo o il nome di ogni elemento Group by.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-124">The following example groups results by the System.ItemDate property, and then sorts each group by item URL, kind, or name.</span></span>


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



<span data-ttu-id="e1cf9-125">I risultati della query precedente verrebbero restituiti in cinque gruppi e ordinati come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e1cf9-125">The results of the preceding query would be returned in five groups and sorted as described in the following table.</span></span>



| <span data-ttu-id="e1cf9-126">Gruppo</span><span class="sxs-lookup"><span data-stu-id="e1cf9-126">Group</span></span>    | <span data-ttu-id="e1cf9-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1cf9-127">Description</span></span>                                               | <span data-ttu-id="e1cf9-128">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="e1cf9-128">Sorted by</span></span>                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="e1cf9-129">MINVALUE</span><span class="sxs-lookup"><span data-stu-id="e1cf9-129">MINVALUE</span></span> | <span data-ttu-id="e1cf9-130">Elementi con date precedenti alla 2006-1-1</span><span class="sxs-lookup"><span data-stu-id="e1cf9-130">Items with dates before 2006-1-1</span></span>                          | <span data-ttu-id="e1cf9-131">Ordinato in base all'URL dell'elemento, in ordine crescente</span><span class="sxs-lookup"><span data-stu-id="e1cf9-131">Sorted by the item's URL, in ascending order</span></span> |
| <span data-ttu-id="e1cf9-132">2006-1-1</span><span class="sxs-lookup"><span data-stu-id="e1cf9-132">2006-1-1</span></span> | <span data-ttu-id="e1cf9-133">Elementi con date il o dopo il 2006-1-1 ma prima del 2007-1-1</span><span class="sxs-lookup"><span data-stu-id="e1cf9-133">Items with dates on or after 2006-1-1 but before 2007-1-1</span></span> | <span data-ttu-id="e1cf9-134">Ordinato per data dell'elemento, in ordine crescente</span><span class="sxs-lookup"><span data-stu-id="e1cf9-134">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="e1cf9-135">2007-1-1</span><span class="sxs-lookup"><span data-stu-id="e1cf9-135">2007-1-1</span></span> | <span data-ttu-id="e1cf9-136">Elementi con date il o dopo il 2007-1-1 ma prima del 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="e1cf9-136">Items with dates on or after 2007-1-1 but before 2008-1-1</span></span> | <span data-ttu-id="e1cf9-137">Ordinato per valore di tipo, in ordine crescente</span><span class="sxs-lookup"><span data-stu-id="e1cf9-137">Sorted by kind value, in ascending order</span></span>     |
| <span data-ttu-id="e1cf9-138">2008-1-1</span><span class="sxs-lookup"><span data-stu-id="e1cf9-138">2008-1-1</span></span> | <span data-ttu-id="e1cf9-139">Elementi con date il o dopo il 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="e1cf9-139">Items with dates on or after 2008-1-1</span></span>                     | <span data-ttu-id="e1cf9-140">Ordinato per data dell'elemento, in ordine crescente</span><span class="sxs-lookup"><span data-stu-id="e1cf9-140">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="e1cf9-141">**NULL**</span><span class="sxs-lookup"><span data-stu-id="e1cf9-141">**NULL**</span></span> | <span data-ttu-id="e1cf9-142">Elementi senza valore nella colonna System. ItemDate</span><span class="sxs-lookup"><span data-stu-id="e1cf9-142">Items with no value in the System.ItemDate column</span></span>         | <span data-ttu-id="e1cf9-143">Ordinato in base al nome dell'elemento, in ordine crescente</span><span class="sxs-lookup"><span data-stu-id="e1cf9-143">Sorted by item name, in ascending order</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="e1cf9-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1cf9-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e1cf9-145">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e1cf9-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e1cf9-146">RAGGRUPPA IN... SOPRA... Istruzione</span><span class="sxs-lookup"><span data-stu-id="e1cf9-146">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
</dt> <dt>

[<span data-ttu-id="e1cf9-147">Clausola ORDER BY</span><span class="sxs-lookup"><span data-stu-id="e1cf9-147">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> </dl>

 

 



