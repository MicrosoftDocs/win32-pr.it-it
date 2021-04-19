---
description: Il valore della proprietà ADDSOURCE è un elenco di funzioni delimitate da virgole e deve essere installato per l'esecuzione dall'origine.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: Proprietà ADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd51d6f86060def1a7536134a0041f1e15178a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333578"
---
# <a name="addsource-property"></a><span data-ttu-id="9283e-103">Proprietà ADDSOURCE</span><span class="sxs-lookup"><span data-stu-id="9283e-103">ADDSOURCE property</span></span>

<span data-ttu-id="9283e-104">Il valore della proprietà **addsource** è un elenco di funzioni delimitate da virgole e deve essere installato per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="9283e-104">The value of the **ADDSOURCE** property is a list of features that are delimited by commas, and are to be installed to run from the source.</span></span> <span data-ttu-id="9283e-105">Le funzionalità devono essere presenti nella colonna funzionalità della tabella delle [funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="9283e-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="9283e-106">Per installare tutte le funzionalità come eseguite dall'origine, usare ADDSOURCE = ALL nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9283e-106">To install all features as run from source, use ADDSOURCE=ALL on the command line.</span></span> <span data-ttu-id="9283e-107">Non immettere ADDSOURCE = ALL nella tabella delle [Proprietà](property-table.md), perché in questo modo viene generato un pacchetto di esecuzione da un'origine che non può essere rimosso correttamente.</span><span class="sxs-lookup"><span data-stu-id="9283e-107">Do not enter ADDSOURCE=ALL into the [Property Table](property-table.md), because this generates a run-from-source package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9283e-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9283e-108">Remarks</span></span>

<span data-ttu-id="9283e-109">I nomi delle funzionalità fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="9283e-109">The feature names are case sensitive.</span></span> <span data-ttu-id="9283e-110">Se il flag di bit LocalOnly è impostato nella colonna attributi della [tabella dei componenti](component-table.md) per un componente di una funzionalità nell'elenco, tale componente viene installato per l'esecuzione in locale.</span><span class="sxs-lookup"><span data-stu-id="9283e-110">If the LocalOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed to run locally.</span></span>

<span data-ttu-id="9283e-111">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="9283e-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="9283e-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9283e-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="9283e-113">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="9283e-113">**REMOVE**</span></span>](remove.md)
3.  <span data-ttu-id="9283e-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9283e-114">**ADDSOURCE**</span></span>
4.  [<span data-ttu-id="9283e-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9283e-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="9283e-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="9283e-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="9283e-117">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="9283e-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="9283e-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9283e-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="9283e-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9283e-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="9283e-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9283e-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="9283e-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9283e-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="9283e-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9283e-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="9283e-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9283e-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="9283e-124">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9283e-124">For example:</span></span>

-   <span data-ttu-id="9283e-125">Se la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = **funzionalità**, tutte le funzionalità vengono prima impostate su run-local, quindi la **funzionalità** è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="9283e-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="9283e-126">Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la **funzionalità**, First **funzionalità** è impostata su run-local e quindi quando viene valutato addsource = all, tutte le funzionalità (inclusa la **funzionalità**) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="9283e-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="9283e-127">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9283e-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="9283e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9283e-128">Requirements</span></span>



| <span data-ttu-id="9283e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9283e-129">Requirement</span></span> | <span data-ttu-id="9283e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="9283e-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9283e-131">Versione</span><span class="sxs-lookup"><span data-stu-id="9283e-131">Version</span></span><br/> | <span data-ttu-id="9283e-132">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9283e-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9283e-133">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9283e-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9283e-134">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9283e-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9283e-135">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9283e-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9283e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9283e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9283e-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9283e-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




