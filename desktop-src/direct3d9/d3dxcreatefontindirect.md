---
description: Crea indirettamente un oggetto del tipo di carattere per un dispositivo e un tipo di carattere.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: Funzione D3DXCreateFontIndirect (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355459"
---
# <a name="d3dxcreatefontindirect-function"></a><span data-ttu-id="0ee3b-103">D3DXCreateFontIndirect (funzione)</span><span class="sxs-lookup"><span data-stu-id="0ee3b-103">D3DXCreateFontIndirect function</span></span>

<span data-ttu-id="0ee3b-104">Crea indirettamente un oggetto del tipo di carattere per un dispositivo e un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-104">Creates a font object indirectly for both a device and a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee3b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ee3b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="0ee3b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ee3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee3b-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ee3b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee3b-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0ee3b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0ee3b-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , il dispositivo da associare all'oggetto del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="0ee3b-110">*pDesc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ee3b-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee3b-111">Tipo: **const [**D3DXFONT \_ desc**](d3dxfont-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="0ee3b-111">Type: **const [**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="0ee3b-112">Puntatore a una struttura [**D3DXFONT \_ desc**](d3dxfont-desc.md) , che descrive gli attributi dell'oggetto Font da creare.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-112">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="0ee3b-113">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati D3DXFONT \_ desc viene risolto in D3DXFONT \_ DESCW; in caso contrario, il tipo di dati viene risolto in D3DXFONT \_ Desca.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-113">If the compiler settings require Unicode, the data type D3DXFONT\_DESC resolves to D3DXFONT\_DESCW; otherwise, the data type resolves to D3DXFONT\_DESCA.</span></span> <span data-ttu-id="0ee3b-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0ee3b-115">*ppFont* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0ee3b-115">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee3b-116">Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ee3b-116">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="0ee3b-117">Restituisce un puntatore a un'interfaccia [**ID3DXFont**](id3dxfont.md) , che rappresenta l'oggetto del tipo di carattere creato.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-117">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee3b-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ee3b-118">Return value</span></span>

<span data-ttu-id="0ee3b-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ee3b-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ee3b-120">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ee3b-121">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee3b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ee3b-122">Remarks</span></span>

<span data-ttu-id="0ee3b-123">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-123">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0ee3b-124">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-124">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="0ee3b-125">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateFontIndirectA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="0ee3b-125">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee3b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ee3b-126">Requirements</span></span>



| <span data-ttu-id="0ee3b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ee3b-127">Requirement</span></span> | <span data-ttu-id="0ee3b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0ee3b-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee3b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ee3b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0ee3b-130"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ee3b-130"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0ee3b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ee3b-131">Library</span></span><br/> | <dl> <span data-ttu-id="0ee3b-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ee3b-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0ee3b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ee3b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee3b-134">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="0ee3b-134">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
