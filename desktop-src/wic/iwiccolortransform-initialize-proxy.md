---
description: Inizializza un IWICColorTransform con un IWICBitmapSource e lo trasforma da un IWICColorContext a un altro.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: Funzione IWICColorTransform_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327269"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a><span data-ttu-id="aad6e-103">IWICColorTransform \_ Inizializza la \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="aad6e-103">IWICColorTransform\_Initialize\_Proxy function</span></span>

<span data-ttu-id="aad6e-104">Inizializza un [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) con un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) e lo trasforma da un [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) a un altro.</span><span class="sxs-lookup"><span data-stu-id="aad6e-104">Initializes an [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) with a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) and transforms it from one [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad6e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aad6e-105">Syntax</span></span>


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a><span data-ttu-id="aad6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aad6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aad6e-107">*pIColorTransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aad6e-107">*pIColorTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad6e-108">Tipo: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span><span class="sxs-lookup"><span data-stu-id="aad6e-108">Type: **[**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span></span>

<span data-ttu-id="aad6e-109">Trasformazione colore da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="aad6e-109">The color transform to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="aad6e-110">*pIBitmapSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aad6e-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad6e-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="aad6e-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="aad6e-112">Origine della bitmap utilizzata per inizializzare la trasformazione colore.</span><span class="sxs-lookup"><span data-stu-id="aad6e-112">The bitmap source used to initialize the color transform.</span></span>

</dd> <dt>

<span data-ttu-id="aad6e-113">*pIContextSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aad6e-113">*pIContextSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad6e-114">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="aad6e-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="aad6e-115">Origine del contesto del colore.</span><span class="sxs-lookup"><span data-stu-id="aad6e-115">The color context source.</span></span>

</dd> <dt>

<span data-ttu-id="aad6e-116">*pIContextDest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aad6e-116">*pIContextDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad6e-117">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="aad6e-117">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="aad6e-118">Destinazione del contesto del colore.</span><span class="sxs-lookup"><span data-stu-id="aad6e-118">The color context destination.</span></span>

</dd> <dt>

<span data-ttu-id="aad6e-119">*pixelFmtDest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aad6e-119">*pixelFmtDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad6e-120">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="aad6e-120">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="aad6e-121">GUID del formato pixel desiderato.</span><span class="sxs-lookup"><span data-stu-id="aad6e-121">The GUID of the desired pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aad6e-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aad6e-122">Return value</span></span>

<span data-ttu-id="aad6e-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aad6e-123">Type: **HRESULT**</span></span>

<span data-ttu-id="aad6e-124">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aad6e-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aad6e-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aad6e-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aad6e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aad6e-126">Requirements</span></span>



| <span data-ttu-id="aad6e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="aad6e-127">Requirement</span></span> | <span data-ttu-id="aad6e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="aad6e-128">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aad6e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="aad6e-129">DLL</span></span><br/> | <dl> <span data-ttu-id="aad6e-130"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aad6e-130"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 




