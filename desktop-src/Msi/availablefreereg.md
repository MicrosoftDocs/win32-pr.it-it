---
description: La proprietà AVAILABLEFREEREG specifica in kilobyte lo spazio libero totale disponibile nel registro di sistema dopo la chiamata dell'azione AllocateRegistrySpace. Il valore massimo della proprietà AVAILABLEFREEREG è 2 milioni kilobyte. Questa proprietà è impostata solo in Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Proprietà AVAILABLEFREEREG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330635"
---
# <a name="availablefreereg-property"></a><span data-ttu-id="2619d-103">Proprietà AVAILABLEFREEREG</span><span class="sxs-lookup"><span data-stu-id="2619d-103">AVAILABLEFREEREG property</span></span>

<span data-ttu-id="2619d-104">La proprietà **AVAILABLEFREEREG** specifica in kilobyte lo spazio libero totale disponibile nel registro di sistema dopo la chiamata dell' [azione AllocateRegistrySpace](allocateregistryspace-action.md).</span><span class="sxs-lookup"><span data-stu-id="2619d-104">The **AVAILABLEFREEREG** property specifies in kilobytes the total free space available in the registry after calling the [AllocateRegistrySpace action](allocateregistryspace-action.md).</span></span>

<span data-ttu-id="2619d-105">Il valore massimo della proprietà **AVAILABLEFREEREG** è 2 milioni kilobyte.</span><span class="sxs-lookup"><span data-stu-id="2619d-105">The maximum value of the **AVAILABLEFREEREG** property is 2000000 kilobytes.</span></span>

<span data-ttu-id="2619d-106">Questa proprietà è impostata solo in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2619d-106">This property is set only on Windows 2000.</span></span>

## <a name="remarks"></a><span data-ttu-id="2619d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2619d-107">Remarks</span></span>

<span data-ttu-id="2619d-108">La proprietà **AVAILABLEFREEREG** deve essere impostata su un valore sufficientemente grande da garantire spazio sufficiente nel registro di sistema per tutte le informazioni di registrazione aggiunte dall'installazione.</span><span class="sxs-lookup"><span data-stu-id="2619d-108">The **AVAILABLEFREEREG** property must be set to a value large enough to ensure sufficient space in the registry for all registration information added by the installation.</span></span> <span data-ttu-id="2619d-109">Il valore minimo necessario per garantire uno spazio sufficiente dipende dalla posizione in cui si trova l' [azione AllocateRegistrySpace](allocateregistryspace-action.md) nella sequenza di azione perché il programma di installazione aumenta automaticamente lo spazio necessario per la registrazione delle informazioni nelle tabelle [del registro di sistema](registry-table.md), della [classe](class-table.md), di [selfreg](selfreg-table.md), dell' [estensione](extension-table.md), [MIME](mime-table.md)e dei [verbi](verb-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2619d-109">The minimum value required to ensure sufficient space depends on where the [AllocateRegistrySpace action](allocateregistryspace-action.md) is located in the action sequence because the installer automatically increases the space as needed when registering information in the [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md), and [Verb](verb-table.md) tables.</span></span> <span data-ttu-id="2619d-110">Il programma di installazione non aumenta lo spazio totale del registro di sistema per la quantità specificata da **AVAILABLEFREEREG** fino a raggiungere AllocateRegistrySpace nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="2619d-110">The installer does not increase the total registry space to the amount specified by **AVAILABLEFREEREG** until reaching AllocateRegistrySpace in the action sequence.</span></span>

<span data-ttu-id="2619d-111">Se AllocateRegistrySpace è una delle prime azioni nella sequenza di azione, **AVAILABLEFREEREG** deve essere impostato sullo spazio totale richiesto dalle informazioni di registrazione nella tabella del registro di sistema, nella tabella delle classi, nella tabella TypeLib, nella tabella SelfReg, nella tabella di estensione, nella tabella MIME, nella tabella dei verbi, nella registrazione delle [azioni personalizzate](custom-actions.md) , nella registrazione automatica e in qualsiasi altra informazione del registro di sistema scritta durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="2619d-111">If AllocateRegistrySpace is one of the first actions in the action sequence, **AVAILABLEFREEREG** should be set to the total space required by the registration information in the Registry table, Class table, TypeLib table, SelfReg table, Extension table, MIME table, Verb table, [custom actions](custom-actions.md) registration, self registration, and any other registry information written during the installation.</span></span> <span data-ttu-id="2619d-112">Il valore di **AVAILABLEFREEREG** è la quantità totale di informazioni aggiunte dall'installazione e garantisce spazio sufficiente in tutti i casi.</span><span class="sxs-lookup"><span data-stu-id="2619d-112">The value of **AVAILABLEFREEREG** is the total amount of information added by the installation and ensures sufficient space in all cases.</span></span> <span data-ttu-id="2619d-113">Questo è anche il caso più comune.</span><span class="sxs-lookup"><span data-stu-id="2619d-113">This is also the most common case.</span></span>

<span data-ttu-id="2619d-114">Se l'azione AllocateRegistrySpace può essere creata nella sequenza di azione dopo tutte le [azioni standard](standard-actions.md) che scrivono i dati di registrazione, ad esempio [WriteRegistryValori consente](writeregistryvalues-action.md) e [registerClassInfo](registerclassinfo-action.md), il valore di **AVAILABLEFREEREG** deve essere impostato solo sullo spazio necessario per registrare azioni personalizzate, registrare le librerie dei tipi e qualsiasi altra informazione non ancora registrata tramite le tabelle.</span><span class="sxs-lookup"><span data-stu-id="2619d-114">If the AllocateRegistrySpace action can be authored into the action sequence after all [standard actions](standard-actions.md) that write registration data, such as [WriteRegistryValues](writeregistryvalues-action.md) and [RegisterClassInfo](registerclassinfo-action.md), the value of **AVAILABLEFREEREG** needs only be set to the space needed to register custom actions, register type libraries, and any other information not yet registered through the tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="2619d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2619d-115">Requirements</span></span>



| <span data-ttu-id="2619d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2619d-116">Requirement</span></span> | <span data-ttu-id="2619d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2619d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2619d-118">Versione</span><span class="sxs-lookup"><span data-stu-id="2619d-118">Version</span></span><br/> | <span data-ttu-id="2619d-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2619d-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2619d-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2619d-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2619d-121">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2619d-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2619d-122">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2619d-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2619d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2619d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2619d-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2619d-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




