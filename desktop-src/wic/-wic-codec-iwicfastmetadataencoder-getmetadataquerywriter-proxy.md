---
description: Funzione proxy per il metodo GetMetadataQueryWriter.
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: Funzione IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 08ebc29691432ebed7b2a1eb01eecfcd109dbd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317266"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="ac667-103">IWICFastMetadataEncoder \_ GetMetadataQueryWriter- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="ac667-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="ac667-104">Funzione proxy per il metodo [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="ac667-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac667-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac667-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="ac667-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac667-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac667-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac667-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac667-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="ac667-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="ac667-109">Puntatore a questo oggetto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="ac667-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="ac667-110">*ppIMetadataQueryWriter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ac667-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac667-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="ac667-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="ac667-112">Puntatore che riceve un puntatore al writer della query di metadati del codificatore.</span><span class="sxs-lookup"><span data-stu-id="ac667-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac667-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac667-113">Return value</span></span>

<span data-ttu-id="ac667-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ac667-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ac667-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ac667-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac667-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac667-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac667-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ac667-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ac667-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac667-118">Requirements</span></span>



| <span data-ttu-id="ac667-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac667-119">Requirement</span></span> | <span data-ttu-id="ac667-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ac667-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac667-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac667-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ac667-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac667-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ac667-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac667-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ac667-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac667-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ac667-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ac667-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac667-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac667-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




