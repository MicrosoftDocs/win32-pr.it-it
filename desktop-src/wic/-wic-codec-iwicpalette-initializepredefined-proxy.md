---
description: Funzione proxy per il metodo InitializePredefined.
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: Funzione IWICPalette_InitializePredefined_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d65202d9d7800763e15f52ef0eb03b16bc348e78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758849"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a><span data-ttu-id="f826d-103">IWICPalette \_ InitializePredefined- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="f826d-103">IWICPalette\_InitializePredefined\_Proxy function</span></span>

<span data-ttu-id="f826d-104">Funzione proxy per il metodo [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) .</span><span class="sxs-lookup"><span data-stu-id="f826d-104">Proxy function for the [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f826d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f826d-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="f826d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f826d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f826d-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f826d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f826d-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="f826d-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="f826d-109">Puntatore a questo oggetto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="f826d-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="f826d-110">*ePaletteType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f826d-110">*ePaletteType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f826d-111">Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="f826d-111">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="f826d-112">Tipo di tavolozza predefinito desiderato.</span><span class="sxs-lookup"><span data-stu-id="f826d-112">The desired pre-defined palette type.</span></span>

</dd> <dt>

<span data-ttu-id="f826d-113">*fAddTransparentColor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f826d-113">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f826d-114">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="f826d-114">Type: **BOOL**</span></span>

<span data-ttu-id="f826d-115">Colore facoltativo di tranparent da aggiungere alla tavolozza.</span><span class="sxs-lookup"><span data-stu-id="f826d-115">The optional tranparent color to add to the palette.</span></span> <span data-ttu-id="f826d-116">Se non è necessario alcun colore trasparente, utilizzare 0.</span><span class="sxs-lookup"><span data-stu-id="f826d-116">If no transparent color is needed, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f826d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f826d-117">Return value</span></span>

<span data-ttu-id="f826d-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f826d-118">Type: **HRESULT**</span></span>

<span data-ttu-id="f826d-119">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f826d-119">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f826d-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f826d-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f826d-121">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f826d-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f826d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f826d-122">Requirements</span></span>



| <span data-ttu-id="f826d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f826d-123">Requirement</span></span> | <span data-ttu-id="f826d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f826d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f826d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f826d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f826d-126">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f826d-126">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f826d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f826d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f826d-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f826d-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f826d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f826d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f826d-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f826d-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




