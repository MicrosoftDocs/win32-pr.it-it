---
description: Funzione proxy per il metodo GetEncoderInfo.
ms.assetid: 759965fd-7bc6-4130-b102-b49d1f0d4bf8
title: Funzione IWICBitmapEncoder_GetEncoderInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetEncoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 00764021542648c42fa9bf8213e799edb8b8fd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319569"
---
# <a name="iwicbitmapencoder_getencoderinfo_proxy-function"></a><span data-ttu-id="e3f42-103">IWICBitmapEncoder \_ GetEncoderInfo- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="e3f42-103">IWICBitmapEncoder\_GetEncoderInfo\_Proxy function</span></span>

<span data-ttu-id="e3f42-104">Funzione proxy per il metodo [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3f42-104">Proxy function for the [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f42-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3f42-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetEncoderInfo_Proxy(
  _In_  IWICBitmapEncoder     *THIS_PTR,
  _Out_ IWICBitmapEncoderInfo **ppIEncoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e3f42-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3f42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f42-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3f42-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f42-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="e3f42-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="e3f42-109">Puntatore a questo oggetto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="e3f42-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="e3f42-110">*ppIEncoderInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e3f42-110">*ppIEncoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f42-111">Tipo: **[ **IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="e3f42-111">Type: **[**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span></span>

<span data-ttu-id="e3f42-112">Puntatore che riceve un puntatore a un [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span><span class="sxs-lookup"><span data-stu-id="e3f42-112">A pointer that receives a pointer to an [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f42-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3f42-113">Return value</span></span>

<span data-ttu-id="e3f42-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e3f42-114">Type: **HRESULT**</span></span>

<span data-ttu-id="e3f42-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3f42-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3f42-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3f42-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f42-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e3f42-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f42-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3f42-118">Requirements</span></span>



| <span data-ttu-id="e3f42-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3f42-119">Requirement</span></span> | <span data-ttu-id="e3f42-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e3f42-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f42-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3f42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f42-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3f42-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e3f42-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3f42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f42-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3f42-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e3f42-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e3f42-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3f42-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3f42-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




