---
description: Funzione proxy per il metodo GetChannelCount.
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: Funzione IWICPixelFormatInfo_GetChannelCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6bf3f0d8aaf6cf95633fa4cce771bd7c7e8db85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319557"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a><span data-ttu-id="d6c78-103">IWICPixelFormatInfo \_ GetChannelCount- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="d6c78-103">IWICPixelFormatInfo\_GetChannelCount\_Proxy function</span></span>

<span data-ttu-id="d6c78-104">Funzione proxy per il metodo [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) .</span><span class="sxs-lookup"><span data-stu-id="d6c78-104">Proxy function for the [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c78-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6c78-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a><span data-ttu-id="d6c78-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6c78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c78-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6c78-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c78-108">Tipo: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="d6c78-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="d6c78-109">Puntatore a questo oggetto [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="d6c78-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="d6c78-110">*puiChannelCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d6c78-110">*puiChannelCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c78-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="d6c78-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="d6c78-112">Puntatore che riceve il numero di canali.</span><span class="sxs-lookup"><span data-stu-id="d6c78-112">Pointer that receives the channel count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c78-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6c78-113">Return value</span></span>

<span data-ttu-id="d6c78-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d6c78-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d6c78-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d6c78-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6c78-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6c78-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6c78-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d6c78-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c78-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6c78-118">Requirements</span></span>



| <span data-ttu-id="d6c78-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c78-119">Requirement</span></span> | <span data-ttu-id="d6c78-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d6c78-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c78-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6c78-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c78-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6c78-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d6c78-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6c78-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c78-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6c78-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d6c78-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d6c78-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6c78-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6c78-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




