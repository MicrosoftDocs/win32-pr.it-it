---
description: Specifica lo spessore della linea.
ms.assetid: cedf9217-2b47-40c3-a64c-9872c1083d71
title: 'Metodo ID3DXLine:: sewidth (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetWidth
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d357d7516233caf6ef9206aa2aecc2a98a435cde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058674"
---
# <a name="id3dxlinesetwidth-method"></a><span data-ttu-id="80691-103">Metodo ID3DXLine:: sewidth</span><span class="sxs-lookup"><span data-stu-id="80691-103">ID3DXLine::SetWidth method</span></span>

<span data-ttu-id="80691-104">Specifica lo spessore della linea.</span><span class="sxs-lookup"><span data-stu-id="80691-104">Specifies the thickness of the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="80691-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80691-105">Syntax</span></span>


```C++
HRESULT SetWidth(
  [in] FLOAT fWidth
);
```



## <a name="parameters"></a><span data-ttu-id="80691-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80691-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80691-107">*fWidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80691-107">*fWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80691-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80691-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80691-109">Descrive lo spessore riga.</span><span class="sxs-lookup"><span data-stu-id="80691-109">Describes the line width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80691-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80691-110">Return value</span></span>

<span data-ttu-id="80691-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80691-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80691-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80691-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80691-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="80691-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="80691-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80691-114">Requirements</span></span>



| <span data-ttu-id="80691-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="80691-115">Requirement</span></span> | <span data-ttu-id="80691-116">Valore</span><span class="sxs-lookup"><span data-stu-id="80691-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80691-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80691-117">Header</span></span><br/>  | <dl> <span data-ttu-id="80691-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="80691-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="80691-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="80691-119">Library</span></span><br/> | <dl> <span data-ttu-id="80691-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80691-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80691-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80691-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80691-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="80691-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
