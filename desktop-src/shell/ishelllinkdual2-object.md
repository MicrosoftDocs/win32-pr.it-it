---
description: Estende l'oggetto ShellLinkObject e supporta una proprietà aggiuntiva.
title: Oggetto IShellLinkDual2 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 8a63552c-6bce-4583-8df8-a7f7731b35eb
ms.openlocfilehash: 47dc46d20fc6cf5096a38ccfd1790957f1fdd318
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842642"
---
# <a name="ishelllinkdual2-object"></a><span data-ttu-id="7ddc7-103">Oggetto IShellLinkDual2</span><span class="sxs-lookup"><span data-stu-id="7ddc7-103">IShellLinkDual2 object</span></span>

<span data-ttu-id="7ddc7-104">Estende [**l'oggetto ShellLinkObject**](shelllinkobject-object.md) e supporta una proprietà aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="7ddc7-104">Extends the [**ShellLinkObject**](shelllinkobject-object.md) object and supports one additional property.</span></span>

## <a name="members"></a><span data-ttu-id="7ddc7-105">Membri</span><span class="sxs-lookup"><span data-stu-id="7ddc7-105">Members</span></span>

<span data-ttu-id="7ddc7-106">**L'oggetto IShellLinkDual2** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7ddc7-106">The **IShellLinkDual2** object has these types of members:</span></span>

-   [<span data-ttu-id="7ddc7-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ddc7-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ddc7-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ddc7-108">Properties</span></span>

<span data-ttu-id="7ddc7-109">**L'oggetto IShellLinkDual2** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7ddc7-109">The **IShellLinkDual2** object has these properties.</span></span>



| <span data-ttu-id="7ddc7-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ddc7-110">Property</span></span>                                            | <span data-ttu-id="7ddc7-111">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="7ddc7-111">Access type</span></span>          | <span data-ttu-id="7ddc7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ddc7-112">Description</span></span>                                   |
|:----------------------------------------------------|:---------------------|:----------------------------------------------|
| [<span data-ttu-id="7ddc7-113">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="7ddc7-113">**Target**</span></span>](ishelllinkdual2-target.md)<br/> | <span data-ttu-id="7ddc7-114">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ddc7-114">Read-only</span></span><br/> | <span data-ttu-id="7ddc7-115">Contiene la destinazione dell'oggetto collegamento.</span><span class="sxs-lookup"><span data-stu-id="7ddc7-115">Contains the link object's target.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7ddc7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ddc7-116">Requirements</span></span>



| <span data-ttu-id="7ddc7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ddc7-117">Requirement</span></span> | <span data-ttu-id="7ddc7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7ddc7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ddc7-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ddc7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7ddc7-120">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7ddc7-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ddc7-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ddc7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7ddc7-122">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ddc7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7ddc7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ddc7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ddc7-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7ddc7-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7ddc7-125">Idl</span><span class="sxs-lookup"><span data-stu-id="7ddc7-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ddc7-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ddc7-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7ddc7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7ddc7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ddc7-128"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7ddc7-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




