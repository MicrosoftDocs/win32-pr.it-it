---
description: Dopo aver valutato la strategia di proprietà, è necessario determinare quali proprietà visualizzare nell'interfaccia utente di Esplora risorse e dove.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Uso degli elenchi di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967114"
---
# <a name="using-property-lists"></a><span data-ttu-id="8f99e-103">Uso degli elenchi di proprietà</span><span class="sxs-lookup"><span data-stu-id="8f99e-103">Using Property Lists</span></span>

<span data-ttu-id="8f99e-104">Dopo aver valutato la strategia di proprietà, è necessario determinare quali proprietà visualizzare nell'interfaccia utente di Esplora risorse e dove.</span><span class="sxs-lookup"><span data-stu-id="8f99e-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="8f99e-105">Sono disponibili diverse posizioni in cui le proprietà vengono visualizzate in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8f99e-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="8f99e-106">La modifica delle proprietà, d'altra parte, è abilitata solo nella finestra di dialogo **Proprietà** .</span><span class="sxs-lookup"><span data-stu-id="8f99e-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="8f99e-107">Questa finestra di dialogo può essere richiamata tramite il collegamento **modifica proprietà** nel **riquadro di anteprima** o il menu di scelta rapida di un elemento.</span><span class="sxs-lookup"><span data-stu-id="8f99e-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="8f99e-108">Gli elenchi di proprietà sono stringhe delimitate da punto e virgola che hanno il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="8f99e-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="8f99e-109">L'unico flag attualmente disponibile è illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8f99e-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="8f99e-110">Flag</span><span class="sxs-lookup"><span data-stu-id="8f99e-110">Flag</span></span> | <span data-ttu-id="8f99e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f99e-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="8f99e-112">Non visualizzare la proprietà nel riquadro di **Anteprima** come indicato nel valore della chiave del registro di sistema **PreviewDetails** .</span><span class="sxs-lookup"><span data-stu-id="8f99e-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="8f99e-113">Se il valore di questa proprietà non è impostato, vedere l'esempio che segue la tabella successiva.</span><span class="sxs-lookup"><span data-stu-id="8f99e-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="8f99e-114">Dopo aver definito un elenco di proprietà, è possibile archiviare tale stringa nel registro di sistema tramite il sistema di [associazione file della shell](../shell/fa-file-types.md) standard nella **radice delle \_ classi HKEY \_ .**</span><span class="sxs-lookup"><span data-stu-id="8f99e-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="8f99e-115">Nella tabella seguente sono riepilogati i valori per gli elenchi di proprietà che possono essere assegnati nella chiave del registro di sistema per una particolare estensione di file.</span><span class="sxs-lookup"><span data-stu-id="8f99e-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f99e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8f99e-116">Value</span></span></th>
<th><span data-ttu-id="8f99e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f99e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f99e-118">FullDetails</span><span class="sxs-lookup"><span data-stu-id="8f99e-118">FullDetails</span></span></td>
<td><span data-ttu-id="8f99e-119">Le proprietà vengono visualizzate nella scheda <strong>Dettagli</strong> della finestra di dialogo <strong>Proprietà</strong> .</span><span class="sxs-lookup"><span data-stu-id="8f99e-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="8f99e-120">Questo è l'elenco completo delle proprietà supportate dal tipo di file.</span><span class="sxs-lookup"><span data-stu-id="8f99e-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f99e-121">PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="8f99e-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="8f99e-122">Le proprietà vengono visualizzate nel <strong>riquadro di anteprima</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f99e-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f99e-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="8f99e-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="8f99e-124">Le proprietà vengono visualizzate nell'area del titolo del <strong>riquadro di anteprima</strong> accanto all'anteprima dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8f99e-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="8f99e-125">Il numero massimo di voci è 3.</span><span class="sxs-lookup"><span data-stu-id="8f99e-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="8f99e-126">Se l'elenco di proprietà contiene un numero di dimensioni superiore al massimo consentito, il resto delle voci viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="8f99e-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f99e-127">TileInfo</span><span class="sxs-lookup"><span data-stu-id="8f99e-127">TileInfo</span></span></td>
<td><span data-ttu-id="8f99e-128">Le proprietà vengono visualizzate quando la visualizzazione elenco è in modalità di visualizzazione <strong>riquadri</strong> .</span><span class="sxs-lookup"><span data-stu-id="8f99e-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="8f99e-129">Il numero massimo di voci è 3.</span><span class="sxs-lookup"><span data-stu-id="8f99e-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="8f99e-130">Se l'elenco di proprietà contiene un numero di dimensioni superiore al massimo consentito, il resto delle voci viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="8f99e-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8f99e-131">Questo valore era presente in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f99e-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f99e-132">ExtendedTileInfo</span><span class="sxs-lookup"><span data-stu-id="8f99e-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="8f99e-133">Le proprietà vengono visualizzate per un elemento quando la visualizzazione elenco è in modalità di visualizzazione <strong>affiancata estesa</strong> .</span><span class="sxs-lookup"><span data-stu-id="8f99e-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f99e-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="8f99e-134">InfoTip</span></span></td>
<td><span data-ttu-id="8f99e-135">Le proprietà vengono visualizzate in un infotip quando un utente passa il mouse su un elemento.</span><span class="sxs-lookup"><span data-stu-id="8f99e-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8f99e-136">Questo valore era presente in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f99e-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f99e-137">QuickTip</span><span class="sxs-lookup"><span data-stu-id="8f99e-137">QuickTip</span></span></td>
<td><span data-ttu-id="8f99e-138">Le proprietà vengono visualizzate quando è difficile recuperare le proprietà direttamente da un elemento, ad esempio quando è necessario accedere all'elemento tramite una connessione di rete lenta.</span><span class="sxs-lookup"><span data-stu-id="8f99e-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="8f99e-139">È consigliabile che le proprietà denominate qui, ad esempio tipo o dimensione, non richiedano l'apertura del flusso di file per determinarne il valore.</span><span class="sxs-lookup"><span data-stu-id="8f99e-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8f99e-140">Questo valore era presente in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f99e-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8f99e-141">Nell'esempio seguente viene definito il valore PreviewDetails per un tipo di file Recipe, usando un ProgID di **RecipeKey**.</span><span class="sxs-lookup"><span data-stu-id="8f99e-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="8f99e-142">Come illustrato nell'argomento relativo all' [associazione di file della shell](../shell/fa-file-types.md) , è possibile descrivere le associazioni di file per il formato più specifico.</span><span class="sxs-lookup"><span data-stu-id="8f99e-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="8f99e-143">Il formato più specifico è l'unica estensione del nome file e il modulo più generico è una chiave che si applica a tutti i file e le cartelle di file.</span><span class="sxs-lookup"><span data-stu-id="8f99e-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="8f99e-144">Tra questi due estremi, è anche possibile definire un [ProgID](../shell/fa-progids.md) che raggruppa un set di estensioni di file (ad esempio, i tipi jpg e JPEG raggruppati come **jpegfile**).</span><span class="sxs-lookup"><span data-stu-id="8f99e-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="8f99e-145">Quando si definiscono gli elenchi di proprietà, è necessario definirli per i ProgID oppure, in alcuni casi, estensioni di file specifiche.</span><span class="sxs-lookup"><span data-stu-id="8f99e-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="8f99e-146">Evitare di basarsi su voci ampie, ad esempio la chiave **AllFileSystemObjects** .</span><span class="sxs-lookup"><span data-stu-id="8f99e-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f99e-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f99e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f99e-148">Informazioni sui gestori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8f99e-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="8f99e-149">Uso dei nomi dei tipi</span><span class="sxs-lookup"><span data-stu-id="8f99e-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="8f99e-150">Inizializzazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="8f99e-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="8f99e-151">Registrazione e distribuzione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="8f99e-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="8f99e-152">Procedure consigliate e domande frequenti sul gestore delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8f99e-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
