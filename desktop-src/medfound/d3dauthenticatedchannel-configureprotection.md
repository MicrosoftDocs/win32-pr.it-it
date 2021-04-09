---
description: Contiene i dati di input per un \_ comando D3DAUTHENTICATEDCONFIGURE Protection.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fc1daee7bfd9320539a03974ab431c4ba588d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878453"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a><span data-ttu-id="1446f-103">\_Struttura D3DAUTHENTICATEDCHANNEL CONFIGUREPROTECTION</span><span class="sxs-lookup"><span data-stu-id="1446f-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREPROTECTION structure</span></span>

<span data-ttu-id="1446f-104">Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ Protection**](d3dauthenticatedconfigure-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="1446f-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_PROTECTION**](d3dauthenticatedconfigure-protection.md) command.</span></span>

<span data-ttu-id="1446f-105">Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="1446f-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="1446f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1446f-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a><span data-ttu-id="1446f-107">Members</span><span class="sxs-lookup"><span data-stu-id="1446f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1446f-108">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="1446f-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="1446f-109">D3DAUTHENTICATEDCHANNEL configura la struttura di [**\_ \_ input**](d3dauthenticatedchannel-configure-input.md) che contiene il GUID del comando e altri dati.</span><span class="sxs-lookup"><span data-stu-id="1446f-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="1446f-110">**Protezioni**</span><span class="sxs-lookup"><span data-stu-id="1446f-110">**Protections**</span></span>
</dt> <dd>

<span data-ttu-id="1446f-111">Struttura [**di \_ \_ flag di protezione D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md) che specifica il livello di protezione.</span><span class="sxs-lookup"><span data-stu-id="1446f-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1446f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1446f-112">Requirements</span></span>



| <span data-ttu-id="1446f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1446f-113">Requirement</span></span> | <span data-ttu-id="1446f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1446f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1446f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1446f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1446f-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1446f-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1446f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1446f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1446f-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1446f-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1446f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1446f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1446f-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1446f-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1446f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1446f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1446f-122">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="1446f-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="1446f-123">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="1446f-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




