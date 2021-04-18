---
description: Contiene un Message Authentication Code (MAC).
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: Struttura D3D_OMAC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21c710b21c31147f7208ddd1637426aeafb60234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305457"
---
# <a name="d3d_omac-structure"></a><span data-ttu-id="71b37-103">\_Struttura OMAC D3D</span><span class="sxs-lookup"><span data-stu-id="71b37-103">D3D\_OMAC structure</span></span>

<span data-ttu-id="71b37-104">Contiene un Message Authentication Code (MAC).</span><span class="sxs-lookup"><span data-stu-id="71b37-104">Contains a Message Authentication Code (MAC).</span></span>

## <a name="syntax"></a><span data-ttu-id="71b37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71b37-105">Syntax</span></span>


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a><span data-ttu-id="71b37-106">Members</span><span class="sxs-lookup"><span data-stu-id="71b37-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="71b37-107">**OMAC**</span><span class="sxs-lookup"><span data-stu-id="71b37-107">**Omac**</span></span>
</dt> <dd>

<span data-ttu-id="71b37-108">Matrice di byte che contiene il valore MAC crittografico del messaggio.</span><span class="sxs-lookup"><span data-stu-id="71b37-108">A byte array that contains the cryptographic MAC value of the message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71b37-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71b37-109">Requirements</span></span>



| <span data-ttu-id="71b37-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="71b37-110">Requirement</span></span> | <span data-ttu-id="71b37-111">Valore</span><span class="sxs-lookup"><span data-stu-id="71b37-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71b37-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71b37-112">Minimum supported client</span></span><br/> | <span data-ttu-id="71b37-113">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="71b37-113">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="71b37-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71b37-114">Minimum supported server</span></span><br/> | <span data-ttu-id="71b37-115">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="71b37-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="71b37-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71b37-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b37-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b37-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b37-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71b37-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b37-119">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="71b37-119">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




