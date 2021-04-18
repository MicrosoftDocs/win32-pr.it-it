---
description: Divide i numeri interi estesi.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: RtlExtendedLargeIntegerDivide (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330417"
---
# <a name="rtlextendedlargeintegerdivide-function"></a><span data-ttu-id="98d63-103">RtlExtendedLargeIntegerDivide (funzione)</span><span class="sxs-lookup"><span data-stu-id="98d63-103">RtlExtendedLargeIntegerDivide function</span></span>

<span data-ttu-id="98d63-104">\[La funzione **RtlExtendedLargeIntegerDivide** viene esportata per supportare i binari dei driver esistenti ed è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="98d63-104">\[The **RtlExtendedLargeIntegerDivide** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="98d63-105">Per ottenere prestazioni migliori, usare il supporto del compilatore per le operazioni integer a 64 bit.\]</span><span class="sxs-lookup"><span data-stu-id="98d63-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="98d63-106">Divide i numeri interi estesi.</span><span class="sxs-lookup"><span data-stu-id="98d63-106">Divides extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d63-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98d63-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a><span data-ttu-id="98d63-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="98d63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98d63-109">*Dividendo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98d63-109">*Dividend* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98d63-110">Dividendo.</span><span class="sxs-lookup"><span data-stu-id="98d63-110">Dividend.</span></span>

</dd> <dt>

<span data-ttu-id="98d63-111">*Divisore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98d63-111">*Divisor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98d63-112">Divisore.</span><span class="sxs-lookup"><span data-stu-id="98d63-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="98d63-113">*Resto* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="98d63-113">*Remainder* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98d63-114">Puntatore al resto della divisione.</span><span class="sxs-lookup"><span data-stu-id="98d63-114">Pointer to division remainder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98d63-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98d63-115">Return value</span></span>

<span data-ttu-id="98d63-116">Restituisce il risultato dell'operazione di divisione.</span><span class="sxs-lookup"><span data-stu-id="98d63-116">Returns the result of the division operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d63-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="98d63-117">Remarks</span></span>

<span data-ttu-id="98d63-118">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="98d63-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d63-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98d63-119">Requirements</span></span>



| <span data-ttu-id="98d63-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="98d63-120">Requirement</span></span> | <span data-ttu-id="98d63-121">Valore</span><span class="sxs-lookup"><span data-stu-id="98d63-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="98d63-122">DLL</span><span class="sxs-lookup"><span data-stu-id="98d63-122">DLL</span></span><br/> | <dl> <span data-ttu-id="98d63-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98d63-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
