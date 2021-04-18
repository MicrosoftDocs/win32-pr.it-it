---
description: Funzione proxy per il metodo CreateBitmapFromHICON.
ms.assetid: 5df3d9d9-1b23-4f38-b97e-0b77d6db99d8
title: Funzione IWICImagingFactory_CreateBitmapFromHICON_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHICON_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 58f9f37dc27c76a9eaa55d6baec52efbb773343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316807"
---
# <a name="iwicimagingfactory_createbitmapfromhicon_proxy-function"></a><span data-ttu-id="5024c-103">IWICImagingFactory \_ CreateBitmapFromHICON- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="5024c-103">IWICImagingFactory\_CreateBitmapFromHICON\_Proxy function</span></span>

<span data-ttu-id="5024c-104">Funzione proxy per il metodo [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) .</span><span class="sxs-lookup"><span data-stu-id="5024c-104">Proxy function for the [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5024c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5024c-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHICON_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  HICON              hIcon,
  _Out_ IWICBitmap         **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="5024c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5024c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5024c-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5024c-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5024c-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="5024c-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="5024c-109">_hIcon \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5024c-109">_hIcon\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5024c-110">Tipo: **HICON**</span><span class="sxs-lookup"><span data-stu-id="5024c-110">Type: **HICON**</span></span>

<span data-ttu-id="5024c-111">Handle dell'icona da cui creare la nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="5024c-111">The icon handle to create the new bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="5024c-112">*ppIBitmap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5024c-112">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5024c-113">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="5024c-113">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="5024c-114">Puntatore che riceve un puntatore alla nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="5024c-114">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5024c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5024c-115">Return value</span></span>

<span data-ttu-id="5024c-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5024c-116">Type: **HRESULT**</span></span>

<span data-ttu-id="5024c-117">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5024c-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5024c-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5024c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5024c-119">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="5024c-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5024c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5024c-120">Requirements</span></span>



| <span data-ttu-id="5024c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5024c-121">Requirement</span></span> | <span data-ttu-id="5024c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5024c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5024c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5024c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5024c-124">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5024c-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5024c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5024c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5024c-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5024c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5024c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5024c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5024c-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5024c-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




