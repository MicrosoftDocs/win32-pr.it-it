---
description: Funzione proxy per il metodo DoesSupportMultiframe.
ms.assetid: ceee0090-ff23-4eb4-b0ea-de1d12bceef8
title: Funzione IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d148127345e77da027191114f7e411bdae564deb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128966"
---
# <a name="iwicbitmapcodecinfo_doessupportmultiframe_proxy-function"></a><span data-ttu-id="0f417-103">IWICBitmapCodecInfo \_ DoesSupportMultiframe- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="0f417-103">IWICBitmapCodecInfo\_DoesSupportMultiframe\_Proxy function</span></span>

<span data-ttu-id="0f417-104">Funzione proxy per il metodo [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) .</span><span class="sxs-lookup"><span data-stu-id="0f417-104">Proxy function for the [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f417-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f417-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportMultiframe
);
```



## <a name="parameters"></a><span data-ttu-id="0f417-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f417-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f417-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f417-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f417-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="0f417-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="0f417-109">Puntatore a questo oggetto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="0f417-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="0f417-110">*pfSupportMultiframe* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0f417-110">*pfSupportMultiframe* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f417-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="0f417-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="0f417-112">Puntatore che riceve _ *true*\* se il codec supporta immagini multiframe; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0f417-112">A pointer that receives _ *TRUE*\* if the codec supports multi frame images; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f417-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f417-113">Return value</span></span>

<span data-ttu-id="0f417-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0f417-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0f417-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0f417-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f417-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f417-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f417-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="0f417-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0f417-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f417-118">Requirements</span></span>



| <span data-ttu-id="0f417-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f417-119">Requirement</span></span> | <span data-ttu-id="0f417-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0f417-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f417-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f417-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f417-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f417-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0f417-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f417-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f417-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f417-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0f417-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0f417-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f417-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f417-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




