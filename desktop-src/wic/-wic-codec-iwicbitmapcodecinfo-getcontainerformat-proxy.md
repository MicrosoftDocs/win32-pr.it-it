---
description: Funzione proxy per il metodo GetContainerFormat.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: Funzione IWICBitmapCodecInfo_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 896c2ff88085c0300cffcc56c2877b98cd4ab68a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226042"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="db287-103">IWICBitmapCodecInfo \_ GetContainerFormat- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="db287-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="db287-104">Funzione proxy per il metodo [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="db287-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="db287-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db287-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="db287-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db287-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db287-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db287-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="db287-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="db287-109">Puntatore a questo oggetto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="db287-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="db287-110">*pguidContainerFormat* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="db287-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db287-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="db287-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="db287-112">Puntatore che riceve il GUID del contenitore.</span><span class="sxs-lookup"><span data-stu-id="db287-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db287-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db287-113">Return value</span></span>

<span data-ttu-id="db287-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="db287-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="db287-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="db287-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db287-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db287-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="db287-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="db287-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="db287-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db287-118">Requirements</span></span>



| <span data-ttu-id="db287-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="db287-119">Requirement</span></span> | <span data-ttu-id="db287-120">Valore</span><span class="sxs-lookup"><span data-stu-id="db287-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db287-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db287-121">Minimum supported client</span></span><br/> | <span data-ttu-id="db287-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db287-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="db287-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db287-123">Minimum supported server</span></span><br/> | <span data-ttu-id="db287-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db287-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="db287-125">DLL</span><span class="sxs-lookup"><span data-stu-id="db287-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db287-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db287-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




