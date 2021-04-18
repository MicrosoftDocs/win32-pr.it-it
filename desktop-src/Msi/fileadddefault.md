---
description: Il valore della proprietà FILEADDDEFAULT è un elenco di chiavi di file delimitate da virgole installate nella configurazione predefinita.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: Proprietà FILEADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324780"
---
# <a name="fileadddefault-property"></a><span data-ttu-id="11778-103">Proprietà FILEADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="11778-103">FILEADDDEFAULT property</span></span>

<span data-ttu-id="11778-104">Il valore della proprietà **FILEADDDEFAULT** è un elenco di chiavi di file delimitate da virgole installate nella configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="11778-104">The value of the **FILEADDDEFAULT** property is a list of file keys delimited by commas that are installed in their default configuration.</span></span> <span data-ttu-id="11778-105">Per ogni chiave file nell'elenco, il programma di installazione determina il componente che controlla il file e installa la funzionalità che richiede lo spazio su disco minimo.</span><span class="sxs-lookup"><span data-stu-id="11778-105">For each file key in the list, the installer determines the component that controls that file and installs the feature that requires the least disk space.</span></span> <span data-ttu-id="11778-106">Le chiavi del file nell'elenco devono essere presenti nella colonna file della tabella [file](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="11778-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="11778-107">Una funzionalità viene installata nello stesso stato di installazione come se l'utente avesse richiesto un'installazione su richiesta della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="11778-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="11778-108">Lo stato è determinato dai bit impostati per la funzionalità nella colonna attributi della [tabella delle funzionalità](feature-table.md)e dai bit impostati per i componenti della funzionalità nella colonna attributi della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="11778-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="11778-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="11778-109">Remarks</span></span>

<span data-ttu-id="11778-110">Si noti che i nomi delle chiavi del file fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="11778-110">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="11778-111">Si noti inoltre che se il flag di bit SourceOnly è impostato nella colonna attributi della tabella dei [componenti](component-table.md) per un componente, il componente viene installato per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="11778-111">Also note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="11778-112">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente.</span><span class="sxs-lookup"><span data-stu-id="11778-112">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="11778-113">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="11778-113">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="11778-114">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="11778-114">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="11778-115">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="11778-115">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="11778-116">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="11778-116">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="11778-117">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="11778-117">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="11778-118">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="11778-118">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="11778-119">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="11778-119">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="11778-120">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="11778-120">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="11778-121">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="11778-121">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="11778-122">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="11778-122">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="11778-123">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="11778-123">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. <span data-ttu-id="11778-124">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="11778-124">**FILEADDDEFAULT**</span></span>

<span data-ttu-id="11778-125">Se, ad esempio, la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = la funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la funzionalità è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="11778-125">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="11778-126">Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la funzionalità, First funzionalità è impostata su run-local e quindi quando viene valutato ADDSOURCE = ALL, tutte le funzionalità (inclusa la funzionalità) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="11778-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="11778-127">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="11778-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="11778-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11778-128">Requirements</span></span>



| <span data-ttu-id="11778-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="11778-129">Requirement</span></span> | <span data-ttu-id="11778-130">Valore</span><span class="sxs-lookup"><span data-stu-id="11778-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11778-131">Versione</span><span class="sxs-lookup"><span data-stu-id="11778-131">Version</span></span><br/> | <span data-ttu-id="11778-132">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11778-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="11778-133">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11778-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="11778-134">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="11778-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="11778-135">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="11778-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11778-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11778-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11778-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="11778-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




