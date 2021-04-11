---
description: Applica un modello stipple alla riga.
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'Metodo ID3DXLine:: sepattern (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80a0485991bc06bdb9fcd3280017d4cc60b492ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132390"
---
# <a name="id3dxlinesetpattern-method"></a><span data-ttu-id="09f76-103">Metodo ID3DXLine:: sepattern</span><span class="sxs-lookup"><span data-stu-id="09f76-103">ID3DXLine::SetPattern method</span></span>

<span data-ttu-id="09f76-104">Applica un modello stipple alla riga.</span><span class="sxs-lookup"><span data-stu-id="09f76-104">Applies a stipple pattern to the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f76-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09f76-105">Syntax</span></span>


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a><span data-ttu-id="09f76-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="09f76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f76-107">*dwPattern* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09f76-107">*dwPattern* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f76-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09f76-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09f76-109">Descrive il modello Stipple: 1 è opaco, 0 è trasparente.</span><span class="sxs-lookup"><span data-stu-id="09f76-109">Describes the stipple pattern: 1 is opaque, 0 is transparent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f76-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09f76-110">Return value</span></span>

<span data-ttu-id="09f76-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09f76-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09f76-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09f76-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="09f76-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="09f76-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="09f76-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09f76-114">Requirements</span></span>



| <span data-ttu-id="09f76-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="09f76-115">Requirement</span></span> | <span data-ttu-id="09f76-116">Valore</span><span class="sxs-lookup"><span data-stu-id="09f76-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09f76-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09f76-117">Header</span></span><br/>  | <dl> <span data-ttu-id="09f76-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="09f76-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="09f76-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="09f76-119">Library</span></span><br/> | <dl> <span data-ttu-id="09f76-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09f76-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="09f76-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09f76-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f76-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="09f76-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
