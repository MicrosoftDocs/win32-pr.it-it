---
title: Metodo ID3DX11ThreadPump GetQueueStatus (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Ottiene il numero di elementi in ognuna delle tre code all'interno della pompa di thread.
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Metodo GetQueueStatus Direct3D 11
- Metodo GetQueueStatus Direct3D 11, interfaccia ID3DX11ThreadPump
- Interfaccia ID3DX11ThreadPump Direct3D 11, metodo GetQueueStatus
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982232"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a><span data-ttu-id="6472f-107">Metodo ID3DX11ThreadPump:: GetQueueStatus</span><span class="sxs-lookup"><span data-stu-id="6472f-107">ID3DX11ThreadPump::GetQueueStatus method</span></span>

> [!Note]  
> <span data-ttu-id="6472f-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6472f-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="6472f-109">Ottiene il numero di elementi in ognuna delle tre code all'interno della pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="6472f-109">Gets the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="6472f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6472f-110">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="6472f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="6472f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6472f-112">*pIoQueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6472f-112">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6472f-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="6472f-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="6472f-114">Numero di elementi nella coda di I/O.</span><span class="sxs-lookup"><span data-stu-id="6472f-114">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="6472f-115">*pProcessQueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6472f-115">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6472f-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="6472f-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="6472f-117">Numero di elementi nella coda dei processi.</span><span class="sxs-lookup"><span data-stu-id="6472f-117">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="6472f-118">*pDeviceQueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6472f-118">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6472f-119">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="6472f-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="6472f-120">Numero di elementi nella coda del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6472f-120">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6472f-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6472f-121">Return value</span></span>

<span data-ttu-id="6472f-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6472f-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6472f-123">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6472f-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6472f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6472f-124">Requirements</span></span>



| <span data-ttu-id="6472f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6472f-125">Requirement</span></span> | <span data-ttu-id="6472f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6472f-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6472f-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6472f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6472f-128"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6472f-128"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="6472f-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="6472f-129">Library</span></span><br/> | <dl> <span data-ttu-id="6472f-130"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6472f-130"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6472f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6472f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6472f-132">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="6472f-132">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="6472f-133">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6472f-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

