---
title: Elemento argument
description: L'elemento Argument contiene una parte di una stringa di condizione.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Finestra degli elementi argomento Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329206"
---
# <a name="argument-element"></a><span data-ttu-id="d36fd-104">Elemento argument</span><span class="sxs-lookup"><span data-stu-id="d36fd-104">argument Element</span></span>

<span data-ttu-id="d36fd-105">L'elemento **argument** contiene una parte di una stringa di condizione.</span><span class="sxs-lookup"><span data-stu-id="d36fd-105">The **argument** element contains one portion of a condition string.</span></span> <span data-ttu-id="d36fd-106">Una stringa di condizione ha in genere una parte della condizione e una parte del valore.</span><span class="sxs-lookup"><span data-stu-id="d36fd-106">A condition string typically has a condition portion and a value portion.</span></span> <span data-ttu-id="d36fd-107">Ad esempio, nella stringa di condizione "Artist uguale a Joe", la parte della condizione è "Equals" e la parte del valore è "Joe".</span><span class="sxs-lookup"><span data-stu-id="d36fd-107">For example, in the condition string "Artist Equals Joe", the condition portion is "Equals" and the value portion is "Joe".</span></span>

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a><span data-ttu-id="d36fd-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="d36fd-108">Attributes</span></span>

<span data-ttu-id="d36fd-109">**nome** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="d36fd-109">**name** (required)</span></span>

<span data-ttu-id="d36fd-110">Nome di una parte della stringa della condizione.</span><span class="sxs-lookup"><span data-stu-id="d36fd-110">The name of one portion of the condition string.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d36fd-111">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="d36fd-111">Parent/Child Elements</span></span>



| <span data-ttu-id="d36fd-112">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="d36fd-112">Hierarchy</span></span> | <span data-ttu-id="d36fd-113">Elementi</span><span class="sxs-lookup"><span data-stu-id="d36fd-113">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="d36fd-114">Padre</span><span class="sxs-lookup"><span data-stu-id="d36fd-114">Parent</span></span>    | [<span data-ttu-id="d36fd-115">frammento</span><span class="sxs-lookup"><span data-stu-id="d36fd-115">fragment</span></span>](fragment-element.md) |
| <span data-ttu-id="d36fd-116">Figlio</span><span class="sxs-lookup"><span data-stu-id="d36fd-116">Child</span></span>     | <span data-ttu-id="d36fd-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="d36fd-117">None</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="d36fd-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d36fd-118">Remarks</span></span>

<span data-ttu-id="d36fd-119">Quando l'attributo **Name** di un elemento **Fragment** è una caratteristica dell'elemento multimediale, ad esempio Album Artist o genre, l'elemento **Fragment** deve contenere due elementi **argument** : uno che specifica una condizione e un altro che specifica un valore.</span><span class="sxs-lookup"><span data-stu-id="d36fd-119">When the **name** attribute of a **fragment** element is a media item characteristic such as Album Artist, or Genre, the **fragment** element must contain two **argument** elements: one that specifies a condition and another that specifies a value.</span></span> <span data-ttu-id="d36fd-120">La tabella seguente mostra due valori possibili per l'attributo **Name** e come vengono usati gli elementi **argument** per specificare le condizioni e i valori.</span><span class="sxs-lookup"><span data-stu-id="d36fd-120">The following table shows two possible values for the **name** attribute and how **argument** elements are used to specify conditions and values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d36fd-121">Valore di attributo</span><span class="sxs-lookup"><span data-stu-id="d36fd-121">Attribute value</span></span></th>
<th><span data-ttu-id="d36fd-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d36fd-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d36fd-123">Condizione</span><span class="sxs-lookup"><span data-stu-id="d36fd-123">Condition</span></span></td>
<td><span data-ttu-id="d36fd-124">Il contenuto dell'elemento <strong>argument</strong> è la parte della condizione di una stringa di condizione.</span><span class="sxs-lookup"><span data-stu-id="d36fd-124">The content of the <strong>argument</strong> element is the condition portion of a condition string.</span></span> <span data-ttu-id="d36fd-125">Nella condizione, ad esempio, &quot; la stringa Artist è uguale a Joe &quot; , la parte della condizione è &quot; uguale a &quot; .</span><span class="sxs-lookup"><span data-stu-id="d36fd-125">For example, in the condition string &quot;Artist Equals Joe&quot;, the condition portion is &quot;Equals&quot;.</span></span> <span data-ttu-id="d36fd-126">La parte della condizione di una stringa di condizione deve essere una delle seguenti: Equals, non uguale a, Contains, non contiene, è minore di, è maggiore di, è, non è, è precedente a, è successiva a, è più recente di, superiore, inferiore, crescente, decrescente, casuale, è almeno, non è maggiore di.</span><span class="sxs-lookup"><span data-stu-id="d36fd-126">The condition portion of a condition string must be one of the following: Equals, Does Not Equal, Contains, Does Not Contain, Is Less Than, Is Greater Than, Is, Is Not, Is Before, Is Later Than, Is More Recent Than, Above, Below, Ascending, Descending, Random, Is At Least, Is No More Than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d36fd-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d36fd-127">Value</span></span></td>
<td><span data-ttu-id="d36fd-128">Il contenuto dell'elemento <strong>argument</strong> è la parte relativa al valore di una stringa di condizione.</span><span class="sxs-lookup"><span data-stu-id="d36fd-128">The content of the <strong>argument</strong> element is the value portion of a condition string.</span></span> <span data-ttu-id="d36fd-129">Nella condizione, ad esempio, &quot; la stringa Artist è uguale a Joe &quot; , la parte relativa al valore è &quot; Joe &quot; . Esempio</span><span class="sxs-lookup"><span data-stu-id="d36fd-129">For example, in the condition string &quot;Artist Equals Joe&quot;, the value portion is &quot;Joe&quot;.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d36fd-130">Quando l'attributo **Name** di un elemento **Fragment** è "Limit Total Size to" o "Limit Total Duration to", l'elemento **Fragment** deve contenere due elementi **argument** : uno che specifica un formato e uno che specifica un numero.</span><span class="sxs-lookup"><span data-stu-id="d36fd-130">When the **name** attribute of a **fragment** element is "Limit Total Size To" or "Limit Total Duration To", the **fragment** element must contain two **argument** elements: one that specifies a format and one that specifies a number.</span></span> <span data-ttu-id="d36fd-131">La tabella seguente illustra due valori possibili per l'attributo **Name** e come vengono usati gli elementi **argument** per limitare le dimensioni o la durata di una playlist.</span><span class="sxs-lookup"><span data-stu-id="d36fd-131">The following table shows two possible values for the **name** attribute and how **argument** elements are used to limit the size or duration of a playlist.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d36fd-132">Valore di attributo</span><span class="sxs-lookup"><span data-stu-id="d36fd-132">Attribute value</span></span></th>
<th><span data-ttu-id="d36fd-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d36fd-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d36fd-134">Formato</span><span class="sxs-lookup"><span data-stu-id="d36fd-134">Format</span></span></td>
<td><span data-ttu-id="d36fd-135">Quando l'attributo <strong>Name</strong> dell'elemento <strong>Fragment</strong> è &quot; limitato alle dimensioni totali &quot; , il contenuto dell'elemento <strong>argument</strong> deve essere uno dei seguenti: kilobyte, megabyte o gigabyte. quando l'attributo <strong>Name</strong> dell'elemento <strong>Fragment</strong> è &quot; limite Total Duration a &quot; , il contenuto dell'elemento <strong>argument</strong> deve essere uno dei seguenti: seconds, minutes, hours o Days.</span><span class="sxs-lookup"><span data-stu-id="d36fd-135">When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Size To&quot;, the content of the <strong>argument</strong> element must be one of the following: Kilobytes, Megabytes, or Gigabytes.When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Duration To&quot;, the content of the <strong>argument</strong> element must be one of the following: Seconds, Minutes, Hours, or Days.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d36fd-136">Number</span><span class="sxs-lookup"><span data-stu-id="d36fd-136">Number</span></span></td>
<td><span data-ttu-id="d36fd-137">Il contenuto dell'elemento <strong>argument</strong> è un numero che limita la dimensione o la durata della playlist. Esempi</span><span class="sxs-lookup"><span data-stu-id="d36fd-137">The content of the <strong>argument</strong> element is a number that limits the size or duration of the playlist.Examples:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d36fd-138">Quando l'attributo **Name** di un elemento **Fragment** è "Limit number of items", l'elemento **Fragment** deve contenere un elemento **argument** che specifica il numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="d36fd-138">When the **name** attribute of a **fragment** element is "Limit Number of Items", the **fragment** element must contain one **argument** element that specifies the number of items.</span></span> <span data-ttu-id="d36fd-139">Nella tabella seguente viene illustrato come utilizzare il valore numerico dell'attributo **Name** .</span><span class="sxs-lookup"><span data-stu-id="d36fd-139">The following table shows how to use the Number value of the **name** attribute.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d36fd-140">Valore di attributo</span><span class="sxs-lookup"><span data-stu-id="d36fd-140">Attribute value</span></span></th>
<th><span data-ttu-id="d36fd-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d36fd-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d36fd-142">Number</span><span class="sxs-lookup"><span data-stu-id="d36fd-142">Number</span></span></td>
<td><span data-ttu-id="d36fd-143">Il contenuto dell'elemento <strong>argument</strong> è un numero che limita il numero di elementi in una playlist. Esempio</span><span class="sxs-lookup"><span data-stu-id="d36fd-143">The content of the <strong>argument</strong> element is a number that limits the number of items in a playlist.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d36fd-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d36fd-144">Requirements</span></span>



| <span data-ttu-id="d36fd-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="d36fd-145">Requirement</span></span> | <span data-ttu-id="d36fd-146">Valore</span><span class="sxs-lookup"><span data-stu-id="d36fd-146">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="d36fd-147">Versione</span><span class="sxs-lookup"><span data-stu-id="d36fd-147">Version</span></span><br/> | <span data-ttu-id="d36fd-148">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="d36fd-148">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d36fd-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d36fd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d36fd-150">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="d36fd-150">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="d36fd-151">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d36fd-151">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





