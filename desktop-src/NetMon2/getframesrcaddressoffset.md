---
description: La funzione GetFrameSrcAddressOffset restituisce l'offset dell'indirizzo di origine dei frame.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Funzione GetFrameSrcAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232677"
---
# <a name="getframesrcaddressoffset-function"></a><span data-ttu-id="a5986-103">GetFrameSrcAddressOffset (funzione)</span><span class="sxs-lookup"><span data-stu-id="a5986-103">GetFrameSrcAddressOffset function</span></span>

<span data-ttu-id="a5986-104">La funzione **GetFrameSrcAddressOffset** restituisce l'offset dell'indirizzo di origine del frame.</span><span class="sxs-lookup"><span data-stu-id="a5986-104">The **GetFrameSrcAddressOffset** function returns the offset of the frame's source address.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5986-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5986-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="a5986-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5986-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5986-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="a5986-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="a5986-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="a5986-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="a5986-109">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="a5986-109">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="a5986-110">Tipo di indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="a5986-110">Source address type.</span></span> <span data-ttu-id="a5986-111">Il valore del parametro può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5986-111">The parameter value can be one of the following:</span></span>

-   <span data-ttu-id="a5986-112">tipo di indirizzo \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="a5986-112">ADDRESS\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="a5986-113">INDIRIZZO \_ \_ IP tipo</span><span class="sxs-lookup"><span data-stu-id="a5986-113">ADDRESS\_TYPE\_IP</span></span>
-   <span data-ttu-id="a5986-114">tipo di indirizzo \_ \_ IPX</span><span class="sxs-lookup"><span data-stu-id="a5986-114">ADDRESS\_TYPE\_IPX</span></span>
-   <span data-ttu-id="a5986-115">tipo di indirizzo \_ \_ Tokenring</span><span class="sxs-lookup"><span data-stu-id="a5986-115">ADDRESS\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="a5986-116">tipo di indirizzo \_ \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="a5986-116">ADDRESS\_TYPE\_FDDI</span></span>
-   <span data-ttu-id="a5986-117">tipo di indirizzo \_ \_ XNS</span><span class="sxs-lookup"><span data-stu-id="a5986-117">ADDRESS\_TYPE\_XNS</span></span>
-   <span data-ttu-id="a5986-118">tipo di indirizzo \_ \_ \_ IP viti</span><span class="sxs-lookup"><span data-stu-id="a5986-118">ADDRESS\_TYPE\_VINES\_IP</span></span>
-   <span data-ttu-id="a5986-119">tipo di indirizzo \_ \_ ATM</span><span class="sxs-lookup"><span data-stu-id="a5986-119">ADDRESS\_TYPE\_ATM</span></span>

</dd> <dt>

<span data-ttu-id="a5986-120">*AddressLength*</span><span class="sxs-lookup"><span data-stu-id="a5986-120">*AddressLength*</span></span> 
</dt> <dd>

<span data-ttu-id="a5986-121">Puntatore a un **valore DWORD**, che, in restituzione, contiene la lunghezza dell'indirizzo, in byte.</span><span class="sxs-lookup"><span data-stu-id="a5986-121">Pointer to a **DWORD**, which on return, contains the length of the address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5986-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5986-122">Return value</span></span>

<span data-ttu-id="a5986-123">Se la funzione ha esito positivo, il valore restituito è l'offset per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="a5986-123">If the function is successful, the return value is the offset to the source address.</span></span>

<span data-ttu-id="a5986-124">Se la funzione ha esito negativo, il valore restituito è meno uno (-1).</span><span class="sxs-lookup"><span data-stu-id="a5986-124">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5986-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5986-125">Requirements</span></span>



| <span data-ttu-id="a5986-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5986-126">Requirement</span></span> | <span data-ttu-id="a5986-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a5986-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a5986-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5986-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a5986-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5986-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a5986-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5986-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a5986-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5986-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a5986-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5986-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5986-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5986-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a5986-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="a5986-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5986-135"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5986-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a5986-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a5986-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5986-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5986-137"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




