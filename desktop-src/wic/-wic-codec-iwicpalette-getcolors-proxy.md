---
description: Funzione proxy per il metodo getcolors.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: Funzione IWICPalette_GetColors_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232475"
---
# <a name="iwicpalette_getcolors_proxy-function"></a><span data-ttu-id="cc5de-103">\_Funzione proxy IWICPalette Getcolors \_</span><span class="sxs-lookup"><span data-stu-id="cc5de-103">IWICPalette\_GetColors\_Proxy function</span></span>

<span data-ttu-id="cc5de-104">Funzione proxy per il metodo [**Getcolors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) .</span><span class="sxs-lookup"><span data-stu-id="cc5de-104">Proxy function for the [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc5de-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc5de-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a><span data-ttu-id="cc5de-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc5de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc5de-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc5de-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5de-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="cc5de-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="cc5de-109">Puntatore a questo oggetto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="cc5de-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="cc5de-110">*colorCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc5de-110">*colorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5de-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="cc5de-111">Type: **UINT**</span></span>

<span data-ttu-id="cc5de-112">Dimensioni della matrice *pColors* .</span><span class="sxs-lookup"><span data-stu-id="cc5de-112">The size of the *pColors* array.</span></span>

</dd> <dt>

<span data-ttu-id="cc5de-113">*pColors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc5de-113">*pColors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5de-114">Tipo: \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="cc5de-114">Type: \**WICColor\** _</span></span>

<span data-ttu-id="cc5de-115">Puntatore che riceve i colori della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="cc5de-115">Pointer that receives the colors of the palette.</span></span>

</dd> <dt>

<span data-ttu-id="cc5de-116">_pcActualColors \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc5de-116">_pcActualColors\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5de-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="cc5de-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="cc5de-118">Dimensioni effettive necessarie per ottenere i colori della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="cc5de-118">The actual size needed to obtain the palette colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc5de-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc5de-119">Return value</span></span>

<span data-ttu-id="cc5de-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="cc5de-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="cc5de-121">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc5de-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc5de-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc5de-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc5de-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="cc5de-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cc5de-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc5de-124">Requirements</span></span>



| <span data-ttu-id="cc5de-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc5de-125">Requirement</span></span> | <span data-ttu-id="cc5de-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cc5de-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc5de-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc5de-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cc5de-128">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc5de-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cc5de-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc5de-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cc5de-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc5de-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cc5de-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cc5de-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc5de-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc5de-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




