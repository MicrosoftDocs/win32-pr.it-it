---
description: La struttura MACFRAME è un'Unione dei protocolli iniziali più comuni.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: Unione MACFRAME (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307715"
---
# <a name="macframe-union"></a><span data-ttu-id="f5028-103">Unione MACFRAME</span><span class="sxs-lookup"><span data-stu-id="f5028-103">MACFRAME union</span></span>

<span data-ttu-id="f5028-104">La struttura **MACFRAME** è un'Unione dei protocolli iniziali più comuni.</span><span class="sxs-lookup"><span data-stu-id="f5028-104">The **MACFRAME** structure is a union of the most common initial protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5028-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5028-105">Syntax</span></span>


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a><span data-ttu-id="f5028-106">Members</span><span class="sxs-lookup"><span data-stu-id="f5028-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5028-107">**MacHeader**</span><span class="sxs-lookup"><span data-stu-id="f5028-107">**MacHeader**</span></span>
</dt> <dd>

<span data-ttu-id="f5028-108">Puntatore generico a un frame.</span><span class="sxs-lookup"><span data-stu-id="f5028-108">Generic pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="f5028-109">**Ethernet**</span><span class="sxs-lookup"><span data-stu-id="f5028-109">**Ethernet**</span></span>
</dt> <dd>

<span data-ttu-id="f5028-110">Puntatore Ethernet a un frame.</span><span class="sxs-lookup"><span data-stu-id="f5028-110">Ethernet pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="f5028-111">**Tokenring**</span><span class="sxs-lookup"><span data-stu-id="f5028-111">**Tokenring**</span></span>
</dt> <dd>

<span data-ttu-id="f5028-112">Puntatore all'anello token a un frame.</span><span class="sxs-lookup"><span data-stu-id="f5028-112">Token ring pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="f5028-113">**FDDI**</span><span class="sxs-lookup"><span data-stu-id="f5028-113">**Fddi**</span></span>
</dt> <dd>

<span data-ttu-id="f5028-114">Puntatore FDDI a un frame.</span><span class="sxs-lookup"><span data-stu-id="f5028-114">FDDI pointer to a frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5028-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5028-115">Remarks</span></span>

<span data-ttu-id="f5028-116">Questa struttura viene utilizzata con maggiore frequenza come sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="f5028-116">This structure is most frequently used as an overlay.</span></span> <span data-ttu-id="f5028-117">Per rendere accessibili le proprietà del primo protocollo, eseguire il cast del frame come lo stesso tipo del protocollo.</span><span class="sxs-lookup"><span data-stu-id="f5028-117">To make the properties of the first protocol accessible, cast the frame as the same type as the protocol.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5028-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5028-118">Requirements</span></span>



| <span data-ttu-id="f5028-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5028-119">Requirement</span></span> | <span data-ttu-id="f5028-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f5028-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f5028-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5028-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f5028-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f5028-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f5028-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5028-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f5028-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f5028-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f5028-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5028-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5028-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5028-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




