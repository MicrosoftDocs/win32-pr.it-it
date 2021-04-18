---
description: Funzione proxy per il metodo DoesSupportAnimation.
ms.assetid: dd7ed856-14b5-4215-96da-8f5db19a7796
title: Funzione IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 443a8ec7871af6161de2efbb6d4f21d65e5ae9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306684"
---
# <a name="iwicbitmapcodecinfo_doessupportanimation_proxy-function"></a><span data-ttu-id="a1e3d-103">IWICBitmapCodecInfo \_ DoesSupportAnimation- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="a1e3d-103">IWICBitmapCodecInfo\_DoesSupportAnimation\_Proxy function</span></span>

<span data-ttu-id="a1e3d-104">Funzione proxy per il metodo [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) .</span><span class="sxs-lookup"><span data-stu-id="a1e3d-104">Proxy function for the [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e3d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1e3d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportAnimation_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportAnimation
);
```



## <a name="parameters"></a><span data-ttu-id="a1e3d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1e3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e3d-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1e3d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e3d-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="a1e3d-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="a1e3d-109">Puntatore a questo oggetto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="a1e3d-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="a1e3d-110">*pfSupportAnimation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1e3d-110">*pfSupportAnimation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e3d-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="a1e3d-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="a1e3d-112">Puntatore che riceve _ *true*\* se il codec supporta immagini con informazioni sull'intervallo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a1e3d-112">A pointer that receives _ *TRUE*\* if the codec supports images with timing information; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e3d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1e3d-113">Return value</span></span>

<span data-ttu-id="a1e3d-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a1e3d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a1e3d-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a1e3d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1e3d-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a1e3d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1e3d-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a1e3d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e3d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1e3d-118">Requirements</span></span>



| <span data-ttu-id="a1e3d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1e3d-119">Requirement</span></span> | <span data-ttu-id="a1e3d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a1e3d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e3d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1e3d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e3d-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1e3d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a1e3d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1e3d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e3d-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1e3d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a1e3d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a1e3d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1e3d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1e3d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




