---
description: Il valore della proprietà ADDLOCAL è un elenco di funzioni delimitate da virgole e devono essere installate localmente.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: Proprietà ADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333580"
---
# <a name="addlocal-property"></a><span data-ttu-id="9dc29-103">Proprietà ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="9dc29-103">ADDLOCAL property</span></span>

<span data-ttu-id="9dc29-104">Il valore della proprietà **ADDLOCAL** è un elenco di funzioni delimitate da virgole e devono essere installate localmente.</span><span class="sxs-lookup"><span data-stu-id="9dc29-104">The value of the **ADDLOCAL** property is a list of features that are delimited by commas, and are to be installed locally.</span></span> <span data-ttu-id="9dc29-105">Le funzionalità devono essere presenti nella colonna funzionalità della tabella delle [funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="9dc29-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="9dc29-106">Per installare tutte le funzionalità localmente, usare ADDLOCAL = ALL nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9dc29-106">To install all features locally, use ADDLOCAL=ALL on the command line.</span></span> <span data-ttu-id="9dc29-107">Non immettere ADDLOCAL = ALL nella tabella delle [Proprietà](property-table.md), perché questo genera un pacchetto installato localmente che non può essere rimosso correttamente.</span><span class="sxs-lookup"><span data-stu-id="9dc29-107">Do not enter ADDLOCAL=ALL into the [Property Table](property-table.md), because this generates a locally installed package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dc29-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dc29-108">Remarks</span></span>

<span data-ttu-id="9dc29-109">I nomi delle funzionalità fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="9dc29-109">Feature names are case sensitive.</span></span> <span data-ttu-id="9dc29-110">Se il flag di bit SourceOnly è impostato nella colonna attributi della [tabella dei componenti](component-table.md) per un componente di una funzionalità nell'elenco, tale componente viene installato come eseguito dall'origine.</span><span class="sxs-lookup"><span data-stu-id="9dc29-110">If the SourceOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed as run from source.</span></span>

<span data-ttu-id="9dc29-111">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="9dc29-111">The installer always evaluates the following properties in the following order:</span></span>

1.  <span data-ttu-id="9dc29-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9dc29-112">**ADDLOCAL**</span></span>
2.  [<span data-ttu-id="9dc29-113">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="9dc29-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="9dc29-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9dc29-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="9dc29-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9dc29-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="9dc29-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="9dc29-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="9dc29-117">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="9dc29-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="9dc29-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9dc29-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="9dc29-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9dc29-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="9dc29-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9dc29-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="9dc29-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9dc29-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="9dc29-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9dc29-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="9dc29-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9dc29-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="9dc29-124">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9dc29-124">For example:</span></span>

-   <span data-ttu-id="9dc29-125">Se la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = **funzionalità**, tutte le funzionalità vengono prima impostate su run-local, quindi la **funzionalità** è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="9dc29-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="9dc29-126">Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la **funzionalità**, First **funzionalità** è impostata su run-local e quindi quando viene valutato addsource = all, tutte le funzionalità (inclusa la **funzionalità**) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="9dc29-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="9dc29-127">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà precedenti viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9dc29-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the previous properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dc29-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dc29-128">Requirements</span></span>



| <span data-ttu-id="9dc29-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dc29-129">Requirement</span></span> | <span data-ttu-id="9dc29-130">Valore</span><span class="sxs-lookup"><span data-stu-id="9dc29-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dc29-131">Versione</span><span class="sxs-lookup"><span data-stu-id="9dc29-131">Version</span></span><br/> | <span data-ttu-id="9dc29-132">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9dc29-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9dc29-133">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9dc29-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9dc29-134">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9dc29-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9dc29-135">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9dc29-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dc29-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dc29-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dc29-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9dc29-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




