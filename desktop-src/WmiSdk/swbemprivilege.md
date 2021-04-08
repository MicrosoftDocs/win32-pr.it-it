---
description: L'oggetto SWbemPrivilege rappresenta un singolo privilegio. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Oggetto SWbemPrivilege (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c3be448b4088011cd4d628a7d98b448af550b010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058264"
---
# <a name="swbemprivilege-object"></a><span data-ttu-id="86095-104">Oggetto SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="86095-104">SWbemPrivilege object</span></span>

<span data-ttu-id="86095-105">L'oggetto **SWbemPrivilege** rappresenta un singolo privilegio.</span><span class="sxs-lookup"><span data-stu-id="86095-105">The **SWbemPrivilege** object represents a single privilege.</span></span> <span data-ttu-id="86095-106">Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.</span><span class="sxs-lookup"><span data-stu-id="86095-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="86095-107">Membri</span><span class="sxs-lookup"><span data-stu-id="86095-107">Members</span></span>

<span data-ttu-id="86095-108">L'oggetto **SWbemPrivilege** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="86095-108">The **SWbemPrivilege** object has these types of members:</span></span>

-   [<span data-ttu-id="86095-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86095-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86095-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86095-110">Properties</span></span>

<span data-ttu-id="86095-111">L'oggetto **SWbemPrivilege** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="86095-111">The **SWbemPrivilege** object has these properties.</span></span>



| <span data-ttu-id="86095-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86095-112">Property</span></span>                                                     | <span data-ttu-id="86095-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="86095-113">Access type</span></span>           | <span data-ttu-id="86095-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86095-114">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="86095-115">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="86095-115">**Displayname**</span></span>](swbemprivilege-displayname.md)<br/> | <span data-ttu-id="86095-116">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="86095-116">Read-only</span></span><br/>  | <span data-ttu-id="86095-117">Nome visualizzato del privilegio.</span><span class="sxs-lookup"><span data-stu-id="86095-117">Display name of this privilege.</span></span><br/>                                       |
| [<span data-ttu-id="86095-118">**Identificatore**</span><span class="sxs-lookup"><span data-stu-id="86095-118">**Identifier**</span></span>](swbemprivilege-identifier.md)<br/>   | <span data-ttu-id="86095-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="86095-119">Read/write</span></span><br/> | <span data-ttu-id="86095-120">Integer che rappresenta il privilegio da impostare o recuperare.</span><span class="sxs-lookup"><span data-stu-id="86095-120">Integer that represents the privilege that is being set or retrieved.</span></span><br/> |
| [<span data-ttu-id="86095-121">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="86095-121">**IsEnabled**</span></span>](swbemprivilege-isenabled.md)<br/>     | <span data-ttu-id="86095-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="86095-122">Read/write</span></span><br/> | <span data-ttu-id="86095-123">Valore booleano che indica se questo privilegio è abilitato.</span><span class="sxs-lookup"><span data-stu-id="86095-123">Boolean value that indicates if this privilege is enabled.</span></span><br/>            |
| [<span data-ttu-id="86095-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="86095-124">**Name**</span></span>](swbemprivilege-name.md)<br/>               | <span data-ttu-id="86095-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="86095-125">Read-only</span></span><br/>  | <span data-ttu-id="86095-126">Nome del privilegio.</span><span class="sxs-lookup"><span data-stu-id="86095-126">Name of this privilege.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="86095-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86095-127">Requirements</span></span>



| <span data-ttu-id="86095-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="86095-128">Requirement</span></span> | <span data-ttu-id="86095-129">Valore</span><span class="sxs-lookup"><span data-stu-id="86095-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86095-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86095-130">Minimum supported client</span></span><br/> | <span data-ttu-id="86095-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86095-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86095-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86095-132">Minimum supported server</span></span><br/> | <span data-ttu-id="86095-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86095-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86095-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86095-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="86095-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="86095-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="86095-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="86095-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="86095-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86095-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86095-138">DLL</span><span class="sxs-lookup"><span data-stu-id="86095-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86095-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86095-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="86095-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="86095-140">CLSID</span></span><br/>                    | <span data-ttu-id="86095-141">\_SWBEMPRIVILEGE CLSID</span><span class="sxs-lookup"><span data-stu-id="86095-141">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="86095-142">IID</span><span class="sxs-lookup"><span data-stu-id="86095-142">IID</span></span><br/>                      | <span data-ttu-id="86095-143">\_ISWBEMPRIVILEGE IID</span><span class="sxs-lookup"><span data-stu-id="86095-143">IID\_ISWbemPrivilege</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="86095-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86095-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86095-145">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="86095-145">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="86095-146">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="86095-146">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




