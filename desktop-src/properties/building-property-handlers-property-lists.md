---
description: Dopo aver valutato la strategia di proprietà, è necessario determinare le proprietà da visualizzare nell'interfaccia Windows Explorer e dove.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Uso degli elenchi di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade6cba2807e87306aa9cacb3649499d9e5ffe1
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481916"
---
# <a name="using-property-lists"></a><span data-ttu-id="c0809-103">Uso degli elenchi di proprietà</span><span class="sxs-lookup"><span data-stu-id="c0809-103">Using Property Lists</span></span>

<span data-ttu-id="c0809-104">Dopo aver valutato la strategia di proprietà, è necessario determinare le proprietà da visualizzare nell'interfaccia Windows Explorer e dove.</span><span class="sxs-lookup"><span data-stu-id="c0809-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="c0809-105">Esistono diverse posizioni in cui le proprietà vengono visualizzate in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c0809-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="c0809-106">La modifica delle proprietà, d'altra parte, è abilitata solo nella **finestra di dialogo** Proprietà.</span><span class="sxs-lookup"><span data-stu-id="c0809-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="c0809-107">Tale finestra di dialogo può essere richiamata tramite il **collegamento** Modifica proprietà nel riquadro di **anteprima** o il menu di scelta rapida di un elemento.</span><span class="sxs-lookup"><span data-stu-id="c0809-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="c0809-108">Gli elenchi di proprietà sono stringhe delimitate da punto e virgola con il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="c0809-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="c0809-109">L'unico flag attualmente disponibile è illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c0809-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="c0809-110">Flag</span><span class="sxs-lookup"><span data-stu-id="c0809-110">Flag</span></span> | <span data-ttu-id="c0809-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0809-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="c0809-112">Non visualizzare la proprietà nel riquadro **di** anteprima come indicato nel valore della chiave del Registro di sistema **PreviewDetails.**</span><span class="sxs-lookup"><span data-stu-id="c0809-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="c0809-113">Vedere l'esempio che segue la tabella successiva se il valore della proprietà non è impostato.</span><span class="sxs-lookup"><span data-stu-id="c0809-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="c0809-114">Dopo aver definito un elenco di proprietà, è possibile archiviare tale stringa nel Registro di sistema tramite il [file association](../shell/fa-file-types.md) system shell standard in **HKEY CLASSES \_ \_ ROOT.**</span><span class="sxs-lookup"><span data-stu-id="c0809-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="c0809-115">Nella tabella seguente sono riepilogati i valori per gli elenchi di proprietà che possono essere assegnati nella chiave del Registro di sistema per una determinata estensione di file.</span><span class="sxs-lookup"><span data-stu-id="c0809-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0809-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c0809-116">Value</span></span></th>
<th><span data-ttu-id="c0809-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0809-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0809-118">FullDetails</span><span class="sxs-lookup"><span data-stu-id="c0809-118">FullDetails</span></span></td>
<td><span data-ttu-id="c0809-119">Le proprietà vengono visualizzate nella <strong>scheda Dettagli</strong> della finestra <strong>di dialogo</strong> Proprietà .</span><span class="sxs-lookup"><span data-stu-id="c0809-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="c0809-120">Questo è l'elenco completo delle proprietà supportate dal tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c0809-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0809-121">PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="c0809-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="c0809-122">Le proprietà vengono visualizzate nel riquadro <strong>di anteprima.</strong></span><span class="sxs-lookup"><span data-stu-id="c0809-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0809-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="c0809-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="c0809-124">Le proprietà vengono visualizzate nell'area del titolo del riquadro <strong>di anteprima</strong> accanto all'anteprima dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c0809-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="c0809-125">Il numero massimo di voci è 3.</span><span class="sxs-lookup"><span data-stu-id="c0809-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="c0809-126">Se l'elenco di proprietà contiene più del numero massimo consentito, le altre voci vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="c0809-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0809-127">TileInfo</span><span class="sxs-lookup"><span data-stu-id="c0809-127">TileInfo</span></span></td>
<td><span data-ttu-id="c0809-128">Le proprietà vengono visualizzate quando la visualizzazione elenco è in <strong>modalità di</strong> visualizzazione Riquadri.</span><span class="sxs-lookup"><span data-stu-id="c0809-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="c0809-129">Il numero massimo di voci è 3.</span><span class="sxs-lookup"><span data-stu-id="c0809-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="c0809-130">Se l'elenco di proprietà contiene più del numero massimo consentito, le altre voci vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="c0809-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0809-131">Questo valore era presente in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c0809-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0809-132">ExtendedTileInfo</span><span class="sxs-lookup"><span data-stu-id="c0809-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="c0809-133">Le proprietà vengono visualizzate per un elemento quando la visualizzazione elenco è in <strong>modalità di visualizzazione Riquadro</strong> esteso.</span><span class="sxs-lookup"><span data-stu-id="c0809-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0809-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="c0809-134">InfoTip</span></span></td>
<td><span data-ttu-id="c0809-135">Le proprietà vengono visualizzate in un suggerimento quando un utente passa il mouse su un elemento.</span><span class="sxs-lookup"><span data-stu-id="c0809-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0809-136">Questo valore era presente in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c0809-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0809-137">Quicktip</span><span class="sxs-lookup"><span data-stu-id="c0809-137">QuickTip</span></span></td>
<td><span data-ttu-id="c0809-138">Le proprietà vengono visualizzate quando è difficile recuperare le proprietà direttamente da un elemento, ad esempio quando è necessario accedere all'elemento tramite una connessione di rete lenta.</span><span class="sxs-lookup"><span data-stu-id="c0809-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="c0809-139">È consigliabile che le proprietà denominate qui, ad esempio Tipo o Dimensione, non richiedano l'apertura del flusso di file per determinarne il valore.</span><span class="sxs-lookup"><span data-stu-id="c0809-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0809-140">Questo valore era presente in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c0809-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c0809-141">L'esempio seguente definisce il valore PreviewDetails per un tipo di file con estensione recipe, usando un ProgID **di RecipeKey**.</span><span class="sxs-lookup"><span data-stu-id="c0809-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="c0809-142">Come illustrato [nell'argomento Associazione file shell,](../shell/fa-file-types.md) le associazioni di file possono essere descritte per la forma più specifica per la forma più generale.</span><span class="sxs-lookup"><span data-stu-id="c0809-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="c0809-143">La forma più specifica è la singola estensione di file e la forma più generica è una chiave che si applica a tutti i file e le cartelle di file.</span><span class="sxs-lookup"><span data-stu-id="c0809-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="c0809-144">Tra questi due estremi, è anche possibile definire un [PROGID](../shell/fa-progids.md) che raggruppa un set di estensioni di file (ad esempio, i tipi .jpg e jpeg raggruppati come **jpegfile**).</span><span class="sxs-lookup"><span data-stu-id="c0809-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="c0809-145">Quando si definiscono elenchi di proprietà, è necessario definirli per ProgID o, in alcuni casi, estensioni di file specifiche.</span><span class="sxs-lookup"><span data-stu-id="c0809-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="c0809-146">Evitare di basarsi su voci generali, ad esempio la **chiave AllFileSystemObjects.**</span><span class="sxs-lookup"><span data-stu-id="c0809-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0809-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0809-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0809-148">Informazioni sui gestori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="c0809-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="c0809-149">Uso dei nomi dei tipi</span><span class="sxs-lookup"><span data-stu-id="c0809-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="c0809-150">Inizializzazione dei gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="c0809-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="c0809-151">Registrazione e distribuzione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="c0809-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="c0809-152">Procedure consigliate e domande frequenti sul gestore delle proprietà</span><span class="sxs-lookup"><span data-stu-id="c0809-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
