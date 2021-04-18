---
description: Rimuovere un osso.
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: 'Metodo ID3DX10SkinInfo:: RemoveBone (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 49fd24c5661bbedb7fb839171fa4a835f07e446a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322736"
---
# <a name="id3dx10skininforemovebone-method"></a><span data-ttu-id="92576-103">Metodo ID3DX10SkinInfo:: RemoveBone</span><span class="sxs-lookup"><span data-stu-id="92576-103">ID3DX10SkinInfo::RemoveBone method</span></span>

<span data-ttu-id="92576-104">Rimuovere un osso.</span><span class="sxs-lookup"><span data-stu-id="92576-104">Remove a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="92576-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92576-105">Syntax</span></span>


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="92576-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="92576-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92576-107">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="92576-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92576-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92576-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92576-109">Indice che specifica l'osso da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="92576-109">An index that specifies which bone to remove.</span></span> <span data-ttu-id="92576-110">Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="92576-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92576-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92576-111">Return value</span></span>

<span data-ttu-id="92576-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92576-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92576-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="92576-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="92576-114">Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="92576-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="92576-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92576-115">Requirements</span></span>



| <span data-ttu-id="92576-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="92576-116">Requirement</span></span> | <span data-ttu-id="92576-117">Valore</span><span class="sxs-lookup"><span data-stu-id="92576-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92576-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92576-118">Header</span></span><br/>  | <dl> <span data-ttu-id="92576-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="92576-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="92576-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="92576-120">Library</span></span><br/> | <dl> <span data-ttu-id="92576-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92576-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92576-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92576-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92576-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="92576-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="92576-124">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="92576-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
