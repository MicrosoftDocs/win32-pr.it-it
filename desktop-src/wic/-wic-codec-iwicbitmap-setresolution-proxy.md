---
description: IWICBitmap_SetResolution_Proxy funzione proxy per il metodo SetResolution.
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: IWICBitmap_SetResolution_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f11189307ad14dde6ea1e1373583a8ab4b08b9be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086379"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="d9bfc-103">Funzione proxy IWICBitmap \_ SetResolution \_</span><span class="sxs-lookup"><span data-stu-id="d9bfc-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="d9bfc-104">Funzione proxy per il [**metodo SetResolution.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution)</span><span class="sxs-lookup"><span data-stu-id="d9bfc-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bfc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9bfc-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="d9bfc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9bfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9bfc-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9bfc-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bfc-108">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="d9bfc-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="d9bfc-109">Puntatore a [**questo oggetto IWICBitmap.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)</span><span class="sxs-lookup"><span data-stu-id="d9bfc-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="d9bfc-110">*dpiX* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d9bfc-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bfc-111">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="d9bfc-111">Type: **double**</span></span>

<span data-ttu-id="d9bfc-112">Risoluzione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="d9bfc-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="d9bfc-113">*dpiY* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d9bfc-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bfc-114">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="d9bfc-114">Type: **double**</span></span>

<span data-ttu-id="d9bfc-115">Risoluzione verticale.</span><span class="sxs-lookup"><span data-stu-id="d9bfc-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9bfc-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9bfc-116">Return value</span></span>

<span data-ttu-id="d9bfc-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d9bfc-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d9bfc-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d9bfc-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9bfc-119">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d9bfc-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9bfc-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d9bfc-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d9bfc-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9bfc-121">Requirements</span></span>



| <span data-ttu-id="d9bfc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9bfc-122">Requirement</span></span> | <span data-ttu-id="d9bfc-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d9bfc-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bfc-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9bfc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d9bfc-125">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9bfc-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d9bfc-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9bfc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d9bfc-127">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9bfc-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d9bfc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d9bfc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9bfc-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9bfc-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




