---
description: Il valore della proprietà COMPADDDEFAULT è un elenco di GUID del componente della colonna ComponentId della tabella Component, delimitati da virgole, che vengono installati nella configurazione predefinita.
ms.assetid: 1bf05680-fcba-4fbb-8f8c-4203a90346ce
title: Proprietà COMPADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e96d2259f0610a3030e79f8685c498a0fb2d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326901"
---
# <a name="compadddefault-property"></a><span data-ttu-id="49d4c-103">Proprietà COMPADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="49d4c-103">COMPADDDEFAULT property</span></span>

<span data-ttu-id="49d4c-104">Il valore della proprietà **COMPADDDEFAULT** è un elenco di GUID del componente della colonna ComponentID della [tabella Component](component-table.md), delimitati da virgole, che vengono installati nella configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="49d4c-104">The value of the **COMPADDDEFAULT** property is a list of component GUIDs from the ComponentId column of the [Component table](component-table.md), delimited by commas, that are installed in their default configuration.</span></span> <span data-ttu-id="49d4c-105">Per ogni ID componente nell'elenco, il programma di installazione installa la funzionalità che richiede lo spazio minimo su disco.</span><span class="sxs-lookup"><span data-stu-id="49d4c-105">For each component ID in the list, the installer installs the feature that requires the least disk space.</span></span> <span data-ttu-id="49d4c-106">Gli ID componente nell'elenco devono essere presenti nella colonna ComponentId della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="49d4c-106">The component IDs in the list must be present in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="49d4c-107">Una funzionalità viene installata nello stesso stato di installazione come se l'utente avesse richiesto un'installazione su richiesta della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="49d4c-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="49d4c-108">Lo stato è determinato dai bit impostati per la funzionalità nella colonna attributi della [tabella delle funzionalità](feature-table.md)e dai bit impostati per i componenti della funzionalità nella colonna attributi della tabella dei componenti.</span><span class="sxs-lookup"><span data-stu-id="49d4c-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="49d4c-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="49d4c-109">Remarks</span></span>

<span data-ttu-id="49d4c-110">Si noti che se il flag di bit SourceOnly è impostato nella colonna attributi della tabella dei [componenti](component-table.md) per un componente, il componente viene installato per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="49d4c-110">Note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="49d4c-111">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente.</span><span class="sxs-lookup"><span data-stu-id="49d4c-111">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="49d4c-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="49d4c-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="49d4c-113">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="49d4c-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="49d4c-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="49d4c-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="49d4c-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="49d4c-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="49d4c-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="49d4c-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="49d4c-117">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="49d4c-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="49d4c-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="49d4c-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="49d4c-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="49d4c-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  <span data-ttu-id="49d4c-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="49d4c-120">**COMPADDDEFAULT**</span></span>
10. [<span data-ttu-id="49d4c-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="49d4c-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="49d4c-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="49d4c-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="49d4c-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="49d4c-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="49d4c-124">Se, ad esempio, la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = la funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la funzionalità è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="49d4c-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="49d4c-125">Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la funzionalità, First funzionalità è impostata su run-local e quindi quando viene valutato ADDSOURCE = ALL, tutte le funzionalità (inclusa la funzionalità) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="49d4c-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="49d4c-126">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="49d4c-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="49d4c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49d4c-127">Requirements</span></span>



| <span data-ttu-id="49d4c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="49d4c-128">Requirement</span></span> | <span data-ttu-id="49d4c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="49d4c-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49d4c-130">Versione</span><span class="sxs-lookup"><span data-stu-id="49d4c-130">Version</span></span><br/> | <span data-ttu-id="49d4c-131">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="49d4c-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="49d4c-132">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="49d4c-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="49d4c-133">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="49d4c-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="49d4c-134">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="49d4c-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49d4c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49d4c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d4c-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="49d4c-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




