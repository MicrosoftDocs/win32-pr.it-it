---
description: Il valore della proprietà REINSTALL è un elenco di funzionalità delimitate da virgole da reinstallare. Le funzionalità elencate devono essere presenti nella colonna funzionalità della tabella delle funzionalità. Per reinstallare tutte le funzionalità, usare REINSTALL = ALL nella riga di comando.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: Reinstalla proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328554"
---
# <a name="reinstall-property"></a><span data-ttu-id="da882-105">Reinstalla proprietà</span><span class="sxs-lookup"><span data-stu-id="da882-105">REINSTALL property</span></span>

<span data-ttu-id="da882-106">Il valore della proprietà **REINSTALL** è un elenco di funzionalità delimitate da virgole da reinstallare.</span><span class="sxs-lookup"><span data-stu-id="da882-106">The value of the **REINSTALL** property is a list of features delimited by commas that are to be reinstalled.</span></span> <span data-ttu-id="da882-107">Le funzionalità elencate devono essere presenti nella colonna funzionalità della tabella delle [funzionalità](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="da882-107">The features listed must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="da882-108">Per reinstallare tutte le funzionalità, usare REINSTALL = ALL nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="da882-108">To reinstall all features use REINSTALL=ALL on the command line.</span></span>

## <a name="remarks"></a><span data-ttu-id="da882-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="da882-109">Remarks</span></span>

<span data-ttu-id="da882-110">Si noti che i nomi delle funzionalità fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="da882-110">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="da882-111">Se la proprietà **REINSTALL** è impostata, è necessario impostare anche la proprietà [**REINSTALLMODE**](reinstallmode.md) per indicare il tipo di reinstallazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="da882-111">If the **REINSTALL** property is set, the [**REINSTALLMODE**](reinstallmode.md) property should also be set, to indicate the type of reinstall to be performed.</span></span> <span data-ttu-id="da882-112">Se la proprietà **REINSTALLMODE** non è impostata, per impostazione predefinita tutti i file attualmente installati vengono reinstallati, se la versione del file attualmente installata è minore o non è presente.</span><span class="sxs-lookup"><span data-stu-id="da882-112">If the **REINSTALLMODE** property is not set, then by default all files that are currently installed are reinstalled, IF the currently installed file is a lesser version (or is not present).</span></span> <span data-ttu-id="da882-113">Per impostazione predefinita, nessuna voce del registro di sistema viene riscritta.</span><span class="sxs-lookup"><span data-stu-id="da882-113">By default, no registry entries are rewritten.</span></span>

<span data-ttu-id="da882-114">Si noti che anche se **REINSTALL** è impostato su All, verranno reinstallate solo le funzionalità già installate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="da882-114">Note that even if **REINSTALL** is set to ALL, only those features that were already installed previously are reinstalled.</span></span> <span data-ttu-id="da882-115">Pertanto, se **REINSTALL** è impostato per un prodotto ancora da installare, non verrà eseguita alcuna azione di installazione.</span><span class="sxs-lookup"><span data-stu-id="da882-115">Thus, if **REINSTALL** is set for a product that is yet to be installed, no installation action will take place at all.</span></span>

<span data-ttu-id="da882-116">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="da882-116">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="da882-117">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="da882-117">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="da882-118">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="da882-118">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="da882-119">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="da882-119">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="da882-120">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="da882-120">**ADDDEFAULT**</span></span>](adddefault.md)
5.  <span data-ttu-id="da882-121">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="da882-121">**REINSTALL**</span></span>
6.  [<span data-ttu-id="da882-122">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="da882-122">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="da882-123">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="da882-123">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="da882-124">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="da882-124">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="da882-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="da882-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
10. [<span data-ttu-id="da882-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="da882-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
11. [<span data-ttu-id="da882-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="da882-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="da882-128">Se, ad esempio, la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = la funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la funzionalità è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="da882-128">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="da882-129">Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la funzionalità, First funzionalità è impostata su run-local e quindi quando viene valutato ADDSOURCE = ALL, tutte le funzionalità (inclusa la funzionalità) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="da882-129">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="da882-130">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="da882-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="da882-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da882-131">Requirements</span></span>



| <span data-ttu-id="da882-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="da882-132">Requirement</span></span> | <span data-ttu-id="da882-133">Valore</span><span class="sxs-lookup"><span data-stu-id="da882-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da882-134">Versione</span><span class="sxs-lookup"><span data-stu-id="da882-134">Version</span></span><br/> | <span data-ttu-id="da882-135">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="da882-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="da882-136">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="da882-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="da882-137">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="da882-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="da882-138">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="da882-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da882-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da882-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da882-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da882-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




