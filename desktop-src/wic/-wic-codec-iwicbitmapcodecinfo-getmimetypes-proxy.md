---
description: Funzione proxy per il metodo GetMimeTypes.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: Funzione IWICBitmapCodecInfo_GetMimeTypes_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525933"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a><span data-ttu-id="e7401-103">IWICBitmapCodecInfo \_ GetMimeTypes- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="e7401-103">IWICBitmapCodecInfo\_GetMimeTypes\_Proxy function</span></span>

<span data-ttu-id="e7401-104">Funzione proxy per il metodo [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) .</span><span class="sxs-lookup"><span data-stu-id="e7401-104">Proxy function for the [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7401-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7401-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="e7401-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7401-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7401-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7401-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7401-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="e7401-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="e7401-109">Puntatore a questo oggetto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="e7401-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="e7401-110">*cchMimeTypes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7401-110">*cchMimeTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7401-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e7401-111">Type: **UINT**</span></span>

<span data-ttu-id="e7401-112">Dimensioni del buffer dei tipi MIME.</span><span class="sxs-lookup"><span data-stu-id="e7401-112">The size of the mime types buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e7401-113">*wzMimeTypes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e7401-113">*wzMimeTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7401-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="e7401-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="e7401-115">Puntatore che riceve i tipi MIME associati al codec.</span><span class="sxs-lookup"><span data-stu-id="e7401-115">A pointer that receives the mime types associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="e7401-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e7401-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7401-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="e7401-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="e7401-118">Dimensioni effettive del buffer necessarie per recuperare tutti i tipi MIME associati al codec.</span><span class="sxs-lookup"><span data-stu-id="e7401-118">The actual buffer size needed to retrieve all mime types associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7401-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7401-119">Return value</span></span>

<span data-ttu-id="e7401-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e7401-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e7401-121">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e7401-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7401-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7401-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7401-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e7401-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e7401-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7401-124">Requirements</span></span>



| <span data-ttu-id="e7401-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7401-125">Requirement</span></span> | <span data-ttu-id="e7401-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e7401-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7401-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7401-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e7401-128">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7401-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e7401-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7401-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e7401-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7401-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e7401-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e7401-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7401-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7401-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




