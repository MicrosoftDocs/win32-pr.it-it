---
description: Rappresenta una raccolta di finestre aperte che appartengono alla Shell. I metodi associati a questi oggetti possono controllare ed eseguire comandi all'interno della shell e ottenere altri oggetti correlati alla Shell.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Oggetto ShellWindows (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979810"
---
# <a name="shellwindows-object"></a><span data-ttu-id="64f01-104">Oggetto ShellWindows</span><span class="sxs-lookup"><span data-stu-id="64f01-104">ShellWindows object</span></span>

<span data-ttu-id="64f01-105">Rappresenta una raccolta di finestre aperte che appartengono alla Shell.</span><span class="sxs-lookup"><span data-stu-id="64f01-105">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="64f01-106">I metodi associati a questi oggetti possono controllare ed eseguire comandi all'interno della shell e ottenere altri oggetti correlati alla Shell.</span><span class="sxs-lookup"><span data-stu-id="64f01-106">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="64f01-107">Membri</span><span class="sxs-lookup"><span data-stu-id="64f01-107">Members</span></span>

<span data-ttu-id="64f01-108">L'oggetto **ShellWindows** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="64f01-108">The **ShellWindows** object has these types of members:</span></span>

-   [<span data-ttu-id="64f01-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="64f01-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="64f01-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64f01-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="64f01-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="64f01-111">Methods</span></span>

<span data-ttu-id="64f01-112">L'oggetto **ShellWindows** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="64f01-112">The **ShellWindows** object has these methods.</span></span>



| <span data-ttu-id="64f01-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="64f01-113">Method</span></span>                                                 | <span data-ttu-id="64f01-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64f01-114">Description</span></span>                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64f01-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="64f01-115">**\_NewEnum**</span></span>](shellwindows--newenum-method-7ral.md) | <span data-ttu-id="64f01-116">Crea e restituisce un nuovo oggetto **ShellWindows** che è una copia di questo oggetto **ShellWindows** .</span><span class="sxs-lookup"><span data-stu-id="64f01-116">Creates and returns a new **ShellWindows** object that is a copy of this **ShellWindows** object.</span></span><br/>        |
| [<span data-ttu-id="64f01-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64f01-117">**Item**</span></span>](shellwindows-item.md)                      | <span data-ttu-id="64f01-118">Recupera un oggetto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) che rappresenta la finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="64f01-118">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="64f01-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64f01-119">Properties</span></span>

<span data-ttu-id="64f01-120">L'oggetto **ShellWindows** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="64f01-120">The **ShellWindows** object has these properties.</span></span>



| <span data-ttu-id="64f01-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64f01-121">Property</span></span>                                       | <span data-ttu-id="64f01-122">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="64f01-122">Access type</span></span>          | <span data-ttu-id="64f01-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64f01-123">Description</span></span>                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="64f01-124">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="64f01-124">**Count**</span></span>](shellwindows-count.md)<br/> | <span data-ttu-id="64f01-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="64f01-125">Read-only</span></span><br/> | <span data-ttu-id="64f01-126">Contiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="64f01-126">Contains the number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="64f01-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64f01-127">Requirements</span></span>



| <span data-ttu-id="64f01-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="64f01-128">Requirement</span></span> | <span data-ttu-id="64f01-129">Valore</span><span class="sxs-lookup"><span data-stu-id="64f01-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f01-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64f01-130">Minimum supported client</span></span><br/> | <span data-ttu-id="64f01-131">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="64f01-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="64f01-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64f01-132">Minimum supported server</span></span><br/> | <span data-ttu-id="64f01-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="64f01-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64f01-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64f01-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="64f01-135"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="64f01-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="64f01-136">DLL</span><span class="sxs-lookup"><span data-stu-id="64f01-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64f01-137"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="64f01-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
