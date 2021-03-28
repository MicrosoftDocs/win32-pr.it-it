---
title: Metodo ID3DX11DataProcessor CreateDeviceObject (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Crea un oggetto dispositivo.
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- Metodo CreateDeviceObject Direct3D 11
- Metodo CreateDeviceObject Direct3D 11, interfaccia ID3DX11DataProcessor
- Interfaccia ID3DX11DataProcessor Direct3D 11, metodo CreateDeviceObject
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ff178cec1830d1b0213af23a2a70654416d35e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356034"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="f98dd-107">Metodo ID3DX11DataProcessor:: CreateDeviceObject</span><span class="sxs-lookup"><span data-stu-id="f98dd-107">ID3DX11DataProcessor::CreateDeviceObject method</span></span>

> [!Note]  
> <span data-ttu-id="f98dd-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f98dd-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f98dd-109">Crea un oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f98dd-109">Creates a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98dd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f98dd-110">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="f98dd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f98dd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f98dd-112">*ppDataObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f98dd-112">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f98dd-113">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="f98dd-113">Type: **void\*\***</span></span>

<span data-ttu-id="f98dd-114">Indirizzo di un puntatore all'oggetto dispositivo creato.</span><span class="sxs-lookup"><span data-stu-id="f98dd-114">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f98dd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f98dd-115">Return value</span></span>

<span data-ttu-id="f98dd-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f98dd-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f98dd-117">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f98dd-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f98dd-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f98dd-118">Remarks</span></span>

<span data-ttu-id="f98dd-119">Questo metodo viene utilizzato da un' [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="f98dd-119">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f98dd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f98dd-120">Requirements</span></span>



| <span data-ttu-id="f98dd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f98dd-121">Requirement</span></span> | <span data-ttu-id="f98dd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f98dd-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f98dd-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f98dd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f98dd-124"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f98dd-124"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="f98dd-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f98dd-125">Library</span></span><br/> | <dl> <span data-ttu-id="f98dd-126"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f98dd-126"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f98dd-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f98dd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98dd-128">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="f98dd-128">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="f98dd-129">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="f98dd-129">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





