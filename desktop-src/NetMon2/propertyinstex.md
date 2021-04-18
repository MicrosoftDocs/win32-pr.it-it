---
description: La struttura PROPERTYINSTEX definisce un'istanza di proprietà estesa a mano libera.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Struttura PROPERTYINSTEX (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306481"
---
# <a name="propertyinstex-structure"></a><span data-ttu-id="0ec7b-103">Struttura PROPERTYINSTEX</span><span class="sxs-lookup"><span data-stu-id="0ec7b-103">PROPERTYINSTEX structure</span></span>

<span data-ttu-id="0ec7b-104">La struttura **PROPERTYINSTEX** definisce un'istanza di proprietà estesa a mano libera.</span><span class="sxs-lookup"><span data-stu-id="0ec7b-104">The **PROPERTYINSTEX** structure defines a freeform, extended property instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ec7b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ec7b-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a><span data-ttu-id="0ec7b-106">Members</span><span class="sxs-lookup"><span data-stu-id="0ec7b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ec7b-107">**Length**</span><span class="sxs-lookup"><span data-stu-id="0ec7b-107">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="0ec7b-108">Lunghezza dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="0ec7b-108">Length of the data in Bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0ec7b-109">**LengthEx**</span><span class="sxs-lookup"><span data-stu-id="0ec7b-109">**LengthEx**</span></span>
</dt> <dd>

<span data-ttu-id="0ec7b-110">Lunghezza dei dati estesi.</span><span class="sxs-lookup"><span data-stu-id="0ec7b-110">Length of the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="0ec7b-111">**lpData**</span><span class="sxs-lookup"><span data-stu-id="0ec7b-111">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="0ec7b-112">Puntatore ai dati estesi.</span><span class="sxs-lookup"><span data-stu-id="0ec7b-112">Pointer to the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="0ec7b-113">**Byte**</span><span class="sxs-lookup"><span data-stu-id="0ec7b-113">**Byte**</span></span>
</dt> <dd>

<span data-ttu-id="0ec7b-114">Puntatore ai dati **byte** .</span><span class="sxs-lookup"><span data-stu-id="0ec7b-114">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="0ec7b-115">**Word**</span><span class="sxs-lookup"><span data-stu-id="0ec7b-115">**Word**</span></span>
</dt> <dd>

<span data-ttu-id="0ec7b-116">Puntatore ai dati di **Word** .</span><span class="sxs-lookup"><span data-stu-id="0ec7b-116">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="0ec7b-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="0ec7b-117">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="0ec7b-118">Puntatore ai dati **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0ec7b-118">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="0ec7b-119">**LargeInt**</span><span class="sxs-lookup"><span data-stu-id="0ec7b-119">**LargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="0ec7b-120">Puntatore ai dati **largeInt** .</span><span class="sxs-lookup"><span data-stu-id="0ec7b-120">Pointer to the **LARGEINT** data.</span></span>

</dd> <dt>

<span data-ttu-id="0ec7b-121">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="0ec7b-121">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="0ec7b-122">Puntatore ai dati di **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="0ec7b-122">Pointer to the **SYSTEMTIME** data.</span></span>

</dd> <dt>

<span data-ttu-id="0ec7b-123">**TypedString**</span><span class="sxs-lookup"><span data-stu-id="0ec7b-123">**TypedString**</span></span>
</dt> <dd>

<span data-ttu-id="0ec7b-124">Stringa tipizzata che può avere dati estesi.</span><span class="sxs-lookup"><span data-stu-id="0ec7b-124">A typed string that may have extended data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ec7b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ec7b-125">Requirements</span></span>



| <span data-ttu-id="0ec7b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ec7b-126">Requirement</span></span> | <span data-ttu-id="0ec7b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0ec7b-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec7b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ec7b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0ec7b-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ec7b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0ec7b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ec7b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0ec7b-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ec7b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0ec7b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ec7b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ec7b-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ec7b-133"><dt>Netmon.h</dt></span></span> </dl> |



 

 




