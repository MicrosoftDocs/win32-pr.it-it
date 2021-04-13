---
description: Funzione proxy per il metodo GetMetadataQueryReader.
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: Funzione IWICBitmapDecoder_GetMetadataQueryReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 72b47652c76934fdf3ea518925990d6d4d1d3eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343221"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="558e1-103">IWICBitmapDecoder \_ GetMetadataQueryReader- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="558e1-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="558e1-104">Funzione proxy per il metodo [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="558e1-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="558e1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="558e1-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="558e1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="558e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="558e1-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="558e1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="558e1-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="558e1-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="558e1-109">Puntatore a questo oggetto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="558e1-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="558e1-110">*ppIMetadataQueryReader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="558e1-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="558e1-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="558e1-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="558e1-112">Puntatore che riceve un puntatore ai metadati.</span><span class="sxs-lookup"><span data-stu-id="558e1-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="558e1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="558e1-113">Return value</span></span>

<span data-ttu-id="558e1-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="558e1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="558e1-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="558e1-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="558e1-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="558e1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="558e1-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="558e1-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="558e1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="558e1-118">Requirements</span></span>



| <span data-ttu-id="558e1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="558e1-119">Requirement</span></span> | <span data-ttu-id="558e1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="558e1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="558e1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="558e1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="558e1-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="558e1-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="558e1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="558e1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="558e1-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="558e1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="558e1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="558e1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="558e1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="558e1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




