---
description: IWICBitmapScaler_Initialize_Proxy funzione proxy per il metodo Initialize.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy funzione
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
ms.openlocfilehash: 76b7c754273f4d55fbf3de9d8ba592806e590aac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100539"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="7cd22-103">Funzione proxy di inizializzazione IWICBitmapScaler \_ \_</span><span class="sxs-lookup"><span data-stu-id="7cd22-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="7cd22-104">Funzione proxy per il [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize)</span><span class="sxs-lookup"><span data-stu-id="7cd22-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd22-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cd22-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="7cd22-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cd22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd22-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd22-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd22-108">Tipo: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span><span class="sxs-lookup"><span data-stu-id="7cd22-108">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span></span>

<span data-ttu-id="7cd22-109">Puntatore a [**questo oggetto IWICBitmapScaler.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)</span><span class="sxs-lookup"><span data-stu-id="7cd22-109">Pointer to this [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="7cd22-110">*pISource* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7cd22-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd22-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="7cd22-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="7cd22-112">Origine bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="7cd22-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="7cd22-113">*uiWidth* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7cd22-113">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd22-114">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="7cd22-114">Type: **UINT**</span></span>

<span data-ttu-id="7cd22-115">Larghezza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7cd22-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="7cd22-116">*uiHeight* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7cd22-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd22-117">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="7cd22-117">Type: **UINT**</span></span>

<span data-ttu-id="7cd22-118">Altezza di desination.</span><span class="sxs-lookup"><span data-stu-id="7cd22-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="7cd22-119">*modalità* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7cd22-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd22-120">Tipo: **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="7cd22-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="7cd22-121">Modalità di interpolazione da utilizzare per il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="7cd22-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd22-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cd22-122">Return value</span></span>

<span data-ttu-id="7cd22-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7cd22-123">Type: **HRESULT**</span></span>

<span data-ttu-id="7cd22-124">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7cd22-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7cd22-125">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="7cd22-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd22-126">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7cd22-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd22-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cd22-127">Requirements</span></span>



| <span data-ttu-id="7cd22-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cd22-128">Requirement</span></span> | <span data-ttu-id="7cd22-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7cd22-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd22-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cd22-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd22-131">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7cd22-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7cd22-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cd22-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd22-133">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7cd22-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7cd22-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd22-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cd22-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cd22-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




