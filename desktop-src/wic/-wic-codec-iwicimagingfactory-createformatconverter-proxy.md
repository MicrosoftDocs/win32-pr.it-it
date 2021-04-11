---
description: Funzione proxy per il metodo CreateFormatConverter.
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: Funzione IWICImagingFactory_CreateFormatConverter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 91e0d87a57326e413e725e056bd5f44aff152934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233168"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a><span data-ttu-id="e93bc-103">IWICImagingFactory \_ CreateFormatConverter- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="e93bc-103">IWICImagingFactory\_CreateFormatConverter\_Proxy function</span></span>

<span data-ttu-id="e93bc-104">Funzione proxy per il metodo [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="e93bc-104">Proxy function for the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e93bc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e93bc-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a><span data-ttu-id="e93bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e93bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e93bc-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e93bc-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e93bc-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="e93bc-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="e93bc-109">_ppIFormatConverter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e93bc-109">_ppIFormatConverter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e93bc-110">Tipo: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span><span class="sxs-lookup"><span data-stu-id="e93bc-110">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span></span>

<span data-ttu-id="e93bc-111">Puntatore che riceve un puntatore a un nuovo [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span><span class="sxs-lookup"><span data-stu-id="e93bc-111">A pointer that receives a pointer to a new [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e93bc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e93bc-112">Return value</span></span>

<span data-ttu-id="e93bc-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e93bc-113">Type: **HRESULT**</span></span>

<span data-ttu-id="e93bc-114">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e93bc-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e93bc-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e93bc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e93bc-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e93bc-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e93bc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e93bc-117">Requirements</span></span>



| <span data-ttu-id="e93bc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e93bc-118">Requirement</span></span> | <span data-ttu-id="e93bc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e93bc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e93bc-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e93bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e93bc-121">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e93bc-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e93bc-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e93bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e93bc-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e93bc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e93bc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e93bc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e93bc-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e93bc-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




