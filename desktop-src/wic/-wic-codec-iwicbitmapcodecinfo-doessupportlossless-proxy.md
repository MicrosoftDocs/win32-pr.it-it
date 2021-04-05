---
description: Funzione proxy per il metodo DoesSupportLossless.
ms.assetid: c88d7971-cc93-458c-a31e-19a8b8350d09
title: Funzione IWICBitmapCodecInfo_DoesSupportLossless_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportLossless_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f498af72391aa0a7745ed79d06c6e1d55317393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751247"
---
# <a name="iwicbitmapcodecinfo_doessupportlossless_proxy-function"></a><span data-ttu-id="8997c-103">IWICBitmapCodecInfo \_ DoesSupportLossless- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="8997c-103">IWICBitmapCodecInfo\_DoesSupportLossless\_Proxy function</span></span>

<span data-ttu-id="8997c-104">Funzione proxy per il metodo [**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) .</span><span class="sxs-lookup"><span data-stu-id="8997c-104">Proxy function for the [**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8997c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8997c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportLossless_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportLossless
);
```



## <a name="parameters"></a><span data-ttu-id="8997c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8997c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8997c-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8997c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8997c-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="8997c-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="8997c-109">Puntatore a questo oggetto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="8997c-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="8997c-110">*pfSupportLossless* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8997c-110">*pfSupportLossless* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8997c-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="8997c-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="8997c-112">Puntatore che riceve _ *true*\* se il codec supporta i formati lossless; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8997c-112">A pointer that receives _ *TRUE*\* if the codec supports lossless formats; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8997c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8997c-113">Return value</span></span>

<span data-ttu-id="8997c-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8997c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8997c-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8997c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8997c-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8997c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8997c-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8997c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8997c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8997c-118">Requirements</span></span>



| <span data-ttu-id="8997c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8997c-119">Requirement</span></span> | <span data-ttu-id="8997c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8997c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8997c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8997c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8997c-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8997c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8997c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8997c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8997c-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8997c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8997c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8997c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8997c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8997c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




