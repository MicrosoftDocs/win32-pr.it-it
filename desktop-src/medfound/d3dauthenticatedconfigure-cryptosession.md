---
description: Associa una sessione crittografica a un dispositivo decodificatore DirectX Video Acceleration 2 (DXVA-2) e a un dispositivo Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305432"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a><span data-ttu-id="969de-103">\_CRYPTOSESSION D3DAUTHENTICATEDCONFIGURE</span><span class="sxs-lookup"><span data-stu-id="969de-103">D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION</span></span>

<span data-ttu-id="969de-104">Associa una sessione crittografica a un dispositivo decodificatore DirectX Video Acceleration 2 (DXVA-2) e a un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="969de-104">Associates a cryptographic session with a DirectX Video Acceleration 2 (DXVA-2) decoder device and a Direct3D device.</span></span>



| <span data-ttu-id="969de-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="969de-105">Requirement</span></span> | <span data-ttu-id="969de-106">Valore</span><span class="sxs-lookup"><span data-stu-id="969de-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="969de-107">GUID comando</span><span class="sxs-lookup"><span data-stu-id="969de-107">Command GUID</span></span> | <span data-ttu-id="969de-108">**\_CRYPTOSESSION D3DAUTHENTICATEDCONFIGURE**</span><span class="sxs-lookup"><span data-stu-id="969de-108">**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**</span></span>                                                              |
| <span data-ttu-id="969de-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="969de-109">Input data</span></span>   | [<span data-ttu-id="969de-110">**\_CONFIGURECRYPTOSESSION D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="969de-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION**</span></span>](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a><span data-ttu-id="969de-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="969de-111">Remarks</span></span>

<span data-ttu-id="969de-112">Dopo l'invio di questo comando, è possibile inviare la query [D3DAUTHENTICATEDQUERY \_ OUTPUTID](d3dauthenticatedquery-outputid.md) per scoprire quali output video sono associati alla sessione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="969de-112">After this command is sent, you can send the [D3DAUTHENTICATEDQUERY\_OUTPUTID](d3dauthenticatedquery-outputid.md) query to find out which video outputs are associated with the cryptographic session.</span></span>

<span data-ttu-id="969de-113">I tipi di canale seguenti supportano questo comando:</span><span class="sxs-lookup"><span data-stu-id="969de-113">The following channel types support this command:</span></span>

-   <span data-ttu-id="969de-114">**\_D3d9 D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="969de-114">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="969de-115">**\_Software driver \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="969de-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="969de-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="969de-116">Requirements</span></span>



| <span data-ttu-id="969de-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="969de-117">Requirement</span></span> | <span data-ttu-id="969de-118">Valore</span><span class="sxs-lookup"><span data-stu-id="969de-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="969de-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="969de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="969de-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="969de-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="969de-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="969de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="969de-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="969de-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="969de-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="969de-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="969de-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="969de-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="969de-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="969de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="969de-126">Comandi protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="969de-126">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="969de-127">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="969de-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="969de-128">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="969de-128">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




