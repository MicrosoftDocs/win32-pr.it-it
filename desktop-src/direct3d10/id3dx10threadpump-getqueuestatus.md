---
description: Ottenere il numero di elementi in ognuna delle tre code all'interno della pompa di thread.
ms.assetid: b5b829a5-5ef7-4ef5-afb4-efe1bb22ae70
title: 'Metodo ID3DX10ThreadPump:: GetQueueStatus (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetQueueStatus
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4cf3b5879da0346cefbb5b8835d6922dd736cfd3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323672"
---
# <a name="id3dx10threadpumpgetqueuestatus-method"></a><span data-ttu-id="8286c-103">Metodo ID3DX10ThreadPump:: GetQueueStatus</span><span class="sxs-lookup"><span data-stu-id="8286c-103">ID3DX10ThreadPump::GetQueueStatus method</span></span>

<span data-ttu-id="8286c-104">Ottenere il numero di elementi in ognuna delle tre code all'interno della pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="8286c-104">Get the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="8286c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8286c-105">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="8286c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8286c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8286c-107">*pIoQueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8286c-107">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8286c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8286c-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8286c-109">Numero di elementi nella coda di I/O.</span><span class="sxs-lookup"><span data-stu-id="8286c-109">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="8286c-110">*pProcessQueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8286c-110">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8286c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8286c-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8286c-112">Numero di elementi nella coda dei processi.</span><span class="sxs-lookup"><span data-stu-id="8286c-112">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="8286c-113">*pDeviceQueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8286c-113">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8286c-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8286c-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8286c-115">Numero di elementi nella coda del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8286c-115">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8286c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8286c-116">Return value</span></span>

<span data-ttu-id="8286c-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8286c-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8286c-118">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8286c-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8286c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8286c-119">Requirements</span></span>



| <span data-ttu-id="8286c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8286c-120">Requirement</span></span> | <span data-ttu-id="8286c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8286c-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8286c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8286c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8286c-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8286c-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8286c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="8286c-124">Library</span></span><br/> | <dl> <span data-ttu-id="8286c-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8286c-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8286c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8286c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8286c-127">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="8286c-127">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="8286c-128">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="8286c-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
