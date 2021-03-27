---
description: Estende l'oggetto FolderItem. Oltre alle proprietà e ai metodi supportati da FolderItem, ShellFolderItem dispone di due metodi aggiuntivi.
title: Oggetto ShellFolderItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: 84e230e295a956f3f83833a577b47be1e46873a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980434"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="8018e-104">Oggetto ShellFolderItem</span><span class="sxs-lookup"><span data-stu-id="8018e-104">ShellFolderItem object</span></span>

<span data-ttu-id="8018e-105">Estende l'oggetto [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="8018e-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="8018e-106">Oltre alle proprietà e ai metodi supportati da **FolderItem**, **ShellFolderItem** dispone di due metodi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="8018e-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="8018e-107">Membri</span><span class="sxs-lookup"><span data-stu-id="8018e-107">Members</span></span>

<span data-ttu-id="8018e-108">L'oggetto **ShellFolderItem** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8018e-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="8018e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="8018e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8018e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="8018e-110">Methods</span></span>

<span data-ttu-id="8018e-111">L'oggetto **ShellFolderItem** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8018e-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="8018e-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="8018e-112">Method</span></span>                                                       | <span data-ttu-id="8018e-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8018e-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8018e-114">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="8018e-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="8018e-115">Ottiene il valore di una proprietà dal set di proprietà di un elemento.</span><span class="sxs-lookup"><span data-stu-id="8018e-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="8018e-116">La proprietà può essere specificata in base al nome o in base all'identificatore di formato (FMTID) e all'identificatore di proprietà (PID) del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8018e-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="8018e-117">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="8018e-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="8018e-118">Esegue un verbo su un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="8018e-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="8018e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8018e-119">Requirements</span></span>



| <span data-ttu-id="8018e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8018e-120">Requirement</span></span> | <span data-ttu-id="8018e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8018e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8018e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8018e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8018e-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8018e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8018e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8018e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8018e-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8018e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8018e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8018e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8018e-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8018e-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8018e-128">IDL</span><span class="sxs-lookup"><span data-stu-id="8018e-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8018e-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8018e-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8018e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8018e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8018e-131"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="8018e-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




