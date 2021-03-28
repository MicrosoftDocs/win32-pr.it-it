---
title: Metodo di elaborazione ID3DX11DataProcessor (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Elabora i dati.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Metodo di elaborazione Direct3D 11
- Metodo di elaborazione Direct3D 11, interfaccia ID3DX11DataProcessor
- Interfaccia ID3DX11DataProcessor Direct3D 11, metodo Process
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530949"
---
# <a name="id3dx11dataprocessorprocess-method"></a><span data-ttu-id="39ead-107">ID3DX11DataProcessor::P metodo rocess</span><span class="sxs-lookup"><span data-stu-id="39ead-107">ID3DX11DataProcessor::Process method</span></span>

> [!Note]  
> <span data-ttu-id="39ead-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="39ead-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="39ead-109">Elabora i dati.</span><span class="sxs-lookup"><span data-stu-id="39ead-109">Processes data.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ead-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39ead-110">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="39ead-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="39ead-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ead-112">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39ead-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ead-113">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="39ead-113">Type: **void\***</span></span>

<span data-ttu-id="39ead-114">Puntatore ai dati da elaborare.</span><span class="sxs-lookup"><span data-stu-id="39ead-114">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="39ead-115">*cBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39ead-115">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ead-116">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39ead-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39ead-117">Dimensione dei dati da elaborare.</span><span class="sxs-lookup"><span data-stu-id="39ead-117">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ead-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39ead-118">Return value</span></span>

<span data-ttu-id="39ead-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39ead-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39ead-120">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="39ead-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="39ead-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="39ead-121">Remarks</span></span>

<span data-ttu-id="39ead-122">Questo metodo viene utilizzato da un' [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="39ead-122">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39ead-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39ead-123">Requirements</span></span>



| <span data-ttu-id="39ead-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="39ead-124">Requirement</span></span> | <span data-ttu-id="39ead-125">Valore</span><span class="sxs-lookup"><span data-stu-id="39ead-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39ead-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39ead-126">Header</span></span><br/>  | <dl> <span data-ttu-id="39ead-127"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="39ead-127"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="39ead-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="39ead-128">Library</span></span><br/> | <dl> <span data-ttu-id="39ead-129"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39ead-129"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="39ead-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39ead-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ead-131">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="39ead-131">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="39ead-132">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="39ead-132">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

