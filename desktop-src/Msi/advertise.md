---
description: Il valore della proprietà ADVERTISe è un elenco di funzionalità delimitate da virgole da annunciare.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: Pubblicizza proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e768f22f86dacf35009ca0e0e3ef9337ef84ab70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330285"
---
# <a name="advertise-property"></a><span data-ttu-id="a07b4-103">Pubblicizza proprietà</span><span class="sxs-lookup"><span data-stu-id="a07b4-103">ADVERTISE property</span></span>

<span data-ttu-id="a07b4-104">Il valore della proprietà **advertise** è un elenco di funzionalità delimitate da virgole da annunciare.</span><span class="sxs-lookup"><span data-stu-id="a07b4-104">The value of the **ADVERTISE** property is a list of features delimited by commas that are to be advertised.</span></span> <span data-ttu-id="a07b4-105">Le funzionalità devono essere presenti nella colonna funzionalità della tabella delle [funzionalità](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a07b4-105">The features must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="a07b4-106">Per installare tutte le funzionalità come pubblicizzate, usare ADVERTISe = ALL nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="a07b4-106">To install all features as advertised, use ADVERTISE=ALL on the command line.</span></span> <span data-ttu-id="a07b4-107">Non immettere ADVERTISe = ALL nella [tabella delle proprietà](property-table.md) perché genera un pacchetto annunciato che non può essere installato o rimosso.</span><span class="sxs-lookup"><span data-stu-id="a07b4-107">Do not enter ADVERTISE=ALL into the [Property table](property-table.md) because this generates an advertised package that cannot be installed or removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a07b4-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="a07b4-108">Remarks</span></span>

<span data-ttu-id="a07b4-109">Si noti che i nomi di funzionalità fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a07b4-109">Note that feature names are case-sensitive.</span></span>

<span data-ttu-id="a07b4-110">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente.</span><span class="sxs-lookup"><span data-stu-id="a07b4-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="a07b4-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="a07b4-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="a07b4-112">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="a07b4-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="a07b4-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a07b4-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="a07b4-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a07b4-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="a07b4-115">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="a07b4-115">**REINSTALL**</span></span>](reinstall.md)
6.  <span data-ttu-id="a07b4-116">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="a07b4-116">**ADVERTISE**</span></span>
7.  [<span data-ttu-id="a07b4-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="a07b4-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="a07b4-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a07b4-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="a07b4-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a07b4-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="a07b4-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="a07b4-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="a07b4-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a07b4-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="a07b4-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a07b4-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="a07b4-123">Se, ad esempio, la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = la funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la funzionalità è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="a07b4-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="a07b4-124">Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la funzionalità, First funzionalità è impostata su run-local e quindi quando viene valutato ADDSOURCE = ALL, tutte le funzionalità (inclusa la funzionalità) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="a07b4-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="a07b4-125">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="a07b4-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="a07b4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a07b4-126">Requirements</span></span>



| <span data-ttu-id="a07b4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a07b4-127">Requirement</span></span> | <span data-ttu-id="a07b4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a07b4-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a07b4-129">Versione</span><span class="sxs-lookup"><span data-stu-id="a07b4-129">Version</span></span><br/> | <span data-ttu-id="a07b4-130">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a07b4-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a07b4-131">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a07b4-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a07b4-132">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a07b4-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a07b4-133">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a07b4-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a07b4-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a07b4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a07b4-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a07b4-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




