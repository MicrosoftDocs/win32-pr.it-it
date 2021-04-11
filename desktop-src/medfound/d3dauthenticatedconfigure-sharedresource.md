---
description: Consente a un processo di aprire una risorsa condivisa o di disabilitare l'apertura di risorse condivise da un processo.
ms.assetid: 5fa2b88f-e946-436c-953e-04e0e338146c
title: D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7404a4bed3ac3b1d4002bb03c45d7732500b77e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225816"
---
# <a name="d3dauthenticatedconfigure_sharedresource"></a><span data-ttu-id="e06dc-103">\_SHAREDRESOURCE D3DAUTHENTICATEDCONFIGURE</span><span class="sxs-lookup"><span data-stu-id="e06dc-103">D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE</span></span>

<span data-ttu-id="e06dc-104">Consente a un processo di aprire una risorsa condivisa o di disabilitare l'apertura di risorse condivise da un processo.</span><span class="sxs-lookup"><span data-stu-id="e06dc-104">Enables a process to open a shared resource, or disables a process from opening shared resources.</span></span>



| <span data-ttu-id="e06dc-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="e06dc-105">Requirement</span></span> | <span data-ttu-id="e06dc-106">Valore</span><span class="sxs-lookup"><span data-stu-id="e06dc-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e06dc-107">GUID comando</span><span class="sxs-lookup"><span data-stu-id="e06dc-107">Command GUID</span></span> | <span data-ttu-id="e06dc-108">**\_SHAREDRESOURCE D3DAUTHENTICATEDCONFIGURE**</span><span class="sxs-lookup"><span data-stu-id="e06dc-108">**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**</span></span>                                                               |
| <span data-ttu-id="e06dc-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="e06dc-109">Input data</span></span>   | [<span data-ttu-id="e06dc-110">**\_CONFIGURESHAREDRESOURCE D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="e06dc-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE**</span></span>](d3dauthenticatedchannel-configuresharedresource.md) |



 

## <a name="remarks"></a><span data-ttu-id="e06dc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e06dc-111">Remarks</span></span>

<span data-ttu-id="e06dc-112">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="e06dc-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="e06dc-113">**\_D3d9 driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="e06dc-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_D3D9**</span></span>
-   <span data-ttu-id="e06dc-114">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="e06dc-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="e06dc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e06dc-115">Requirements</span></span>



| <span data-ttu-id="e06dc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e06dc-116">Requirement</span></span> | <span data-ttu-id="e06dc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e06dc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e06dc-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e06dc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e06dc-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e06dc-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e06dc-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e06dc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e06dc-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e06dc-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e06dc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e06dc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e06dc-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e06dc-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e06dc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e06dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e06dc-125">Comandi protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="e06dc-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="e06dc-126">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="e06dc-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="e06dc-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="e06dc-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




