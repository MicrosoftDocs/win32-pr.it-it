---
description: La proprietà manifest viene utilizzata per impostare o ottenere il contesto di attivazione attiva.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: Proprietà ActCtx. manifest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966601"
---
# <a name="actctxmanifest-property"></a><span data-ttu-id="e0b5f-103">Proprietà ActCtx. manifest</span><span class="sxs-lookup"><span data-stu-id="e0b5f-103">ActCtx.Manifest property</span></span>

<span data-ttu-id="e0b5f-104">La proprietà **manifest** viene utilizzata per impostare o ottenere il contesto di attivazione attiva.</span><span class="sxs-lookup"><span data-stu-id="e0b5f-104">The **Manifest** property is used to set or get the active activation context.</span></span>

<span data-ttu-id="e0b5f-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e0b5f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b5f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0b5f-106">Syntax</span></span>


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a><span data-ttu-id="e0b5f-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e0b5f-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e0b5f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0b5f-108">Remarks</span></span>

<span data-ttu-id="e0b5f-109">Se è possibile creare un contesto di attivazione con il file manifesto specificato, lo script seguente imposta la proprietà del manifesto e attiva la costante di attivazione specificata dal manifesto.</span><span class="sxs-lookup"><span data-stu-id="e0b5f-109">If an activation context can be created with the manifest file provided, the following script sets the Manifest property and activates the activation constant specified by the manifest.</span></span> <span data-ttu-id="e0b5f-110">Se non è possibile creare un contesto di attivazione dal manifesto, il contesto di attivazione rimane impostato sul contesto di attivazione attualmente attivo.</span><span class="sxs-lookup"><span data-stu-id="e0b5f-110">If an activation context cannot be created from the manifest, the activation context remains set to the currently active activation context.</span></span>

<span data-ttu-id="e0b5f-111">ActCtxObj. manifest = "<*nome file manifesto*>";</span><span class="sxs-lookup"><span data-stu-id="e0b5f-111">ActCtxObj.Manifest = "<*manifest file name*>";</span></span>

<span data-ttu-id="e0b5f-112">Se un contesto di attivazione è stato creato o attivato in precedenza, lo script seguente imposta la proprietà **manifest** sul contesto di attivazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e0b5f-112">If an activation context has previously been created or activated, the following script sets the **Manifest** property to the current activation context.</span></span> <span data-ttu-id="e0b5f-113">Se un contesto di attivazione non è stato creato o attivato in precedenza, imposta la proprietà del **manifesto** su una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="e0b5f-113">If an activation context has not previously been created or activated, this sets the **Manifest** property to an empty string.</span></span>

<span data-ttu-id="e0b5f-114">"BSTR bstrManifest = ActCtxObj. manifest"</span><span class="sxs-lookup"><span data-stu-id="e0b5f-114">"BSTR bstrManifest = ActCtxObj.Manifest"</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b5f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0b5f-115">Requirements</span></span>



| <span data-ttu-id="e0b5f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b5f-116">Requirement</span></span> | <span data-ttu-id="e0b5f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e0b5f-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b5f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0b5f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b5f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0b5f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e0b5f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0b5f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b5f-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0b5f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e0b5f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b5f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b5f-123"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b5f-123"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0b5f-124">IID</span><span class="sxs-lookup"><span data-stu-id="e0b5f-124">IID</span></span><br/>                      | <span data-ttu-id="e0b5f-125">IID \_ IActCtx è definito come 8FA7728F-B69B-4ee5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="e0b5f-125">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



 

 




