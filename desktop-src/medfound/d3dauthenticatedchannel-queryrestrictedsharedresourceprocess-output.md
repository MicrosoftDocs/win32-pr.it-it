---
description: Contiene la risposta a una \_ query D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESS.
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bd93e1cadb7da500a82218924044af79fbb1f493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127926"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a><span data-ttu-id="3882b-103">\_Struttura di output QUERYRESTRICTEDSHAREDRESOURCEPROCESS di D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="3882b-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT structure</span></span>

<span data-ttu-id="3882b-104">Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .</span><span class="sxs-lookup"><span data-stu-id="3882b-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="3882b-105">Per inviare la query, chiamare [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="3882b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="3882b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3882b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="3882b-107">Members</span><span class="sxs-lookup"><span data-stu-id="3882b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3882b-108">**Output**</span><span class="sxs-lookup"><span data-stu-id="3882b-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="3882b-109">Struttura [**di \_ \_ output della query D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) che contiene un Message Authentication Code (Mac) e altri dati.</span><span class="sxs-lookup"><span data-stu-id="3882b-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="3882b-110">**ProcessIndex**</span><span class="sxs-lookup"><span data-stu-id="3882b-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="3882b-111">Indice del processo nell'elenco dei processi.</span><span class="sxs-lookup"><span data-stu-id="3882b-111">The index of the process in the list of processes.</span></span>

</dd> <dt>

<span data-ttu-id="3882b-112">**ProcessIdentifer**</span><span class="sxs-lookup"><span data-stu-id="3882b-112">**ProcessIdentifer**</span></span>
</dt> <dd>

<span data-ttu-id="3882b-113">Valore [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) che specifica il tipo di processo.</span><span class="sxs-lookup"><span data-stu-id="3882b-113">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span>

</dd> <dt>

<span data-ttu-id="3882b-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="3882b-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="3882b-115">Handle di processo.</span><span class="sxs-lookup"><span data-stu-id="3882b-115">A process handle.</span></span> <span data-ttu-id="3882b-116">Se il membro **ProcessIdentifier** è uguale a **PROCESSIDTYPE \_ handle**, il membro **ProcessHandle** contiene un handle valido a un processo.</span><span class="sxs-lookup"><span data-stu-id="3882b-116">If the **ProcessIdentifier** member equals **PROCESSIDTYPE\_HANDLE**, the **ProcessHandle** member contains a valid handle to a process.</span></span> <span data-ttu-id="3882b-117">In caso contrario, questo membro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3882b-117">Otherwise, this member is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3882b-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3882b-118">Remarks</span></span>

<span data-ttu-id="3882b-119">Il processo di Gestione finestre desktop (DWM) viene identificato impostando **ProcessIdentifier** uguale a **PROCESSIDTYPE \_ DWM**.</span><span class="sxs-lookup"><span data-stu-id="3882b-119">The Desktop Window Manager (DWM) process is identified by setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="3882b-120">Per identificare altri processi, impostare l'handle di processo in **ProcessHandle** e impostare **ProcessIdentifier** uguale a **PROCESSIDTYPE \_ handle**.</span><span class="sxs-lookup"><span data-stu-id="3882b-120">Other processes are identified by setting the process handle in **ProcessHandle** and setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_HANDLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3882b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3882b-121">Requirements</span></span>



| <span data-ttu-id="3882b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3882b-122">Requirement</span></span> | <span data-ttu-id="3882b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3882b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3882b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3882b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3882b-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3882b-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3882b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3882b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3882b-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3882b-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3882b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3882b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3882b-129"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3882b-129"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3882b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3882b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3882b-131">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="3882b-131">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="3882b-132">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="3882b-132">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




