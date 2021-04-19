---
description: Aggiungere un elemento di lavoro alla pompa di thread.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'Metodo ID3DX10ThreadPump:: AddWorkItem (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323674"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a><span data-ttu-id="3d78d-103">Metodo ID3DX10ThreadPump:: AddWorkItem</span><span class="sxs-lookup"><span data-stu-id="3d78d-103">ID3DX10ThreadPump::AddWorkItem method</span></span>

<span data-ttu-id="3d78d-104">Aggiungere un elemento di lavoro alla pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="3d78d-104">Add a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d78d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d78d-105">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="3d78d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d78d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d78d-107">*pDataLoader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d78d-107">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d78d-108">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d78d-108">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\***</span></span>

<span data-ttu-id="3d78d-109">Caricatore che verrà utilizzato dal thread Pump quando un elemento di lavoro richiede il caricamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="3d78d-109">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="3d78d-110">*pDataProcessor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d78d-110">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d78d-111">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d78d-111">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span></span>

<span data-ttu-id="3d78d-112">Processore che verrà utilizzato dal thread Pump quando un elemento di lavoro richiede l'elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="3d78d-112">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="3d78d-113">*pHResult* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d78d-113">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d78d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="3d78d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="3d78d-115">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="3d78d-115">A pointer to the return value.</span></span> <span data-ttu-id="3d78d-116">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3d78d-116">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3d78d-117">*ppDeviceObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d78d-117">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d78d-118">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="3d78d-118">Type: **void\*\***</span></span>

<span data-ttu-id="3d78d-119">Dispositivo che usa l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d78d-119">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d78d-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d78d-120">Return value</span></span>

<span data-ttu-id="3d78d-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d78d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d78d-122">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3d78d-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d78d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d78d-123">Requirements</span></span>



| <span data-ttu-id="3d78d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d78d-124">Requirement</span></span> | <span data-ttu-id="3d78d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3d78d-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d78d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d78d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3d78d-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d78d-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d78d-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d78d-128">Library</span></span><br/> | <dl> <span data-ttu-id="3d78d-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d78d-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d78d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d78d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d78d-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="3d78d-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="3d78d-132">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="3d78d-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




