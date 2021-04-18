---
description: Funzione proxy per il metodo Initialize.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: Funzione IWICBitmapFlipRotator_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306670"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="3c71f-103">IWICBitmapFlipRotator \_ Inizializza la \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="3c71f-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="3c71f-104">Funzione proxy per il metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .</span><span class="sxs-lookup"><span data-stu-id="3c71f-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c71f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c71f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="3c71f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c71f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c71f-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c71f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c71f-108">Tipo: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _</span><span class="sxs-lookup"><span data-stu-id="3c71f-108">Type: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\** _</span></span>

<span data-ttu-id="3c71f-109">Puntatore a questo oggetto [_ *IWICBitmapFlipRotator* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="3c71f-109">Pointer to this [_ *IWICBitmapFlipRotator*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="3c71f-110">*pISource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c71f-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c71f-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="3c71f-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="3c71f-112">Origine della bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="3c71f-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="3c71f-113">_options \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c71f-113">_options\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c71f-114">Tipo: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="3c71f-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="3c71f-115">[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) per capovolgere o ruotare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="3c71f-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c71f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c71f-116">Return value</span></span>

<span data-ttu-id="3c71f-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3c71f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="3c71f-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3c71f-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c71f-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c71f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c71f-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3c71f-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3c71f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c71f-121">Requirements</span></span>



| <span data-ttu-id="3c71f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c71f-122">Requirement</span></span> | <span data-ttu-id="3c71f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3c71f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c71f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c71f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3c71f-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c71f-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3c71f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c71f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3c71f-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c71f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3c71f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3c71f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c71f-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c71f-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




