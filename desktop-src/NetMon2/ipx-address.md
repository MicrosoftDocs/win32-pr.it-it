---
description: La \_ struttura dell'indirizzo IPX fornisce un indirizzo a livello di protocollo IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: Struttura IPX_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525867"
---
# <a name="ipx_address-structure"></a><span data-ttu-id="ca17b-103">\_Struttura di indirizzi IPX</span><span class="sxs-lookup"><span data-stu-id="ca17b-103">IPX\_ADDRESS structure</span></span>

<span data-ttu-id="ca17b-104">La struttura dell' **\_ indirizzo IPX** fornisce un indirizzo a livello di protocollo IPX.</span><span class="sxs-lookup"><span data-stu-id="ca17b-104">The **IPX\_ADDRESS** structure provides an address at the IPX protocol level.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca17b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca17b-105">Syntax</span></span>


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="ca17b-106">Members</span><span class="sxs-lookup"><span data-stu-id="ca17b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca17b-107">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="ca17b-107">**Subnet**</span></span>
</dt> <dd>

<span data-ttu-id="ca17b-108">Identificatore della subnet di rete.</span><span class="sxs-lookup"><span data-stu-id="ca17b-108">Network subnet identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ca17b-109">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="ca17b-109">**Address**</span></span>
</dt> <dd>

<span data-ttu-id="ca17b-110">Identificatore NIC subnet.</span><span class="sxs-lookup"><span data-stu-id="ca17b-110">Subnet NIC identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca17b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca17b-111">Requirements</span></span>



| <span data-ttu-id="ca17b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca17b-112">Requirement</span></span> | <span data-ttu-id="ca17b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ca17b-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca17b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca17b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ca17b-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca17b-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ca17b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca17b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ca17b-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca17b-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ca17b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca17b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca17b-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca17b-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




