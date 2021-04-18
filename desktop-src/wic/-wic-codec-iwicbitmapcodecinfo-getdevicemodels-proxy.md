---
description: Funzione proxy per il metodo GetDeviceModels.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: Funzione IWICBitmapCodecInfo_GetDeviceModels_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306679"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a><span data-ttu-id="f6c0a-103">IWICBitmapCodecInfo \_ GetDeviceModels- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="f6c0a-103">IWICBitmapCodecInfo\_GetDeviceModels\_Proxy function</span></span>

<span data-ttu-id="f6c0a-104">Funzione proxy per il metodo [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) .</span><span class="sxs-lookup"><span data-stu-id="f6c0a-104">Proxy function for the [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c0a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6c0a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="f6c0a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6c0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c0a-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6c0a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c0a-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="f6c0a-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="f6c0a-109">Puntatore a questo oggetto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="f6c0a-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="f6c0a-110">*cchDeviceModels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6c0a-110">*cchDeviceModels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c0a-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f6c0a-111">Type: **UINT**</span></span>

<span data-ttu-id="f6c0a-112">Dimensioni del buffer dei modelli di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6c0a-112">The size of the device models buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f6c0a-113">*wzDeviceModels* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f6c0a-113">*wzDeviceModels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c0a-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="f6c0a-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="f6c0a-115">Puntatore che riceve un elenco delimitato da virgole di nomi di modelli di dispositivo associati al codec.</span><span class="sxs-lookup"><span data-stu-id="f6c0a-115">A pointer that receives a comma delimited list of device model names associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="f6c0a-116">_pcchActual \* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f6c0a-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c0a-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="f6c0a-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="f6c0a-118">Dimensioni effettive del buffer necessarie per recuperare tutti i nomi dei modelli di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6c0a-118">The actual buffer size needed to retrieve all of the device model names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c0a-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6c0a-119">Return value</span></span>

<span data-ttu-id="f6c0a-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f6c0a-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f6c0a-121">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f6c0a-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6c0a-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6c0a-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6c0a-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f6c0a-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c0a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6c0a-124">Requirements</span></span>



| <span data-ttu-id="f6c0a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6c0a-125">Requirement</span></span> | <span data-ttu-id="f6c0a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f6c0a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c0a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6c0a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c0a-128">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6c0a-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f6c0a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6c0a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c0a-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6c0a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f6c0a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f6c0a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6c0a-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6c0a-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




