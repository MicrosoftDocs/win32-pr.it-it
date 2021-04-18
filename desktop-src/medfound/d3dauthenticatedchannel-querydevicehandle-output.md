---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY DEVICEHANDLE.
ms.assetid: f2e0ae6c-dc97-46f7-933f-6c14d83adf18
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b862523c54dc9f483e63cee525dc61c5f469602d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305443"
---
# <a name="d3dauthenticatedchannel_querydevicehandle_output-structure"></a><span data-ttu-id="2ac79-103">\_Struttura di output QUERYDEVICEHANDLE di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="2ac79-103">D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT structure</span></span>

<span data-ttu-id="2ac79-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="2ac79-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) query.</span></span>

<span data-ttu-id="2ac79-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="2ac79-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac79-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ac79-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="2ac79-107">Members</span><span class="sxs-lookup"><span data-stu-id="2ac79-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2ac79-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="2ac79-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="2ac79-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="2ac79-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="2ac79-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="2ac79-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="2ac79-111">Handle per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ac79-111">A handle to the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ac79-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ac79-112">Requirements</span></span>



| <span data-ttu-id="2ac79-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ac79-113">Requirement</span></span> | <span data-ttu-id="2ac79-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2ac79-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac79-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ac79-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2ac79-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2ac79-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2ac79-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ac79-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2ac79-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ac79-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2ac79-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ac79-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ac79-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac79-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ac79-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ac79-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac79-122">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="2ac79-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2ac79-123">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="2ac79-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




