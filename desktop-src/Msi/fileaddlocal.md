---
description: Il valore della proprietà FILEADDLOCAL indica un elenco di chiavi di file delimitate da virgole da installare per l'esecuzione dal supporto di origine locale.
ms.assetid: 89ae876e-53f0-4c1d-ba16-7513af79ee5e
title: Proprietà FILEADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e3e05a35e5bcd4fc672a2feb6bd2f40619bfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324779"
---
# <a name="fileaddlocal-property"></a><span data-ttu-id="83401-103">Proprietà FILEADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="83401-103">FILEADDLOCAL property</span></span>

<span data-ttu-id="83401-104">Il valore della proprietà **FILEADDLOCAL** indica un elenco di chiavi di file delimitate da virgole da installare per l'esecuzione dal supporto di origine locale.</span><span class="sxs-lookup"><span data-stu-id="83401-104">The value of the **FILEADDLOCAL** property denotes a list of file keys delimited by commas that are to be installed to run from the local source media.</span></span> <span data-ttu-id="83401-105">Per ogni chiave file nell'elenco, il programma di installazione determina il componente che controlla il file, quindi esamina tutte le funzionalità collegate a tale componente dalla tabella [FeatureComponents](featurecomponents-table.md) e installa la funzionalità che richiede la quantità minima di spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="83401-105">For each file key in the list, the installer determines the component that controls that file, then examines all features linked to that component by the [FeatureComponents](featurecomponents-table.md) table and installs the feature that requires the least amount of disk space.</span></span> <span data-ttu-id="83401-106">Le chiavi del file nell'elenco devono essere presenti nella colonna file della tabella [file](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="83401-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="83401-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="83401-107">Remarks</span></span>

<span data-ttu-id="83401-108">Si noti che i nomi delle chiavi del file fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="83401-108">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="83401-109">Si noti inoltre che se il flag di bit LocalOnly è impostato nella colonna attributi della tabella dei [componenti](component-table.md) per un componente, il componente viene installato per l'esecuzione in locale.</span><span class="sxs-lookup"><span data-stu-id="83401-109">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="83401-110">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente.</span><span class="sxs-lookup"><span data-stu-id="83401-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="83401-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="83401-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="83401-112">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="83401-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="83401-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="83401-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="83401-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="83401-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="83401-115">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="83401-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="83401-116">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="83401-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="83401-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="83401-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="83401-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="83401-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="83401-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="83401-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. <span data-ttu-id="83401-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="83401-120">**FILEADDLOCAL**</span></span>
11. [<span data-ttu-id="83401-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="83401-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="83401-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="83401-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="83401-123">Se, ad esempio, la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = la funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la funzionalità è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="83401-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="83401-124">Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la funzionalità, First funzionalità è impostata su run-local e quindi quando viene valutato ADDSOURCE = ALL, tutte le funzionalità (inclusa la funzionalità) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="83401-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="83401-125">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="83401-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="83401-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83401-126">Requirements</span></span>



| <span data-ttu-id="83401-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="83401-127">Requirement</span></span> | <span data-ttu-id="83401-128">Valore</span><span class="sxs-lookup"><span data-stu-id="83401-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83401-129">Versione</span><span class="sxs-lookup"><span data-stu-id="83401-129">Version</span></span><br/> | <span data-ttu-id="83401-130">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="83401-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="83401-131">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="83401-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="83401-132">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83401-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="83401-133">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="83401-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83401-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83401-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83401-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83401-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




