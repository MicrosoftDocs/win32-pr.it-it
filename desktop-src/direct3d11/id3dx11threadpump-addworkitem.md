---
title: Metodo ID3DX11ThreadPump AddWorkItem (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Aggiunge un elemento di lavoro alla pompa di thread.
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Metodo AddWorkItem Direct3D 11
- Metodo AddWorkItem Direct3D 11, interfaccia ID3DX11ThreadPump
- Interfaccia ID3DX11ThreadPump Direct3D 11, metodo AddWorkItem
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354274"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a><span data-ttu-id="54db5-107">Metodo ID3DX11ThreadPump:: AddWorkItem</span><span class="sxs-lookup"><span data-stu-id="54db5-107">ID3DX11ThreadPump::AddWorkItem method</span></span>

> [!Note]  
> <span data-ttu-id="54db5-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="54db5-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="54db5-109">Aggiunge un elemento di lavoro alla pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="54db5-109">Adds a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="54db5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54db5-110">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="54db5-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="54db5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54db5-112">*pDataLoader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54db5-112">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54db5-113">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="54db5-113">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\***</span></span>

<span data-ttu-id="54db5-114">Caricatore che verrà utilizzato dal thread Pump quando un elemento di lavoro richiede il caricamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="54db5-114">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="54db5-115">*pDataProcessor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54db5-115">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54db5-116">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="54db5-116">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span></span>

<span data-ttu-id="54db5-117">Processore che verrà utilizzato dal thread Pump quando un elemento di lavoro richiede l'elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="54db5-117">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="54db5-118">*pHResult* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54db5-118">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54db5-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="54db5-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="54db5-120">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="54db5-120">A pointer to the return value.</span></span> <span data-ttu-id="54db5-121">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="54db5-121">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54db5-122">*ppDeviceObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="54db5-122">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54db5-123">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="54db5-123">Type: **void\*\***</span></span>

<span data-ttu-id="54db5-124">Dispositivo che usa l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="54db5-124">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54db5-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54db5-125">Return value</span></span>

<span data-ttu-id="54db5-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54db5-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54db5-127">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="54db5-127">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54db5-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54db5-128">Requirements</span></span>



| <span data-ttu-id="54db5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="54db5-129">Requirement</span></span> | <span data-ttu-id="54db5-130">Valore</span><span class="sxs-lookup"><span data-stu-id="54db5-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54db5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54db5-131">Header</span></span><br/>  | <dl> <span data-ttu-id="54db5-132"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="54db5-132"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="54db5-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="54db5-133">Library</span></span><br/> | <dl> <span data-ttu-id="54db5-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54db5-134"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54db5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54db5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54db5-136">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="54db5-136">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="54db5-137">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="54db5-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





