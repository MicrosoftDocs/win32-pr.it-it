---
description: Specifica il tipo di processo identificato nella \_ struttura di output QUERYRESTRICTEDSHAREDRESOURCEPROCESS di D3DAUTHENTICATEDCHANNEL \_ .
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: Enumerazione D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127938"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a><span data-ttu-id="b163a-103">\_Enumerazione D3DAUTHENTICATEDCHANNEL PROCESSIDENTIFIERTYPE</span><span class="sxs-lookup"><span data-stu-id="b163a-103">D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE enumeration</span></span>

<span data-ttu-id="b163a-104">Specifica il tipo di processo identificato nella struttura di [**\_ \_ output QUERYRESTRICTEDSHAREDRESOURCEPROCESS di D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) .</span><span class="sxs-lookup"><span data-stu-id="b163a-104">Specifies the type of process that is identified in the [**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b163a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b163a-105">Syntax</span></span>


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a><span data-ttu-id="b163a-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="b163a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b163a-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="b163a-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="b163a-108">Tipo di processo sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b163a-108">Unknown process type.</span></span>

</dd> <dt>

<span data-ttu-id="b163a-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="b163a-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE\_DWM**</span></span>
</dt> <dd>

<span data-ttu-id="b163a-110">Processo di Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="b163a-110">Desktop Window Manager (DWM) process.</span></span>

</dd> <dt>

<span data-ttu-id="b163a-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**\_handle PROCESSIDTYPE**</span><span class="sxs-lookup"><span data-stu-id="b163a-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="b163a-112">Handle per un processo.</span><span class="sxs-lookup"><span data-stu-id="b163a-112">Handle to a process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b163a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b163a-113">Requirements</span></span>



| <span data-ttu-id="b163a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b163a-114">Requirement</span></span> | <span data-ttu-id="b163a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b163a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b163a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b163a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b163a-117">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b163a-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b163a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b163a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b163a-119">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b163a-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b163a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b163a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b163a-121"><dt>D3d9types. h (include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b163a-121"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b163a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b163a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b163a-123">Enumerazioni video Direct3D</span><span class="sxs-lookup"><span data-stu-id="b163a-123">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




