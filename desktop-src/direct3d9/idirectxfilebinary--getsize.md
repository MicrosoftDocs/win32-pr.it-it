---
description: Recupera le dimensioni dei dati binari. Deprecato.
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: 'Metodo IDirectXFileBinary:: GetSize (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 664e2bf026df6d9e4b5bc07067ce1ce7fe7669db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531003"
---
# <a name="idirectxfilebinarygetsize-method"></a><span data-ttu-id="06d44-104">Metodo IDirectXFileBinary:: GetSize</span><span class="sxs-lookup"><span data-stu-id="06d44-104">IDirectXFileBinary::GetSize method</span></span>

<span data-ttu-id="06d44-105">Recupera le dimensioni dei dati binari.</span><span class="sxs-lookup"><span data-stu-id="06d44-105">Retrieves the size of the binary data.</span></span> <span data-ttu-id="06d44-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="06d44-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="06d44-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06d44-107">Syntax</span></span>


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="06d44-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06d44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06d44-109">*pcbSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="06d44-109">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06d44-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="06d44-110">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06d44-111">Puntatore alle dimensioni restituite dei dati binari, in byte.</span><span class="sxs-lookup"><span data-stu-id="06d44-111">Pointer to the returned size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06d44-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06d44-112">Return value</span></span>

<span data-ttu-id="06d44-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06d44-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06d44-114">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06d44-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="06d44-115">Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="06d44-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="06d44-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06d44-116">Requirements</span></span>



| <span data-ttu-id="06d44-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="06d44-117">Requirement</span></span> | <span data-ttu-id="06d44-118">Valore</span><span class="sxs-lookup"><span data-stu-id="06d44-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06d44-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06d44-119">Header</span></span><br/>  | <dl> <span data-ttu-id="06d44-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="06d44-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="06d44-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="06d44-121">Library</span></span><br/> | <dl> <span data-ttu-id="06d44-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06d44-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06d44-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06d44-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06d44-124">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="06d44-124">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
