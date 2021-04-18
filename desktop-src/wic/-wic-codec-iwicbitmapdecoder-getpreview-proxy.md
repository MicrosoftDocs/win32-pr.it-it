---
description: Funzione proxy per il metodo getpreview.
ms.assetid: 8251af14-68db-4e4a-a501-115e7bbd53cd
title: Funzione IWICBitmapDecoder_GetPreview_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetPreview_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc6808d94cdc1cdcdaf65e252107b939e12eeaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306673"
---
# <a name="iwicbitmapdecoder_getpreview_proxy-function"></a><span data-ttu-id="8004a-103">\_Funzione proxy IWICBitmapDecoder Getpreview \_</span><span class="sxs-lookup"><span data-stu-id="8004a-103">IWICBitmapDecoder\_GetPreview\_Proxy function</span></span>

<span data-ttu-id="8004a-104">Funzione proxy per il metodo [**getpreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="8004a-104">Proxy function for the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8004a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8004a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetPreview_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIBitmapSource
);
```



## <a name="parameters"></a><span data-ttu-id="8004a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8004a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8004a-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8004a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8004a-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="8004a-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="8004a-109">Puntatore a questo oggetto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="8004a-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="8004a-110">*ppIBitmapSource* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8004a-110">*ppIBitmapSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8004a-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="8004a-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="8004a-112">Puntatore che riceve un puntatore alla bitmap di anteprima se supportata.</span><span class="sxs-lookup"><span data-stu-id="8004a-112">A pointer that receives a pointer to the preview bitmap if supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8004a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8004a-113">Return value</span></span>

<span data-ttu-id="8004a-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8004a-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8004a-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8004a-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8004a-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8004a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8004a-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8004a-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8004a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8004a-118">Requirements</span></span>



| <span data-ttu-id="8004a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8004a-119">Requirement</span></span> | <span data-ttu-id="8004a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8004a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8004a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8004a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8004a-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8004a-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8004a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8004a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8004a-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8004a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8004a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8004a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8004a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8004a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




