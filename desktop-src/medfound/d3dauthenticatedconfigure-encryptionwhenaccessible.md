---
description: Imposta il livello di crittografia che viene eseguito prima che il contenuto protetto diventi accessibile alla CPU o al bus.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8b624c26c81549372e0e09b4a08ce73f6cd3dd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524593"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a><span data-ttu-id="8e84e-103">\_ENCRYPTIONWHENACCESSIBLE D3DAUTHENTICATEDCONFIGURE</span><span class="sxs-lookup"><span data-stu-id="8e84e-103">D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="8e84e-104">Imposta il livello di crittografia che viene eseguito prima che il contenuto protetto diventi accessibile alla CPU o al bus.</span><span class="sxs-lookup"><span data-stu-id="8e84e-104">Sets the level of encryption that is performed before protected content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="8e84e-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e84e-105">Requirement</span></span> | <span data-ttu-id="8e84e-106">Valore</span><span class="sxs-lookup"><span data-stu-id="8e84e-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e84e-107">GUID comando</span><span class="sxs-lookup"><span data-stu-id="8e84e-107">Command GUID</span></span> | <span data-ttu-id="8e84e-108">**\_ENCRYPTIONWHENACCESSIBLE D3DAUTHENTICATEDCONFIGURE**</span><span class="sxs-lookup"><span data-stu-id="8e84e-108">**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**</span></span>                                                                     |
| <span data-ttu-id="8e84e-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="8e84e-109">Input data</span></span>   | [<span data-ttu-id="8e84e-110">**\_CONFIGUREUNCOMPRESSEDENCRYPTION D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="8e84e-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION**</span></span>](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a><span data-ttu-id="8e84e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e84e-111">Remarks</span></span>

<span data-ttu-id="8e84e-112">I tipi di canale seguenti supportano questa query:</span><span class="sxs-lookup"><span data-stu-id="8e84e-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="8e84e-113">**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="8e84e-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="8e84e-114">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="8e84e-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="8e84e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e84e-115">Requirements</span></span>



| <span data-ttu-id="8e84e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e84e-116">Requirement</span></span> | <span data-ttu-id="8e84e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8e84e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e84e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e84e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8e84e-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e84e-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8e84e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e84e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8e84e-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e84e-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8e84e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e84e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e84e-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e84e-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e84e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e84e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e84e-125">Comandi protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="8e84e-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="8e84e-126">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="8e84e-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="8e84e-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="8e84e-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




