---
description: Funzione proxy per il metodo Initialize.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: Funzione IWICBitmapScaler_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cc317adc831b0cf0759580d5c6924fb3f0997524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319564"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="2678a-103">IWICBitmapScaler \_ Inizializza la \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="2678a-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="2678a-104">Funzione proxy per il metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="2678a-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2678a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2678a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="2678a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2678a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2678a-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2678a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2678a-108">Tipo: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) \** _</span><span class="sxs-lookup"><span data-stu-id="2678a-108">Type: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\** _</span></span>

<span data-ttu-id="2678a-109">Puntatore a questo oggetto [_ *IWICBitmapScaler* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="2678a-109">Pointer to this [_ *IWICBitmapScaler*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="2678a-110">*pISource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2678a-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2678a-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="2678a-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="2678a-112">Origine della bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="2678a-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="2678a-113">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2678a-113">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2678a-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2678a-114">Type: **UINT**</span></span>

<span data-ttu-id="2678a-115">Larghezza della destinazione.</span><span class="sxs-lookup"><span data-stu-id="2678a-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="2678a-116">*uiHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2678a-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2678a-117">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2678a-117">Type: **UINT**</span></span>

<span data-ttu-id="2678a-118">Altezza delle destinazioni.</span><span class="sxs-lookup"><span data-stu-id="2678a-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="2678a-119">*modalità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2678a-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2678a-120">Tipo: **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="2678a-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="2678a-121">Modalità di interpolazione da utilizzare per il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="2678a-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2678a-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2678a-122">Return value</span></span>

<span data-ttu-id="2678a-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2678a-123">Type: **HRESULT**</span></span>

<span data-ttu-id="2678a-124">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2678a-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2678a-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2678a-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2678a-126">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="2678a-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2678a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2678a-127">Requirements</span></span>



| <span data-ttu-id="2678a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2678a-128">Requirement</span></span> | <span data-ttu-id="2678a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2678a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2678a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2678a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2678a-131">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2678a-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2678a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2678a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2678a-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2678a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2678a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2678a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2678a-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2678a-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




