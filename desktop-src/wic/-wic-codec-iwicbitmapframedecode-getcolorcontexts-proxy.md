---
description: IWICBitmapFrameDecode_GetColorContexts_Proxy funzione proxy per il metodo GetColorContexts.
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: IWICBitmapFrameDecode_GetColorContexts_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 99fb6caa9b9e654be0adc1235cad0e79a7fa1ef3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100579"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="1cc80-103">Funzione proxy IWICBitmapFrameDecode \_ GetColorContexts \_</span><span class="sxs-lookup"><span data-stu-id="1cc80-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="1cc80-104">Funzione proxy per il [**metodo GetColorContexts.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)</span><span class="sxs-lookup"><span data-stu-id="1cc80-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc80-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cc80-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="1cc80-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cc80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc80-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cc80-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc80-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="1cc80-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="1cc80-109">Puntatore a [**questo oggetto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="1cc80-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="1cc80-110">*cCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1cc80-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc80-111">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="1cc80-111">Type: **UINT**</span></span>

<span data-ttu-id="1cc80-112">Numero di contesti di colore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="1cc80-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="1cc80-113">Questo valore deve essere delle dimensioni di o inferiori alle dimensioni disponibili per *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="1cc80-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="1cc80-114">*ppIColorContexts* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1cc80-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc80-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="1cc80-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="1cc80-116">Puntatore che riceve un puntatore agli [**oggetti IWICColorContext.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)</span><span class="sxs-lookup"><span data-stu-id="1cc80-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="1cc80-117">*pcActualCount* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1cc80-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc80-118">Tipo: **UINT \***</span><span class="sxs-lookup"><span data-stu-id="1cc80-118">Type: **UINT\***</span></span>

<span data-ttu-id="1cc80-119">Puntatore che riceve il numero di contesti di colore contenuti nella cornice dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1cc80-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc80-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cc80-120">Return value</span></span>

<span data-ttu-id="1cc80-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1cc80-121">Type: **HRESULT**</span></span>

<span data-ttu-id="1cc80-122">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1cc80-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1cc80-123">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1cc80-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc80-124">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="1cc80-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc80-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cc80-125">Requirements</span></span>



| <span data-ttu-id="1cc80-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc80-126">Requirement</span></span> | <span data-ttu-id="1cc80-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1cc80-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc80-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cc80-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc80-129">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1cc80-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1cc80-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cc80-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc80-131">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cc80-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1cc80-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1cc80-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cc80-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cc80-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




