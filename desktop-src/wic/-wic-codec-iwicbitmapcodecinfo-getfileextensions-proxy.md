---
description: Funzione proxy per il metodo GetFileExtensions.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: Funzione IWICBitmapCodecInfo_GetFileExtensions_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343231"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a><span data-ttu-id="30ee9-103">IWICBitmapCodecInfo \_ GetFileExtensions- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="30ee9-103">IWICBitmapCodecInfo\_GetFileExtensions\_Proxy function</span></span>

<span data-ttu-id="30ee9-104">Funzione proxy per il metodo [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) .</span><span class="sxs-lookup"><span data-stu-id="30ee9-104">Proxy function for the [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ee9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30ee9-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="30ee9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="30ee9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ee9-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30ee9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ee9-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="30ee9-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="30ee9-109">Puntatore a questo oggetto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="30ee9-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="30ee9-110">*cchFileExtensions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30ee9-110">*cchFileExtensions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ee9-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="30ee9-111">Type: **UINT**</span></span>

<span data-ttu-id="30ee9-112">Dimensioni del buffer dell'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="30ee9-112">The size of the file name extension buffer.</span></span>

</dd> <dt>

<span data-ttu-id="30ee9-113">*wzFileExtensions* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="30ee9-113">*wzFileExtensions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30ee9-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="30ee9-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="30ee9-115">Puntatore che riceve le estensioni dei nomi di file associate al codec.</span><span class="sxs-lookup"><span data-stu-id="30ee9-115">A pointer that receives the file name extensions associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="30ee9-116">_pcchActual \* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="30ee9-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30ee9-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="30ee9-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="30ee9-118">Dimensioni effettive del buffer necessarie per recuperare tutte le estensioni dei nomi di file associate al codec.</span><span class="sxs-lookup"><span data-stu-id="30ee9-118">The actual buffer size needed to retrieve all file name extensions associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ee9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30ee9-119">Return value</span></span>

<span data-ttu-id="30ee9-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="30ee9-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="30ee9-121">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="30ee9-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30ee9-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30ee9-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30ee9-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="30ee9-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="30ee9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30ee9-124">Requirements</span></span>



| <span data-ttu-id="30ee9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="30ee9-125">Requirement</span></span> | <span data-ttu-id="30ee9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="30ee9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ee9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30ee9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="30ee9-128">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30ee9-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="30ee9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30ee9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="30ee9-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30ee9-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="30ee9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="30ee9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30ee9-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30ee9-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




