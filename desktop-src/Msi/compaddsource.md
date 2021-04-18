---
description: Il valore della proprietà COMPADDSOURCE è un elenco di GUID del componente della colonna ComponentId della tabella Component, delimitati da virgole, che devono essere installati per l'esecuzione dal supporto di origine.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: Proprietà COMPADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326900"
---
# <a name="compaddsource-property"></a><span data-ttu-id="289fd-103">Proprietà COMPADDSOURCE</span><span class="sxs-lookup"><span data-stu-id="289fd-103">COMPADDSOURCE property</span></span>

<span data-ttu-id="289fd-104">Il valore della proprietà **COMPADDSOURCE** è un elenco di GUID del componente della colonna ComponentID della tabella [Component](component-table.md) , delimitati da virgole, che devono essere installati per l'esecuzione dal supporto di origine.</span><span class="sxs-lookup"><span data-stu-id="289fd-104">The value of the **COMPADDSOURCE** property is a list of component GUIDs from the ComponentId column of the [Component](component-table.md) table, delimited by commas, that are to be installed to run from the source media.</span></span> <span data-ttu-id="289fd-105">Il programma di installazione utilizza questo valore per determinare quali funzionalità sono impostate per essere installate per l'esecuzione dall'origine, in base ai componenti specificati.</span><span class="sxs-lookup"><span data-stu-id="289fd-105">The installer uses this value to determine which features are set to be installed to run from source, based on the specified components.</span></span> <span data-ttu-id="289fd-106">Per ogni ID componente elencato, il programma di installazione esamina tutte le funzionalità collegate (tramite la tabella [FeatureComponents](featurecomponents-table.md) ) a tale componente e installa la funzionalità che richiede la quantità minima di spazio su disco per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="289fd-106">For each listed component ID, the installer examines all features linked (through the [FeatureComponents](featurecomponents-table.md) table) to that component, and installs the feature that requires the least amount of disk space to install.</span></span> <span data-ttu-id="289fd-107">I componenti elencati devono essere presenti nella colonna componente della tabella dei [componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="289fd-107">The components listed must be present in the Component column of the [Component](component-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="289fd-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="289fd-108">Remarks</span></span>

<span data-ttu-id="289fd-109">Si noti che i nomi dei componenti fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="289fd-109">Note that the component names are case-sensitive.</span></span> <span data-ttu-id="289fd-110">Si noti inoltre che se il flag di bit LocalOnly è impostato nella colonna attributi della tabella dei [componenti](component-table.md) per un componente, il componente viene installato per l'esecuzione in locale.</span><span class="sxs-lookup"><span data-stu-id="289fd-110">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="289fd-111">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="289fd-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="289fd-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="289fd-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="289fd-113">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="289fd-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="289fd-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="289fd-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="289fd-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="289fd-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="289fd-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="289fd-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="289fd-117">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="289fd-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="289fd-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="289fd-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  <span data-ttu-id="289fd-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="289fd-119">**COMPADDSOURCE**</span></span>
9.  [<span data-ttu-id="289fd-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="289fd-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="289fd-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="289fd-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="289fd-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="289fd-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="289fd-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="289fd-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="289fd-124">Se, ad esempio, la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = la funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la funzionalità è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="289fd-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="289fd-125">Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la funzionalità, First funzionalità è impostata su run-local e quindi quando viene valutato ADDSOURCE = ALL, tutte le funzionalità (inclusa la funzionalità) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="289fd-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="289fd-126">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="289fd-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="289fd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="289fd-127">Requirements</span></span>



| <span data-ttu-id="289fd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="289fd-128">Requirement</span></span> | <span data-ttu-id="289fd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="289fd-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="289fd-130">Versione</span><span class="sxs-lookup"><span data-stu-id="289fd-130">Version</span></span><br/> | <span data-ttu-id="289fd-131">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="289fd-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="289fd-132">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="289fd-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="289fd-133">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="289fd-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="289fd-134">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="289fd-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="289fd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="289fd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="289fd-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="289fd-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




