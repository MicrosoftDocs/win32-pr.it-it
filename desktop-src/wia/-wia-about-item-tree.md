---
description: Con Windows Vista, l'albero degli elementi Windows Image Acquisition (WIA) è stato modificato in modo significativo.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Informazioni sull'albero degli elementi IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881901"
---
# <a name="about-the-iwiaitem2-item-tree"></a><span data-ttu-id="170a8-103">Informazioni sull'albero degli elementi IWiaItem2</span><span class="sxs-lookup"><span data-stu-id="170a8-103">About the IWiaItem2 Item Tree</span></span>

<span data-ttu-id="170a8-104">Con Windows Vista, l'albero degli elementi Windows Image Acquisition (WIA) è stato modificato in modo significativo.</span><span class="sxs-lookup"><span data-stu-id="170a8-104">With Windows Vista, the Windows Image Acquisition (WIA) item tree has changed significantly.</span></span> <span data-ttu-id="170a8-105">Gli elementi [**IWiaItem2**](-wia-iwiaitem2.md) vengono usati per rappresentare gli attributi del dispositivo e i dati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="170a8-105">[**IWiaItem2**](-wia-iwiaitem2.md) items are used to represent device attributes and device data.</span></span> <span data-ttu-id="170a8-106">Le applicazioni di imaging visualizzano un dispositivo Windows Image Acquisition (WIA) 2,0 come albero gerarchico di elementi, con l'elemento radice che rappresenta il dispositivo stesso e gli elementi figlio che rappresentano elementi come origini dati programmabili, immagini o cartelle contenenti immagini.</span><span class="sxs-lookup"><span data-stu-id="170a8-106">Imaging applications see a Windows Image Acquisition (WIA) 2.0 device as a hierarchical tree of items, with the root item representing the device itself and the child items representing things like programmable data sources, images, or folders that contain images.</span></span>

-   [<span data-ttu-id="170a8-107">Elementi dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="170a8-107">Application Items</span></span>](#application-items)
-   [<span data-ttu-id="170a8-108">Flag elemento</span><span class="sxs-lookup"><span data-stu-id="170a8-108">Item Flags</span></span>](#item-flags)
-   [<span data-ttu-id="170a8-109">Categorie di elementi</span><span class="sxs-lookup"><span data-stu-id="170a8-109">Item Categories</span></span>](#item-categories)
-   [<span data-ttu-id="170a8-110">Elemento radice</span><span class="sxs-lookup"><span data-stu-id="170a8-110">Root Item</span></span>](#root-item)
-   [<span data-ttu-id="170a8-111">Elemento dati</span><span class="sxs-lookup"><span data-stu-id="170a8-111">Data Item</span></span>](#data-item)
-   [<span data-ttu-id="170a8-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="170a8-112">Related topics</span></span>](#related-topics)

## <a name="application-items"></a><span data-ttu-id="170a8-113">Elementi dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="170a8-113">Application Items</span></span>

<span data-ttu-id="170a8-114">L'albero degli elementi WIA 2,0 che un'applicazione può visualizzare è separato dall'albero creato e gestito da un WIA 2,0 minidriver.</span><span class="sxs-lookup"><span data-stu-id="170a8-114">The WIA 2.0 item tree that an application can see is separate from the tree created and maintained by a WIA 2.0 minidriver.</span></span> <span data-ttu-id="170a8-115">Quando un minidriver crea un albero, il servizio WIA 2,0 utilizza questo albero degli elementi WIA 2,0 come guida per creare una copia dell'albero che può essere visualizzato dalle applicazioni di imaging.</span><span class="sxs-lookup"><span data-stu-id="170a8-115">When a minidriver creates a tree, the WIA 2.0 service uses this WIA 2.0 item tree as a guide to create a copy of the tree that can be viewed by imaging applications.</span></span> <span data-ttu-id="170a8-116">Gli elementi dell'albero copiato sono detti elementi *dell'applicazione* .</span><span class="sxs-lookup"><span data-stu-id="170a8-116">Items in the copied tree are called *application* items.</span></span> <span data-ttu-id="170a8-117">Gli elementi dell'albero creati da un minidriver sono denominati elementi del *driver* .</span><span class="sxs-lookup"><span data-stu-id="170a8-117">Items in the tree created by a minidriver are called *driver* items.</span></span>

<span data-ttu-id="170a8-118">Un elemento WIA può rappresentare un'origine dati programmabile per il feeder di documenti di uno scanner o i dati archiviati nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="170a8-118">A WIA item can represent a programmable data source for a scanner's document feeder or the data stored on that device.</span></span> <span data-ttu-id="170a8-119">Un dispositivo WIA deve essere suddiviso in singoli elementi che descrivono dati diversi prodotti da tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="170a8-119">A WIA device should be divided into individual items that describe different data produced by that device.</span></span>

<span data-ttu-id="170a8-120">Uno scanner WIA, ad esempio, che supporta l'analisi di livello piano e l'analisi dei feed di documenti può essere suddiviso in due elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="170a8-120">For example, a WIA scanner that supports both flatbed scanning and document feeder scanning might be divided into two child items.</span></span> <span data-ttu-id="170a8-121">Uno rappresenta la funzionalità di analisi piana e l'altro rappresenta la funzionalità di analisi del feeder di documenti.</span><span class="sxs-lookup"><span data-stu-id="170a8-121">One represents the flatbed scanning functionality and the other represents the document feeder scanning functionality.</span></span>

<span data-ttu-id="170a8-122">Più immagini disposte in uno scanner piano e analizzate contemporaneamente possono essere inserite in una cartella.</span><span class="sxs-lookup"><span data-stu-id="170a8-122">Multiple images laid out on a flatbed scanner and scanned at the same time can be placed in one folder.</span></span> <span data-ttu-id="170a8-123">Utilizzando il filtro di segmentazione ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), è possibile creare ogni immagine o area secondaria come elemento figlio della cartella.</span><span class="sxs-lookup"><span data-stu-id="170a8-123">Using the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), each image or subregion can then be created as a child item of the folder.</span></span>

<span data-ttu-id="170a8-124">L'albero WIA per un dispositivo fotocamera che archivia foto ("film") può essere suddiviso in elementi che rappresentano cartelle, sottocartelle e foto.</span><span class="sxs-lookup"><span data-stu-id="170a8-124">The WIA tree for a camera device that stores photos ("Film") can be divided into items that represent folders, subfolders, and photos.</span></span>

## <a name="item-flags"></a><span data-ttu-id="170a8-125">Flag elemento</span><span class="sxs-lookup"><span data-stu-id="170a8-125">Item Flags</span></span>

<span data-ttu-id="170a8-126">I flag elemento WIA consentono di classificare il contenuto o il comportamento supportato di un particolare elemento WIA.</span><span class="sxs-lookup"><span data-stu-id="170a8-126">WIA item flags help classify the content or supported behavior of a particular WIA item.</span></span> <span data-ttu-id="170a8-127">I flag elemento WIA rientrano in due gruppi.</span><span class="sxs-lookup"><span data-stu-id="170a8-127">WIA item flags fall into two groups.</span></span>

1.  <span data-ttu-id="170a8-128">I flag di stato dell'elemento segnalano lo stato corrente dell'elemento WIA, ad esempio [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted** e così via.</span><span class="sxs-lookup"><span data-stu-id="170a8-128">Item status flags report the current state of the WIA item, for example, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, and so forth.</span></span>
2.  <span data-ttu-id="170a8-129">I flag di rappresentazione/utilizzo dati elemento segnalano i dati che l'elemento WIA rappresenta o può produrre se trasferiti.</span><span class="sxs-lookup"><span data-stu-id="170a8-129">Item data representation/usage flags report the data that the WIA item represents or can produce if transferred.</span></span> <span data-ttu-id="170a8-130">Ad esempio, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) è un flag di rappresentazione dei dati che indica all'applicazione che i dati associati all'elemento WIA corrente sono dati di immagine e devono avere proprietà dei dati di immagine.</span><span class="sxs-lookup"><span data-stu-id="170a8-130">For example, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) is a data representation flag that tells the application the data associated with the current WIA item is image data and should have image data properties.</span></span> <span data-ttu-id="170a8-131">**WIA \_ I \_ \_ flag degli elementi IPA** sono un flag di utilizzo degli elementi che indica all'applicazione che l'elemento WIA è configurabile e segue un set di regole di configurazione predefinite basate sulla [**\_ \_ \_ categoria di elementi dell'IPA WIA**](-wia-wiaitempropcommonitem.md) e che la configurazione può eventualmente modificare il risultato per ogni trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="170a8-131">**WIA\_IPA\_ITEM\_FLAGS** is an item usage flag that tells the application that the WIA item is configurable and follows a set of predefined configuration rules based on the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) and that the configuration can possibly change the result for each data transfer.</span></span> <span data-ttu-id="170a8-132">Per ulteriori informazioni sulle definizioni di categoria, vedere categorie di elementi delle [categorie di elementi](#item-categories) .</span><span class="sxs-lookup"><span data-stu-id="170a8-132">(For more information about category definitions, see [Item Categories](#item-categories) item categories.)</span></span>

<span data-ttu-id="170a8-133">Nell'immagine seguente viene illustrato un esempio di albero degli elementi WIA e dei diversi flag che possono essere associati a ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="170a8-133">The following graphic shows an example of a WIA item tree and the various flags that might be associated with each item.</span></span>

![esempi di flag di elemento per gli elementi in un albero](images/scannertree1.jpg)

## <a name="item-categories"></a><span data-ttu-id="170a8-135">Categorie di elementi</span><span class="sxs-lookup"><span data-stu-id="170a8-135">Item Categories</span></span>

<span data-ttu-id="170a8-136">Gli elementi WIA sono raggruppati in categorie usando i valori delle proprietà di [**\_ \_ \_ categoria**](-wia-wiaitempropcommonitem.md) degli elementi dell'IPA WIA.</span><span class="sxs-lookup"><span data-stu-id="170a8-136">WIA items are grouped into categories using the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) property values.</span></span> <span data-ttu-id="170a8-137">Queste categorie definiscono la modalità di trattamento o di utilizzo di un elemento WIA.</span><span class="sxs-lookup"><span data-stu-id="170a8-137">These categories define how a WIA item is to be treated or used.</span></span> <span data-ttu-id="170a8-138">Se, ad esempio, l'elemento rappresenta un file terminato ( \_ file di categoria \_ terminata WIA \_ ), un'applicazione WIA deve presupporre che i dati siano statici e che si trovino nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="170a8-138">For example, if the item represents a finished file (WIA\_CATEGORY\_FINISHED\_FILE), a WIA application should assume that the data is static and located on the device.</span></span> <span data-ttu-id="170a8-139">Se l'elemento rappresenta un feeder (WIA \_ Category \_ Feeder), l'applicazione deve prevedere che contenga le proprietà richieste del feed di documenti e funzioni come un feeder di documenti.</span><span class="sxs-lookup"><span data-stu-id="170a8-139">If the item represents a feeder (WIA\_CATEGORY\_FEEDER), the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span>

<span data-ttu-id="170a8-140">Le categorie definite da WIA sono:</span><span class="sxs-lookup"><span data-stu-id="170a8-140">The categories defined by WIA are:</span></span>

-   <span data-ttu-id="170a8-141">\_categoria WIA \_ auto</span><span class="sxs-lookup"><span data-stu-id="170a8-141">WIA\_CATEGORY\_AUTO</span></span>
-   <span data-ttu-id="170a8-142">\_feed di categoria WIA \_</span><span class="sxs-lookup"><span data-stu-id="170a8-142">WIA\_CATEGORY\_FEEDER</span></span>
-   <span data-ttu-id="170a8-143">\_film di categoria WIA \_</span><span class="sxs-lookup"><span data-stu-id="170a8-143">WIA\_CATEGORY\_FILM</span></span>
-   <span data-ttu-id="170a8-144">\_file di categoria \_ completato \_ WIA</span><span class="sxs-lookup"><span data-stu-id="170a8-144">WIA\_CATEGORY\_FINISHED\_FILE</span></span>
-   <span data-ttu-id="170a8-145">\_categoria WIA \_ piana</span><span class="sxs-lookup"><span data-stu-id="170a8-145">WIA\_CATEGORY\_FLATBED</span></span>

<span data-ttu-id="170a8-146">Ad esempio, è possibile che un elemento piano dello scanner includa i [**flag degli \_ \_ elementi \_ dell'IPA WIA**](-wia-wiaitempropcommonitem.md) impostati su [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer** e **WiaItemTypeProgrammableDataSource** e che la proprietà della **categoria di \_ \_ elementi \_ WIA IPA** sia impostata su WIA \_ categoria \_ piana.</span><span class="sxs-lookup"><span data-stu-id="170a8-146">For example, a scanner's flatbed item may have the [**WIA\_IPA\_ITEM\_FLAGS**](-wia-wiaitempropcommonitem.md) set to [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer**, and **WiaItemTypeProgrammableDataSource**, and the **WIA\_IPA\_ITEM\_CATEGORY** property set to WIA\_CATEGORY\_FLATBED.</span></span>

<span data-ttu-id="170a8-147">La tabella seguente illustra il raggruppamento di categorie WIA con i flag di elemento e gli elementi WIA.</span><span class="sxs-lookup"><span data-stu-id="170a8-147">The following table shows WIA category grouping with item flags and WIA items.</span></span> <span data-ttu-id="170a8-148">Questa tabella non include un elenco completo dei flag di elemento WIA definiti da WIA.</span><span class="sxs-lookup"><span data-stu-id="170a8-148">This table does not include a full list of the WIA item flags defined by WIA.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="170a8-149">Categoria WIA</span><span class="sxs-lookup"><span data-stu-id="170a8-149">WIA Category</span></span></th>
<th><span data-ttu-id="170a8-150">Flag elemento WIA validi</span><span class="sxs-lookup"><span data-stu-id="170a8-150">Valid WIA Item Flags</span></span></th>
<th><span data-ttu-id="170a8-151">Set di proprietà WIA</span><span class="sxs-lookup"><span data-stu-id="170a8-151">WIA Property Set</span></span></th>
<th><span data-ttu-id="170a8-152">Elementi WIA</span><span class="sxs-lookup"><span data-stu-id="170a8-152">WIA Items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="170a8-153">WIA_CATEGORY_AUTO</span><span class="sxs-lookup"><span data-stu-id="170a8-153">WIA_CATEGORY_AUTO</span></span></td>
<td><ul>
<li><span data-ttu-id="170a8-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="170a8-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="170a8-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="170a8-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="170a8-158">Il set di proprietà include proprietà dello scanner configurate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="170a8-158">Property set includes auto-configured scanner properties.</span></span></td>
<td><span data-ttu-id="170a8-159">Elemento WIA automatico che rappresenta le impostazioni di analisi configurate automaticamente dello scanner.</span><span class="sxs-lookup"><span data-stu-id="170a8-159">WIA auto item that represents the scanner's auto-configured scanning settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="170a8-160">WIA_CATEGORY_FEEDER</span><span class="sxs-lookup"><span data-stu-id="170a8-160">WIA_CATEGORY_FEEDER</span></span></td>
<td><ul>
<li><span data-ttu-id="170a8-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="170a8-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="170a8-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="170a8-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="170a8-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="170a8-166">Il set di proprietà include le proprietà del controllo dello scanner di Feeder, in genere l'immagine e il set di proprietà specifico del documento</span><span class="sxs-lookup"><span data-stu-id="170a8-166">Property set includes feeder scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="170a8-167">Elementi del feed WIA, inclusi gli elementi figlio che rappresentano le pagine iniziali e secondarie di un documento.</span><span class="sxs-lookup"><span data-stu-id="170a8-167">WIA Feeder items, including child items that represent the front and back pages of a document.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="170a8-168">WIA_CATEGORY_FILM</span><span class="sxs-lookup"><span data-stu-id="170a8-168">WIA_CATEGORY_FILM</span></span></td>
<td><ul>
<li><span data-ttu-id="170a8-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="170a8-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="170a8-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="170a8-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="170a8-173">Il set di proprietà include le proprietà del controllo dello scanner di film (in genere immagini e set di proprietà specifiche del documento).</span><span class="sxs-lookup"><span data-stu-id="170a8-173">Property set includes film scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="170a8-174">Elementi di film WIA, inclusi gli elementi figlio che rappresentano i singoli frame di analisi.</span><span class="sxs-lookup"><span data-stu-id="170a8-174">WIA Film items, including child items that represent the individual scanning frames.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="170a8-175">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="170a8-175">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><ul>
<li><span data-ttu-id="170a8-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
<li><span data-ttu-id="170a8-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="170a8-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span></span></li>
<li><span data-ttu-id="170a8-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span></span></li>
<li><span data-ttu-id="170a8-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="170a8-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="170a8-182">Il set di proprietà per questo elemento dipende dal tipo di elemento segnalato.</span><span class="sxs-lookup"><span data-stu-id="170a8-182">The property set on this item depends on the item type reported.</span></span> <span data-ttu-id="170a8-183">Ad esempio, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> deve includere alcune proprietà dell'elemento immagine, come bits per pixel e così via.</span><span class="sxs-lookup"><span data-stu-id="170a8-183">For example, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> should include some image item properties, like bits per pixel and so forth.</span></span></td>
<td><span data-ttu-id="170a8-184">Elementi di archiviazione WIA, inclusi gli elementi figlio che rappresentano il contenuto del file completato (file di dati quali JPEG, HTML, TXT e così via).</span><span class="sxs-lookup"><span data-stu-id="170a8-184">WIA storage items, including child items that represent finished file content (data files like JPEG, HTML, TXT, and so forth).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="170a8-185">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="170a8-185">WIA_CATEGORY_FLATBED</span></span></td>
<td><ul>
<li><span data-ttu-id="170a8-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="170a8-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="170a8-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="170a8-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="170a8-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="170a8-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>: può essere presente se lo scanner supporta l'analisi a più elementi.</span><span class="sxs-lookup"><span data-stu-id="170a8-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>—may be present if the scanner supports multi-item scanning.</span></span></li>
<li><span data-ttu-id="170a8-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>: può essere presente se l'applicazione genera un elemento WIA durante una sessione di analisi di più elementi.</span><span class="sxs-lookup"><span data-stu-id="170a8-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>—may be present if the application generates a WIA item during a multi-item scanning session.</span></span></li>
</ul></td>
<td><span data-ttu-id="170a8-192">Il set di proprietà include le proprietà del controllo scanner piano (in genere l'immagine e il set di proprietà specifico del documento).</span><span class="sxs-lookup"><span data-stu-id="170a8-192">The property set includes flatbed scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="170a8-193">Gli elementi del piano WIA, inclusi gli elementi figlio che rappresentano le aree sottoposte ad analisi sulla piastra piana dello scanner.</span><span class="sxs-lookup"><span data-stu-id="170a8-193">WIA flatbed items, including child items that represent regions being scanned on the scanner's flatbed platen.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="170a8-194">Il grafico seguente mostra un esempio di albero degli elementi WIA e le varie categorie che possono essere associate a ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="170a8-194">The following graphic shows an example of a WIA item tree and the various categories that might be associated with each item.</span></span>

![esempi di categorie di elementi per gli elementi in un albero](images/scannertree2.jpg)

## <a name="root-item"></a><span data-ttu-id="170a8-196">Elemento radice</span><span class="sxs-lookup"><span data-stu-id="170a8-196">Root Item</span></span>

<span data-ttu-id="170a8-197">Un elemento radice WIA è un elemento di cartella contrassegnato con i flag [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) e **WiaItemTypeDevice** che rappresenta il dispositivo stesso.</span><span class="sxs-lookup"><span data-stu-id="170a8-197">A WIA root item is a folder item marked with [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) and **WiaItemTypeDevice** flags that represents the device itself.</span></span> <span data-ttu-id="170a8-198">Contiene attributi del dispositivo come il produttore, il nome del dispositivo e gli attributi del driver, ad esempio la versione del driver e l'identificatore di classe dell'interfaccia utente (CLSID).</span><span class="sxs-lookup"><span data-stu-id="170a8-198">It contains device attributes like manufacturer, device name, and driver attributes like driver version and user interface class identifier (CLSID).</span></span> <span data-ttu-id="170a8-199">Le applicazioni per la creazione di immagini ottengono la radice nell'albero degli elementi WIA chiamando il metodo [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="170a8-199">Imaging applications get the root to the WIA item tree by calling [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) method.</span></span> <span data-ttu-id="170a8-200">L'applicazione usa l'elemento radice per accedere ai singoli elementi WIA figlio enumerando l'albero (vedere [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span><span class="sxs-lookup"><span data-stu-id="170a8-200">The application uses the root item to gain access to the individual child WIA items by enumerating the tree (see [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span></span>

## <a name="data-item"></a><span data-ttu-id="170a8-201">DataItem</span><span class="sxs-lookup"><span data-stu-id="170a8-201">Data Item</span></span>

<span data-ttu-id="170a8-202">Qualsiasi elemento che può essere utilizzato per trasferire i dati viene considerato un elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="170a8-202">Any item that can be use to transfer data is considered a data item.</span></span> <span data-ttu-id="170a8-203">Sono inclusi gli elementi contrassegnati con il flag [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="170a8-203">This includes items marked with the [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) flag.</span></span>

<span data-ttu-id="170a8-204">Gli elementi della cartella e gli elementi non cartella possono esporre la possibilità di trasferire i dati tramite la funzione contrassegnata con il flag [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="170a8-204">Folder items and nonfolder items can expose the ability to transfer data by being marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag.</span></span> <span data-ttu-id="170a8-205">Qualsiasi elemento con questo set di flag deve fornire le seguenti proprietà dell'elemento WIA:</span><span class="sxs-lookup"><span data-stu-id="170a8-205">Any item with this flag set has to provide the following WIA item properties:</span></span>

-   [<span data-ttu-id="170a8-206">**\_diritti di \_ accesso con IPA WIA \_**</span><span class="sxs-lookup"><span data-stu-id="170a8-206">**WIA\_IPA\_ACCESS\_RIGHTS**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="170a8-207">**\_ \_ dimensioni elemento IPA \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="170a8-207">**WIA\_IPA\_ITEM\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="170a8-208">**\_dimensioni del \_ buffer \_ IPA WIA**</span><span class="sxs-lookup"><span data-stu-id="170a8-208">**WIA\_IPA\_BUFFER\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="170a8-209">**\_formato ipa \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="170a8-209">**WIA\_IPA\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="170a8-210">**\_ \_ formato preferito dell'IPA WIA \_**</span><span class="sxs-lookup"><span data-stu-id="170a8-210">**WIA\_IPA\_PREFERRED\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="170a8-211">**\_TYMED IPA \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="170a8-211">**WIA\_IPA\_TYMED**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="170a8-212">**\_estensione del \_ nome file IPA WIA \_**</span><span class="sxs-lookup"><span data-stu-id="170a8-212">**WIA\_IPA\_FILENAME\_EXTENSION**</span></span>](-wia-wiaitempropcommonitem.md)

<span data-ttu-id="170a8-213">Le origini dati programmabili contrassegnate con il flag [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) devono anche fornire il set di proprietà obbligatorio per l'elemento dati.</span><span class="sxs-lookup"><span data-stu-id="170a8-213">Programmable data source items marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag must also supply the data item required property set.</span></span>

<span data-ttu-id="170a8-214">Gli elementi di dati WIA possono avere proprietà aggiuntive a seconda delle impostazioni dei flag dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="170a8-214">WIA data items may have additional properties depending on the item's flag settings.</span></span> <span data-ttu-id="170a8-215">Ad esempio, gli elementi WIA contrassegnati con il flag [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) devono avere proprietà delle informazioni specifiche dell'immagine, ad esempio la [**\_ \_ profondità dell'IPA WIA**](-wia-wiaitempropcommonitem.md) e il **\_ \_ numero \_ di \_ righe dell'IPA WIA**.</span><span class="sxs-lookup"><span data-stu-id="170a8-215">For example, WIA items marked with the [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) flag should have image specific information properties, like [**WIA\_IPA\_DEPTH**](-wia-wiaitempropcommonitem.md) and **WIA\_IPA\_NUMBER\_OF\_LINES**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="170a8-216">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="170a8-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="170a8-217">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="170a8-217">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="170a8-218">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="170a8-218">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="170a8-219">**IEnumWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="170a8-219">**IEnumWiaItem2**</span></span>](-wia-ienumwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="170a8-220">**IWiaDevMgr2**</span><span class="sxs-lookup"><span data-stu-id="170a8-220">**IWiaDevMgr2**</span></span>](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



