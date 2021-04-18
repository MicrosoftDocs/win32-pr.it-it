---
description: Funzione proxy per il metodo GetMetadataQueryReader.
ms.assetid: 2a3e0a59-3524-4da4-993a-607a3727faba
title: Funzione IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e549fdfbacb5bd508a442c70c203595b8819750f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306669"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="0d6ab-103">IWICBitmapFrameDecode \_ GetMetadataQueryReader- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="0d6ab-103">IWICBitmapFrameDecode\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="0d6ab-104">Funzione proxy per il metodo [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="0d6ab-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d6ab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d6ab-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="0d6ab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d6ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d6ab-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d6ab-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6ab-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="0d6ab-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="0d6ab-109">Puntatore a questo oggetto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="0d6ab-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="0d6ab-110">*ppIMetadataQueryReader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d6ab-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6ab-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="0d6ab-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="0d6ab-112">Puntatore che riceve un puntatore a un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="0d6ab-112">A pointer that receives a pointer to an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d6ab-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d6ab-113">Return value</span></span>

<span data-ttu-id="0d6ab-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0d6ab-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0d6ab-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0d6ab-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d6ab-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d6ab-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d6ab-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="0d6ab-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0d6ab-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d6ab-118">Requirements</span></span>



| <span data-ttu-id="0d6ab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d6ab-119">Requirement</span></span> | <span data-ttu-id="0d6ab-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0d6ab-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6ab-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d6ab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d6ab-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d6ab-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0d6ab-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d6ab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d6ab-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d6ab-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0d6ab-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0d6ab-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d6ab-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d6ab-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




