---
description: Funzione proxy per il metodo GetMetadataQueryWriter.
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: Funzione IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b536e7c4c0553df5dae0f8e11db33c6d709e8c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306671"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="32662-103">IWICBitmapEncoder \_ GetMetadataQueryWriter- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="32662-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="32662-104">Funzione proxy per il metodo [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="32662-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32662-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32662-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="32662-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32662-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32662-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32662-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32662-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="32662-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="32662-109">Puntatore a questo oggetto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="32662-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="32662-110">*ppIMetadataQueryWriter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="32662-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32662-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="32662-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="32662-112">Puntatore che riceve un puntatore a un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="32662-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32662-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32662-113">Return value</span></span>

<span data-ttu-id="32662-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="32662-114">Type: **HRESULT**</span></span>

<span data-ttu-id="32662-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="32662-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="32662-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32662-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="32662-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="32662-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="32662-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32662-118">Requirements</span></span>



| <span data-ttu-id="32662-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="32662-119">Requirement</span></span> | <span data-ttu-id="32662-120">Valore</span><span class="sxs-lookup"><span data-stu-id="32662-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32662-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32662-121">Minimum supported client</span></span><br/> | <span data-ttu-id="32662-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32662-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="32662-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32662-123">Minimum supported server</span></span><br/> | <span data-ttu-id="32662-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32662-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="32662-125">DLL</span><span class="sxs-lookup"><span data-stu-id="32662-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32662-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32662-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




