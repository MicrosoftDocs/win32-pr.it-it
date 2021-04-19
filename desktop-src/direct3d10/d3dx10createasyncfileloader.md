---
description: Creare un caricatore di file asincrono.
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: Funzione D3DX10CreateAsyncFileLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e98bccf709fa4a6d921e266148b94fd8623429ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322421"
---
# <a name="d3dx10createasyncfileloader-function"></a><span data-ttu-id="29233-103">D3DX10CreateAsyncFileLoader (funzione)</span><span class="sxs-lookup"><span data-stu-id="29233-103">D3DX10CreateAsyncFileLoader function</span></span>

<span data-ttu-id="29233-104">Creare un caricatore di file asincrono.</span><span class="sxs-lookup"><span data-stu-id="29233-104">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="29233-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29233-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="29233-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="29233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29233-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29233-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29233-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29233-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29233-109">Nome del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="29233-109">The name of the file to load.</span></span> <span data-ttu-id="29233-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="29233-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="29233-111">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="29233-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="29233-112">*ppDataLoader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="29233-112">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29233-113">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="29233-113">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="29233-114">Indirizzo di un puntatore al caricatore di dati asincrono (vedere [**interfaccia ID3DX10DataLoader**](id3dx10dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="29233-114">Address of a pointer to the asynchronous-data loader (see [**ID3DX10DataLoader Interface**](id3dx10dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29233-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29233-115">Return value</span></span>

<span data-ttu-id="29233-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="29233-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="29233-117">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="29233-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29233-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29233-118">Requirements</span></span>



| <span data-ttu-id="29233-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="29233-119">Requirement</span></span> | <span data-ttu-id="29233-120">Valore</span><span class="sxs-lookup"><span data-stu-id="29233-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29233-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29233-121">Header</span></span><br/> | <dl> <span data-ttu-id="29233-122"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="29233-122"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29233-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29233-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29233-124">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="29233-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
