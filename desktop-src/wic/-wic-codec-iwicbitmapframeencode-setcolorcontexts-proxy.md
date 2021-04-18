---
description: Funzione proxy per il metodo SetColorContexts.
ms.assetid: 985ae179-df59-42a0-9987-5dd863512e57
title: Funzione IWICBitmapFrameEncode_SetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8a960873340c15772113a3f1553a9b6e16c44338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306665"
---
# <a name="iwicbitmapframeencode_setcolorcontexts_proxy-function"></a><span data-ttu-id="bba6e-103">IWICBitmapFrameEncode \_ SetColorContexts- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="bba6e-103">IWICBitmapFrameEncode\_SetColorContexts\_Proxy function</span></span>

<span data-ttu-id="bba6e-104">Funzione proxy per il metodo [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="bba6e-104">Proxy function for the [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba6e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bba6e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetColorContexts_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  cCount,
  _In_ IWICColorContext      **ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="bba6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bba6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba6e-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bba6e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba6e-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="bba6e-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="bba6e-109">Puntatore a questo oggetto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="bba6e-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="bba6e-110">*ccount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bba6e-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba6e-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="bba6e-111">Type: **UINT**</span></span>

<span data-ttu-id="bba6e-112">Numero di profili [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) da impostare.</span><span class="sxs-lookup"><span data-stu-id="bba6e-112">The number of [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) profiles to set.</span></span>

</dd> <dt>

<span data-ttu-id="bba6e-113">*ppIColorContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bba6e-113">*ppIColorContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba6e-114">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="bba6e-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="bba6e-115">Puntatore a un puntatore [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) contenente i profili dei contesti di colore da impostare sul frame.</span><span class="sxs-lookup"><span data-stu-id="bba6e-115">A pointer to an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) pointer containing the color contexts profiles to set to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba6e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bba6e-116">Return value</span></span>

<span data-ttu-id="bba6e-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bba6e-117">Type: **HRESULT**</span></span>

<span data-ttu-id="bba6e-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bba6e-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bba6e-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bba6e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bba6e-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bba6e-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bba6e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bba6e-121">Requirements</span></span>



| <span data-ttu-id="bba6e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba6e-122">Requirement</span></span> | <span data-ttu-id="bba6e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bba6e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba6e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bba6e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bba6e-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bba6e-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bba6e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bba6e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bba6e-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bba6e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bba6e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bba6e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bba6e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bba6e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




