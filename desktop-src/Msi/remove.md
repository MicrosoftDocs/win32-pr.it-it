---
description: Il valore della proprietà REMOVE è un elenco di funzioni delimitate da virgole da rimuovere.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE - proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332606"
---
# <a name="remove-property"></a><span data-ttu-id="0687e-103">REMOVE - proprietà</span><span class="sxs-lookup"><span data-stu-id="0687e-103">REMOVE property</span></span>

<span data-ttu-id="0687e-104">Il valore della proprietà **Remove** è un elenco di funzioni delimitate da virgole da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0687e-104">The value of the **REMOVE** property is a list of features delimited by commas that are to be removed.</span></span> <span data-ttu-id="0687e-105">Le funzionalità devono essere presenti nella colonna funzionalità della tabella delle [funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="0687e-105">The features must be present in the Feature column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="0687e-106">Si noti che se si usa REMOVE = ALL nella riga di comando, il programma di installazione rimuove tutte le funzionalità con un livello di installazione maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="0687e-106">Note that if you use REMOVE=ALL on the command line, the installer removes all features having an install level greater than 0.</span></span> <span data-ttu-id="0687e-107">In questo caso, il programma di installazione non rimuove le funzionalità che hanno un livello di installazione pari a 0.</span><span class="sxs-lookup"><span data-stu-id="0687e-107">In this case, the installer does not remove features having an install level of 0.</span></span> <span data-ttu-id="0687e-108">Per ulteriori informazioni sul livello di installazione delle funzionalità, vedere [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="0687e-108">For more information about the install level of features see [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0687e-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0687e-109">Remarks</span></span>

<span data-ttu-id="0687e-110">Per determinare se un prodotto è stato impostato per la disinstallazione completa, l'autore di un pacchetto può utilizzare un'espressione condizionale per verificare se REMOVE = ALL.</span><span class="sxs-lookup"><span data-stu-id="0687e-110">To determine whether a product has been set to be completely uninstalled, a package author may use a conditional expression to check whether REMOVE=ALL.</span></span> <span data-ttu-id="0687e-111">Si noti che se il prodotto viene rimosso impostando la funzionalità principale su assente, la proprietà **Remove** potrebbe non essere uguale a All fino a dopo l' [azione InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="0687e-111">Note that if the product is removed by setting its top feature to absent, the **REMOVE** property may not equal ALL until after the [InstallValidate action](installvalidate-action.md).</span></span> <span data-ttu-id="0687e-112">Ciò significa che qualsiasi azione personalizzata che dipende da REMOVE = ALL deve essere sequenziata dopo InstallValidate.</span><span class="sxs-lookup"><span data-stu-id="0687e-112">This means that any custom action that depends upon REMOVE=ALL must be sequenced after the InstallValidate.</span></span> <span data-ttu-id="0687e-113">Per ulteriori informazioni, vedere anche [condizionare le azioni da eseguire durante la rimozione](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="0687e-113">For more information see also [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span> <span data-ttu-id="0687e-114">Si noti che i nomi delle funzionalità fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0687e-114">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="0687e-115">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="0687e-115">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="0687e-116">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="0687e-116">**ADDLOCAL**</span></span>](addlocal.md)
2.  <span data-ttu-id="0687e-117">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="0687e-117">**REMOVE**</span></span>
3.  [<span data-ttu-id="0687e-118">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="0687e-118">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="0687e-119">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0687e-119">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="0687e-120">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="0687e-120">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="0687e-121">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="0687e-121">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="0687e-122">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="0687e-122">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="0687e-123">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="0687e-123">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="0687e-124">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0687e-124">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="0687e-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="0687e-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="0687e-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="0687e-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="0687e-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0687e-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="0687e-128">Se, ad esempio, nella riga di comando viene specificato ADDLOCAL = ALL, ADDSOURCE = la funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la funzionalità è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="0687e-128">For example, if the command line specifies ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="0687e-129">Se la riga di comando è ADDSOURCE = ALL, ADDLOCAL = la funzionalità, la prima funzionalità è impostata su run-local, quindi, quando viene valutato ADDSOURCE = ALL, tutte le funzionalità (inclusa la funzionalità) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="0687e-129">If the command line is ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="0687e-130">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="0687e-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="0687e-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0687e-131">Requirements</span></span>



| <span data-ttu-id="0687e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0687e-132">Requirement</span></span> | <span data-ttu-id="0687e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0687e-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0687e-134">Versione</span><span class="sxs-lookup"><span data-stu-id="0687e-134">Version</span></span><br/> | <span data-ttu-id="0687e-135">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0687e-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0687e-136">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0687e-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0687e-137">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0687e-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0687e-138">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0687e-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0687e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0687e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0687e-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0687e-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




