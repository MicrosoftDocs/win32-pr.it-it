---
description: Recupera le caratteristiche dei tipi di carattere identificate in una struttura TEXTMETRIC. Questo metodo supporta le impostazioni del compilatore ANSI e Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'Metodo ID3DXFont:: GetTextMetrics (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354764"
---
# <a name="id3dxfontgettextmetrics-method"></a><span data-ttu-id="a470f-104">Metodo ID3DXFont:: GetTextMetrics</span><span class="sxs-lookup"><span data-stu-id="a470f-104">ID3DXFont::GetTextMetrics method</span></span>

<span data-ttu-id="a470f-105">Recupera le caratteristiche dei tipi di carattere identificate in una struttura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="a470f-105">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="a470f-106">Questo metodo supporta le impostazioni del compilatore ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="a470f-106">This method supports ANSI and Unicode compiler settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="a470f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a470f-107">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="a470f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a470f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a470f-109">*pTextMetrics* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a470f-109">*pTextMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a470f-110">Tipo: **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span><span class="sxs-lookup"><span data-stu-id="a470f-110">Type: **[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span></span>

<span data-ttu-id="a470f-111">Puntatore a una struttura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) che contiene le proprietà del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="a470f-111">Pointer to a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure, which contains font properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a470f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a470f-112">Return value</span></span>

<span data-ttu-id="a470f-113">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a470f-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a470f-114">Diverso da zero se la funzione ha esito positivo; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="a470f-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="a470f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a470f-115">Remarks</span></span>

<span data-ttu-id="a470f-116">L'impostazione del compilatore determina anche il tipo di struttura.</span><span class="sxs-lookup"><span data-stu-id="a470f-116">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="a470f-117">Se è definito Unicode, la funzione restituisce una struttura Campo TEXTMETRICW.</span><span class="sxs-lookup"><span data-stu-id="a470f-117">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="a470f-118">In caso contrario, la chiamata di funzione restituisce una struttura TEXTMETRICA.</span><span class="sxs-lookup"><span data-stu-id="a470f-118">Otherwise, the function call returns a TEXTMETRICA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a470f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a470f-119">Requirements</span></span>



| <span data-ttu-id="a470f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a470f-120">Requirement</span></span> | <span data-ttu-id="a470f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a470f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a470f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a470f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a470f-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a470f-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a470f-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="a470f-124">Library</span></span><br/> | <dl> <span data-ttu-id="a470f-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a470f-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a470f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a470f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a470f-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="a470f-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
