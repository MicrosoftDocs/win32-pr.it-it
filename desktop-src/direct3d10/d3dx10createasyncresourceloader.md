---
description: Creare un caricatore di risorse asincrono.
ms.assetid: 1b3eb21c-4ba6-4910-b2f0-2ffa4ae50e47
title: Funzione D3DX10CreateAsyncResourceLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncResourceLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0539817ffff75c28af41289fc5197f6440a915bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322420"
---
# <a name="d3dx10createasyncresourceloader-function"></a><span data-ttu-id="6cd9a-103">D3DX10CreateAsyncResourceLoader (funzione)</span><span class="sxs-lookup"><span data-stu-id="6cd9a-103">D3DX10CreateAsyncResourceLoader function</span></span>

<span data-ttu-id="6cd9a-104">Creare un caricatore di risorse asincrono.</span><span class="sxs-lookup"><span data-stu-id="6cd9a-104">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd9a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6cd9a-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="6cd9a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6cd9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd9a-107">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cd9a-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd9a-108">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cd9a-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6cd9a-109">Handle per il modulo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6cd9a-109">Handle to the resource module.</span></span> <span data-ttu-id="6cd9a-110">Usare la [funzione GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per ottenere l'handle.</span><span class="sxs-lookup"><span data-stu-id="6cd9a-110">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="6cd9a-111">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cd9a-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd9a-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6cd9a-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6cd9a-113">Nome della risorsa in hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="6cd9a-113">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="6cd9a-114">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6cd9a-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6cd9a-115">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6cd9a-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="6cd9a-116">*ppDataLoader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6cd9a-116">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd9a-117">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6cd9a-117">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="6cd9a-118">Indirizzo di un puntatore al processore di dati asincrono (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="6cd9a-118">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd9a-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6cd9a-119">Return value</span></span>

<span data-ttu-id="6cd9a-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6cd9a-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6cd9a-121">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6cd9a-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd9a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cd9a-122">Requirements</span></span>



| <span data-ttu-id="6cd9a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cd9a-123">Requirement</span></span> | <span data-ttu-id="6cd9a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6cd9a-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd9a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cd9a-125">Header</span></span><br/> | <dl> <span data-ttu-id="6cd9a-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cd9a-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cd9a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6cd9a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd9a-128">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="6cd9a-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
