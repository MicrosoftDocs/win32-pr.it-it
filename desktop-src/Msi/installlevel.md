---
description: La proprietà INSTALLLEVEL è il livello iniziale a cui vengono selezionate le funzionalità &\# 0034;&\# 0034; per l'installazione per impostazione predefinita.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: Proprietà INSTALLLEVEL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328432"
---
# <a name="installlevel-property"></a><span data-ttu-id="3b169-103">Proprietà INSTALLLEVEL</span><span class="sxs-lookup"><span data-stu-id="3b169-103">INSTALLLEVEL property</span></span>

<span data-ttu-id="3b169-104">La proprietà **INSTALLLEVEL** è il livello iniziale a cui vengono selezionate le funzionalità "on" per l'installazione per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3b169-104">The **INSTALLLEVEL** property is the initial level at which features are selected "ON" for installation by default.</span></span> <span data-ttu-id="3b169-105">Una funzionalità viene installata solo se il valore nel campo livello della tabella delle [funzionalità](feature-table.md) è minore o uguale al valore INSTALLLEVEL corrente.</span><span class="sxs-lookup"><span data-stu-id="3b169-105">A feature is installed only if the value in the Level field of the [Feature table](feature-table.md) is less than or equal to the current INSTALLLEVEL value.</span></span> <span data-ttu-id="3b169-106">Il livello di installazione per qualsiasi installazione viene specificato dalla proprietà **INSTALLLEVEL** e può essere un integrale compreso tra 1 e 32.767.</span><span class="sxs-lookup"><span data-stu-id="3b169-106">The installation level for any installation is specified by the **INSTALLLEVEL** property, and can be an integral from 1 to 32,767.</span></span> <span data-ttu-id="3b169-107">Per ulteriori informazioni sui livelli di installazione, vedere [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="3b169-107">For further discussion of installation levels, see [Feature Table](feature-table.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="3b169-108">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="3b169-108">Default Value</span></span>

<span data-ttu-id="3b169-109">Se non viene specificato alcun valore, il livello di installazione viene impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="3b169-109">If no value is specified, the install level defaults to 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b169-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b169-110">Remarks</span></span>

<span data-ttu-id="3b169-111">È possibile eseguire l'override del livello di installazione specificato dalla proprietà **INSTALLLEVEL** con le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b169-111">The installation level specified by the **INSTALLLEVEL** property can be overridden by the following properties:</span></span>

-   [<span data-ttu-id="3b169-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="3b169-112">**ADDLOCAL**</span></span>](addlocal.md)
-   [<span data-ttu-id="3b169-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3b169-113">**ADDSOURCE**</span></span>](addsource.md)
-   [<span data-ttu-id="3b169-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3b169-114">**ADDDEFAULT**</span></span>](adddefault.md)
-   [<span data-ttu-id="3b169-115">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="3b169-115">**COMPADDLOCAL**</span></span>](compaddlocal.md)
-   [<span data-ttu-id="3b169-116">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3b169-116">**COMPADDSOURCE**</span></span>](compaddsource.md)
-   [<span data-ttu-id="3b169-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="3b169-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="3b169-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3b169-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="3b169-119">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="3b169-119">**REMOVE**</span></span>](remove.md)
-   [<span data-ttu-id="3b169-120">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="3b169-120">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="3b169-121">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="3b169-121">**ADVERTISE**</span></span>](advertise.md)

<span data-ttu-id="3b169-122">Ad esempio, l'impostazione di ADDLOCAL = ALL Installa tutte le funzionalità localmente indipendentemente dal valore della proprietà **INSTALLLEVEL** .</span><span class="sxs-lookup"><span data-stu-id="3b169-122">For example, setting ADDLOCAL=ALL installs all features locally regardless of the value of the **INSTALLLEVEL** property.</span></span> <span data-ttu-id="3b169-123">Se il valore della colonna Level nella [tabella Feature](feature-table.md) è 0, tale funzionalità non viene installata e non viene visualizzata nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3b169-123">If the value of the Level column in the [Feature table](feature-table.md) is 0, that feature is not installed and not displayed in the UI.</span></span>

<span data-ttu-id="3b169-124">Un amministratore può disabilitare definitivamente una funzionalità applicando una trasformazione di personalizzazione che imposta un valore 0 nella colonna livello per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3b169-124">An administrator can permanently disable a feature by applying a customization transform that sets a 0 in the Level column for that feature.</span></span> <span data-ttu-id="3b169-125">L'applicazione della trasformazione personalizzazione impedisce l'installazione e la visualizzazione della funzionalità anche se l'utente seleziona un'installazione completa usando l'interfaccia utente o impostando ADDLOCAL su ALL nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3b169-125">The application of the customization transform prevents the installation and display of the feature even if the user selects a complete installation using the UI or by setting ADDLOCAL to ALL on the command line.</span></span> <span data-ttu-id="3b169-126">Vedere [un esempio di trasformazione della personalizzazione](a-customization-transform-example.md).</span><span class="sxs-lookup"><span data-stu-id="3b169-126">See [A Customization Transform Example](a-customization-transform-example.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b169-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b169-127">Requirements</span></span>



| <span data-ttu-id="3b169-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b169-128">Requirement</span></span> | <span data-ttu-id="3b169-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3b169-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b169-130">Versione</span><span class="sxs-lookup"><span data-stu-id="3b169-130">Version</span></span><br/> | <span data-ttu-id="3b169-131">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3b169-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3b169-132">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3b169-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3b169-133">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b169-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3b169-134">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3b169-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b169-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b169-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b169-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b169-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




