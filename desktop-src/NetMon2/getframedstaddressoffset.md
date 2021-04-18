---
description: La funzione GetFrameDstAddressOffset restituisce l'offset all'indirizzo di destinazione di un frame specificato.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Funzione GetFrameDstAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305909"
---
# <a name="getframedstaddressoffset-function"></a><span data-ttu-id="81def-103">GetFrameDstAddressOffset (funzione)</span><span class="sxs-lookup"><span data-stu-id="81def-103">GetFrameDstAddressOffset function</span></span>

<span data-ttu-id="81def-104">La funzione **GetFrameDstAddressOffset** restituisce l'offset all'indirizzo di destinazione di un frame specificato.</span><span class="sxs-lookup"><span data-stu-id="81def-104">The **GetFrameDstAddressOffset** function returns the offset to the destination address of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="81def-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81def-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="81def-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="81def-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81def-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81def-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81def-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="81def-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="81def-109">*AddressType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81def-109">*AddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81def-110">Tipo di indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="81def-110">Type of the destination address.</span></span> <span data-ttu-id="81def-111">Specificare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="81def-111">Specify one of the following values:</span></span>

<span data-ttu-id="81def-112">tipo di indirizzo IP indirizzo IP tipo indirizzo IP tipo di indirizzo IPX tipo di indirizzo Tokenring tipo di indirizzo FDDI tipo di indirizzo XNS tipo di indirizzo di tipo indirizzo \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ IP viti \_ \_ ATM.</span><span class="sxs-lookup"><span data-stu-id="81def-112">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_IP ADDRESS\_TYPE\_IPX ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI ADDRESS\_TYPE\_XNS ADDRESS\_TYPE\_VINES\_IP ADDRESS\_TYPE\_ATM.</span></span>

</dd> <dt>

<span data-ttu-id="81def-113">*AddressLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81def-113">*AddressLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81def-114">Lunghezza, in byte, dell'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="81def-114">Length of the destination address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81def-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81def-115">Return value</span></span>

<span data-ttu-id="81def-116">Se la funzione ha esito positivo, il valore restituito è l'offset, espresso in byte, al tipo di indirizzo richiesto.</span><span class="sxs-lookup"><span data-stu-id="81def-116">If the function is successful, the return value is the offset (measured in bytes) to the requested address type.</span></span>

<span data-ttu-id="81def-117">Se la funzione ha esito negativo, il valore restituito è meno uno (-1).</span><span class="sxs-lookup"><span data-stu-id="81def-117">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="81def-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="81def-118">Remarks</span></span>

<span data-ttu-id="81def-119">Se il parametro *addressType* è impostato sul tipo di indirizzo \_ \_ Ethernet, il valore restituito della funzione **GetFrameDstAddressOffset** è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="81def-119">If the *AddressType* parameter is set to ADDRESS\_TYPE\_ETHERNET, the return value of the **GetFrameDstAddressOffset** function is always zero.</span></span> <span data-ttu-id="81def-120">L'offset di un indirizzo Ethernet è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="81def-120">The offset of an Ethernet address is always zero.</span></span>

<span data-ttu-id="81def-121">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameDstAddressOffset** .</span><span class="sxs-lookup"><span data-stu-id="81def-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameDstAddressOffset** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="81def-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81def-122">Requirements</span></span>



| <span data-ttu-id="81def-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="81def-123">Requirement</span></span> | <span data-ttu-id="81def-124">Valore</span><span class="sxs-lookup"><span data-stu-id="81def-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81def-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81def-125">Minimum supported client</span></span><br/> | <span data-ttu-id="81def-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81def-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="81def-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81def-127">Minimum supported server</span></span><br/> | <span data-ttu-id="81def-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81def-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="81def-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81def-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="81def-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="81def-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="81def-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="81def-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="81def-132"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81def-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="81def-133">DLL</span><span class="sxs-lookup"><span data-stu-id="81def-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81def-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81def-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




