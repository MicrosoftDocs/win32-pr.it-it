---
description: Funzione proxy per il metodo InitializeFromBitmap.
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: Funzione IWICPalette_InitializeFromBitmap_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf5e119acf1efca948281a02f61d8954f4e08818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319117"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a><span data-ttu-id="2ab64-103">IWICPalette \_ InitializeFromBitmap- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="2ab64-103">IWICPalette\_InitializeFromBitmap\_Proxy function</span></span>

<span data-ttu-id="2ab64-104">Funzione proxy per il metodo [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) .</span><span class="sxs-lookup"><span data-stu-id="2ab64-104">Proxy function for the [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab64-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ab64-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="2ab64-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ab64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ab64-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ab64-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab64-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="2ab64-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="2ab64-109">Puntatore a questo oggetto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="2ab64-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="2ab64-110">*pISurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ab64-110">*pISurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab64-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="2ab64-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="2ab64-112">Puntatore alla bitmap di origine.</span><span class="sxs-lookup"><span data-stu-id="2ab64-112">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2ab64-113">_colorCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ab64-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab64-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2ab64-114">Type: **UINT**</span></span>

<span data-ttu-id="2ab64-115">Il numero di colori con cui inizializzare la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="2ab64-115">The number of colors to initialize the palette with.</span></span>

</dd> <dt>

<span data-ttu-id="2ab64-116">*fAddTransparentColor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ab64-116">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab64-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="2ab64-117">Type: **BOOL**</span></span>

<span data-ttu-id="2ab64-118">Valore che indica se aggiungere un colore trasparente.</span><span class="sxs-lookup"><span data-stu-id="2ab64-118">A value to indicate whether to add a transparent color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ab64-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ab64-119">Return value</span></span>

<span data-ttu-id="2ab64-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2ab64-120">Type: **HRESULT**</span></span>

<span data-ttu-id="2ab64-121">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2ab64-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2ab64-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ab64-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab64-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="2ab64-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab64-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ab64-124">Requirements</span></span>



| <span data-ttu-id="2ab64-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ab64-125">Requirement</span></span> | <span data-ttu-id="2ab64-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2ab64-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab64-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ab64-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2ab64-128">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ab64-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2ab64-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ab64-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2ab64-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2ab64-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2ab64-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2ab64-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ab64-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ab64-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




