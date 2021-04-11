---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY CURRENTENCRYPTIONWHENACCESSIBLE.
ms.assetid: 66735ce3-c16b-4eca-9283-5d3bc37d73d3
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cfc0075678163b273acad72fa1724cbca8a29cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127923"
---
# <a name="d3dauthenticatedchannel_queryuncompressedencryptionlevel_output-structure"></a><span data-ttu-id="4e55f-103">\_Struttura di output QUERYUNCOMPRESSEDENCRYPTIONLEVEL di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="4e55f-103">D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT structure</span></span>

<span data-ttu-id="4e55f-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) .</span><span class="sxs-lookup"><span data-stu-id="4e55f-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) query.</span></span>

<span data-ttu-id="4e55f-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="4e55f-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e55f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e55f-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  GUID                                 EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="4e55f-107">Members</span><span class="sxs-lookup"><span data-stu-id="4e55f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e55f-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="4e55f-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="4e55f-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="4e55f-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="4e55f-110">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="4e55f-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="4e55f-111">GUID che specifica il tipo di crittografia corrente.</span><span class="sxs-lookup"><span data-stu-id="4e55f-111">A GUID that specifies the current encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e55f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e55f-112">Requirements</span></span>



| <span data-ttu-id="4e55f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e55f-113">Requirement</span></span> | <span data-ttu-id="4e55f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4e55f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e55f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e55f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4e55f-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e55f-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4e55f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e55f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4e55f-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e55f-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4e55f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e55f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e55f-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e55f-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e55f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e55f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e55f-122">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="4e55f-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="4e55f-123">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="4e55f-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




