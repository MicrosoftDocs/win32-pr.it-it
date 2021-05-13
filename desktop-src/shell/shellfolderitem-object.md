---
description: Estende l'oggetto FolderItem. Oltre alle proprietà e ai metodi supportati da FolderItem, ShellFolderItem dispone di due metodi aggiuntivi.
title: Oggetto ShellFolderItem (Shldisp.h)
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
ms.openlocfilehash: a9e6d6b3f954f0c8ee4b13fb651a9ea04274deb6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840772"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="1f41a-104">Oggetto ShellFolderItem</span><span class="sxs-lookup"><span data-stu-id="1f41a-104">ShellFolderItem object</span></span>

<span data-ttu-id="1f41a-105">Estende [**l'oggetto FolderItem.**](folderitem.md)</span><span class="sxs-lookup"><span data-stu-id="1f41a-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="1f41a-106">Oltre alle proprietà e ai metodi supportati da **FolderItem,** **ShellFolderItem** dispone di due metodi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="1f41a-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="1f41a-107">Membri</span><span class="sxs-lookup"><span data-stu-id="1f41a-107">Members</span></span>

<span data-ttu-id="1f41a-108">**L'oggetto ShellFolderItem** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1f41a-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="1f41a-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="1f41a-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1f41a-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="1f41a-110">Methods</span></span>

<span data-ttu-id="1f41a-111">**L'oggetto ShellFolderItem** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1f41a-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="1f41a-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="1f41a-112">Method</span></span>                                                       | <span data-ttu-id="1f41a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f41a-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f41a-114">**Extendedproperty**</span><span class="sxs-lookup"><span data-stu-id="1f41a-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="1f41a-115">Ottiene il valore di una proprietà dal set di proprietà di un elemento.</span><span class="sxs-lookup"><span data-stu-id="1f41a-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="1f41a-116">La proprietà può essere specificata in base al nome o all'identificatore di formato (FMTID) e all'identificatore di proprietà (PID) del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="1f41a-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="1f41a-117">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="1f41a-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="1f41a-118">Esegue un verbo su un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="1f41a-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="1f41a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f41a-119">Requirements</span></span>



| <span data-ttu-id="1f41a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f41a-120">Requirement</span></span> | <span data-ttu-id="1f41a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1f41a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f41a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f41a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1f41a-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1f41a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f41a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f41a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1f41a-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1f41a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1f41a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f41a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f41a-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1f41a-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1f41a-128">Idl</span><span class="sxs-lookup"><span data-stu-id="1f41a-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f41a-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f41a-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1f41a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1f41a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f41a-131"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="1f41a-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




