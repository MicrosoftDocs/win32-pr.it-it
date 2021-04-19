---
description: Chiude il gestore OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: OcTerminate (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326286"
---
# <a name="octerminate-function"></a><span data-ttu-id="0218d-103">OcTerminate (funzione)</span><span class="sxs-lookup"><span data-stu-id="0218d-103">OcTerminate function</span></span>

<span data-ttu-id="0218d-104">Chiude il gestore OC.</span><span class="sxs-lookup"><span data-stu-id="0218d-104">Closes the OC manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="0218d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0218d-105">Syntax</span></span>


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a><span data-ttu-id="0218d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0218d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0218d-107">*OcManagerContext* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0218d-107">*OcManagerContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0218d-108">In input, contiene il puntatore di contesto del gestore OC restituito da [**OcInitialize**](ocinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="0218d-108">On input, contains the OC manager context pointer returned by [**OcInitialize**](ocinitialize.md).</span></span> <span data-ttu-id="0218d-109">Nell'output, riceve **null**.</span><span class="sxs-lookup"><span data-stu-id="0218d-109">On output, receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0218d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0218d-110">Return value</span></span>

<span data-ttu-id="0218d-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0218d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0218d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0218d-112">Remarks</span></span>

<span data-ttu-id="0218d-113">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0218d-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0218d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0218d-114">Requirements</span></span>



| <span data-ttu-id="0218d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0218d-115">Requirement</span></span> | <span data-ttu-id="0218d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0218d-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0218d-117">DLL</span><span class="sxs-lookup"><span data-stu-id="0218d-117">DLL</span></span><br/> | <dl> <span data-ttu-id="0218d-118"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0218d-118"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0218d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0218d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0218d-120">**OcInitialize**</span><span class="sxs-lookup"><span data-stu-id="0218d-120">**OcInitialize**</span></span>](ocinitialize.md)
</dt> </dl>

 

 
