---
description: Funzione proxy per il metodo CopyPalette.
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: Funzione IWICBitmapDecoder_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee6902668a9c4feffdcc696ce0d5f6214a707bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306678"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="6599f-103">IWICBitmapDecoder \_ CopyPalette- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="6599f-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="6599f-104">Funzione proxy per il metodo [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="6599f-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6599f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6599f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="6599f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6599f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6599f-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6599f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6599f-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="6599f-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="6599f-109">Puntatore a questo oggetto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="6599f-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="6599f-110">*pIPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6599f-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6599f-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="6599f-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="6599f-112">Tavolozza immagini da copiare.</span><span class="sxs-lookup"><span data-stu-id="6599f-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6599f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6599f-113">Return value</span></span>

<span data-ttu-id="6599f-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6599f-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6599f-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6599f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6599f-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6599f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6599f-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="6599f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6599f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6599f-118">Requirements</span></span>



| <span data-ttu-id="6599f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6599f-119">Requirement</span></span> | <span data-ttu-id="6599f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6599f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6599f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6599f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6599f-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6599f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6599f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6599f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6599f-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6599f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6599f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6599f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6599f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6599f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




