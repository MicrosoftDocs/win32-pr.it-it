---
description: La struttura degli \_ indirizzi IP delle viti \_ è un indirizzo IP in una rete VINES.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Struttura VINES_IP_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346296"
---
# <a name="vines_ip_address-structure"></a><span data-ttu-id="ed1af-103">Struttura degli \_ indirizzi IP delle viti \_</span><span class="sxs-lookup"><span data-stu-id="ed1af-103">VINES\_IP\_ADDRESS structure</span></span>

<span data-ttu-id="ed1af-104">La struttura degli **\_ \_ indirizzi IP delle viti** è un indirizzo IP in una rete VINES.</span><span class="sxs-lookup"><span data-stu-id="ed1af-104">The **VINES\_IP\_ADDRESS** structure is an IP address on a Vines network.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed1af-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed1af-105">Syntax</span></span>


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="ed1af-106">Members</span><span class="sxs-lookup"><span data-stu-id="ed1af-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed1af-107">**NetID**</span><span class="sxs-lookup"><span data-stu-id="ed1af-107">**NetID**</span></span>
</dt> <dd>

<span data-ttu-id="ed1af-108">Identificatore di un computer specifico in una subnet specifica.</span><span class="sxs-lookup"><span data-stu-id="ed1af-108">The identifier of a specific machine on a specific subnet.</span></span>

</dd> <dt>

<span data-ttu-id="ed1af-109">**SubnetID**</span><span class="sxs-lookup"><span data-stu-id="ed1af-109">**SubnetID**</span></span>
</dt> <dd>

<span data-ttu-id="ed1af-110">Identificatore di una subnet specifica sull'intera rete.</span><span class="sxs-lookup"><span data-stu-id="ed1af-110">The identifier of a specific subnet on the whole network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed1af-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed1af-111">Requirements</span></span>



| <span data-ttu-id="ed1af-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed1af-112">Requirement</span></span> | <span data-ttu-id="ed1af-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ed1af-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1af-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed1af-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ed1af-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed1af-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ed1af-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed1af-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ed1af-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed1af-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ed1af-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed1af-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed1af-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed1af-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




