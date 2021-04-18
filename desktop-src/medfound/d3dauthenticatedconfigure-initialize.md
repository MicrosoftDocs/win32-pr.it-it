---
description: Inizializza il canale autenticato.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305428"
---
# <a name="d3dauthenticatedconfigure_initialize"></a><span data-ttu-id="8cf48-103">\_Inizializzazione D3DAUTHENTICATEDCONFIGURE</span><span class="sxs-lookup"><span data-stu-id="8cf48-103">D3DAUTHENTICATEDCONFIGURE\_INITIALIZE</span></span>

<span data-ttu-id="8cf48-104">Inizializza il canale autenticato.</span><span class="sxs-lookup"><span data-stu-id="8cf48-104">Initializes the authenticated channel.</span></span>



| <span data-ttu-id="8cf48-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cf48-105">Requirement</span></span> | <span data-ttu-id="8cf48-106">Valore</span><span class="sxs-lookup"><span data-stu-id="8cf48-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf48-107">GUID comando</span><span class="sxs-lookup"><span data-stu-id="8cf48-107">Command GUID</span></span> | <span data-ttu-id="8cf48-108">**\_Inizializzazione D3DAUTHENTICATEDCONFIGURE**</span><span class="sxs-lookup"><span data-stu-id="8cf48-108">**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**</span></span>                                                           |
| <span data-ttu-id="8cf48-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="8cf48-109">Input data</span></span>   | [<span data-ttu-id="8cf48-110">**\_CONFIGUREINITIALIZE D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="8cf48-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE**</span></span>](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a><span data-ttu-id="8cf48-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cf48-111">Remarks</span></span>

<span data-ttu-id="8cf48-112">Inviare questo comando una volta all'inizio della sessione.</span><span class="sxs-lookup"><span data-stu-id="8cf48-112">Send this command once, at the start of the session.</span></span> <span data-ttu-id="8cf48-113">Questo comando può essere inviato solo una volta per ogni canale autenticato.</span><span class="sxs-lookup"><span data-stu-id="8cf48-113">This command can be sent only one time for each authenticated channel.</span></span> <span data-ttu-id="8cf48-114">Il numero di sequenza di input viene ignorato per questo comando.</span><span class="sxs-lookup"><span data-stu-id="8cf48-114">The input sequence number is ignored for this command.</span></span>

<span data-ttu-id="8cf48-115">I tipi di canale seguenti supportano questo comando:</span><span class="sxs-lookup"><span data-stu-id="8cf48-115">The following channel types support this command:</span></span>

-   <span data-ttu-id="8cf48-116">**\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="8cf48-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="8cf48-117">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="8cf48-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf48-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cf48-118">Requirements</span></span>



| <span data-ttu-id="8cf48-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cf48-119">Requirement</span></span> | <span data-ttu-id="8cf48-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8cf48-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf48-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cf48-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf48-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8cf48-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8cf48-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cf48-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf48-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8cf48-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8cf48-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8cf48-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf48-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cf48-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cf48-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cf48-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf48-128">Comandi protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="8cf48-128">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="8cf48-129">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="8cf48-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="8cf48-130">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="8cf48-130">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




