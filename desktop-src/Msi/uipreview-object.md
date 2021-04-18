---
description: L'oggetto UIPreview viene utilizzato per visualizzare le finestre di dialogo e i manifesti dell'interfaccia utente durante la creazione. Questo oggetto viene creato dal metodo EnableUIPreview dell'oggetto di database.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Oggetto UIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327917"
---
# <a name="uipreview-object"></a><span data-ttu-id="51c63-104">Oggetto UIPreview</span><span class="sxs-lookup"><span data-stu-id="51c63-104">UIPreview object</span></span>

<span data-ttu-id="51c63-105">L'oggetto **UIPreview** viene utilizzato per visualizzare le finestre di dialogo e i manifesti dell'interfaccia utente durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="51c63-105">The **UIPreview** object is used to view user interface dialog boxes and billboards during authoring.</span></span> <span data-ttu-id="51c63-106">Questo oggetto viene creato dal metodo [**EnableUIPreview**](database-enableuipreview.md) dell'oggetto di [**database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="51c63-106">This object is created by the [**EnableUIPreview**](database-enableuipreview.md) method of the [**Database**](database-object.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="51c63-107">Membri</span><span class="sxs-lookup"><span data-stu-id="51c63-107">Members</span></span>

<span data-ttu-id="51c63-108">L'oggetto **UIPreview** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="51c63-108">The **UIPreview** object has these types of members:</span></span>

-   [<span data-ttu-id="51c63-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="51c63-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="51c63-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51c63-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="51c63-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="51c63-111">Methods</span></span>

<span data-ttu-id="51c63-112">L'oggetto **UIPreview** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="51c63-112">The **UIPreview** object has these methods.</span></span>



| <span data-ttu-id="51c63-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="51c63-113">Method</span></span>                                           | <span data-ttu-id="51c63-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51c63-114">Description</span></span>                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51c63-115">**ViewBillboard**</span><span class="sxs-lookup"><span data-stu-id="51c63-115">**ViewBillboard**</span></span>](uipreview-viewbillboard.md) | <span data-ttu-id="51c63-116">Consente di visualizzare un Billboard creato utilizzando il controllo host nella finestra di dialogo attualmente visualizzata.</span><span class="sxs-lookup"><span data-stu-id="51c63-116">Displays an authored billboard using the host control in the currently displayed dialog box.</span></span><br/> |
| [<span data-ttu-id="51c63-117">**ViewDialog**</span><span class="sxs-lookup"><span data-stu-id="51c63-117">**ViewDialog**</span></span>](uipreview-viewdialog.md)       | <span data-ttu-id="51c63-118">Consente di visualizzare una finestra di dialogo dell'interfaccia utente creata archiviata nel database corrente.</span><span class="sxs-lookup"><span data-stu-id="51c63-118">Displays an authored UI dialog box stored in the current database.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="51c63-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51c63-119">Properties</span></span>

<span data-ttu-id="51c63-120">L'oggetto **UIPreview** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="51c63-120">The **UIPreview** object has these properties.</span></span>



| <span data-ttu-id="51c63-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51c63-121">Property</span></span>                                          | <span data-ttu-id="51c63-122">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="51c63-122">Access type</span></span>           | <span data-ttu-id="51c63-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51c63-123">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51c63-124">**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="51c63-124">**Property**</span></span>](uipreview-property.md)<br/> | <span data-ttu-id="51c63-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="51c63-125">Read/write</span></span><br/> | <span data-ttu-id="51c63-126">Rappresenta il valore stringa di una proprietà del programma di installazione denominata o, se preceduto da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="51c63-126">Represents the string value of a named installer property or, if prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="51c63-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51c63-127">Requirements</span></span>



| <span data-ttu-id="51c63-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="51c63-128">Requirement</span></span> | <span data-ttu-id="51c63-129">Valore</span><span class="sxs-lookup"><span data-stu-id="51c63-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51c63-130">Versione</span><span class="sxs-lookup"><span data-stu-id="51c63-130">Version</span></span><br/> | <span data-ttu-id="51c63-131">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="51c63-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="51c63-132">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="51c63-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="51c63-133">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="51c63-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="51c63-134">DLL</span><span class="sxs-lookup"><span data-stu-id="51c63-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="51c63-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51c63-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="51c63-136">IID</span><span class="sxs-lookup"><span data-stu-id="51c63-136">IID</span></span><br/>     | <span data-ttu-id="51c63-137">IID \_ IUIPreview è definito come 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="51c63-137">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="51c63-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51c63-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c63-139">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="51c63-139">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




