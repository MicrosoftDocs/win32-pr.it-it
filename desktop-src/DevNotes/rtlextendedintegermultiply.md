---
description: Moltiplica gli Integer estesi.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: RtlExtendedIntegerMultiply (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326832"
---
# <a name="rtlextendedintegermultiply-function"></a><span data-ttu-id="48b33-103">RtlExtendedIntegerMultiply (funzione)</span><span class="sxs-lookup"><span data-stu-id="48b33-103">RtlExtendedIntegerMultiply function</span></span>

<span data-ttu-id="48b33-104">\[La funzione **RtlExtendedIntegerMultiply** viene esportata per supportare i binari dei driver esistenti ed è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="48b33-104">\[The **RtlExtendedIntegerMultiply** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="48b33-105">Per ottenere prestazioni migliori, usare il supporto del compilatore per le operazioni integer a 64 bit.\]</span><span class="sxs-lookup"><span data-stu-id="48b33-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="48b33-106">Moltiplica gli Integer estesi.</span><span class="sxs-lookup"><span data-stu-id="48b33-106">Multiplies extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b33-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48b33-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a><span data-ttu-id="48b33-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="48b33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b33-109">*Multiplicand* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48b33-109">*Multiplicand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b33-110">Multiplicand.</span><span class="sxs-lookup"><span data-stu-id="48b33-110">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="48b33-111">*Moltiplicatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48b33-111">*Multiplier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b33-112">Moltiplicatore.</span><span class="sxs-lookup"><span data-stu-id="48b33-112">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b33-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48b33-113">Return value</span></span>

<span data-ttu-id="48b33-114">Restituisce il risultato della moltiplicazione.</span><span class="sxs-lookup"><span data-stu-id="48b33-114">Returns multiplication result.</span></span>

## <a name="remarks"></a><span data-ttu-id="48b33-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="48b33-115">Remarks</span></span>

<span data-ttu-id="48b33-116">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="48b33-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b33-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48b33-117">Requirements</span></span>



| <span data-ttu-id="48b33-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="48b33-118">Requirement</span></span> | <span data-ttu-id="48b33-119">Valore</span><span class="sxs-lookup"><span data-stu-id="48b33-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="48b33-120">DLL</span><span class="sxs-lookup"><span data-stu-id="48b33-120">DLL</span></span><br/> | <dl> <span data-ttu-id="48b33-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48b33-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
