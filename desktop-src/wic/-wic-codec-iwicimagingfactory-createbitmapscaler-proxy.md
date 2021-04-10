---
description: Funzione proxy per il metodo CreateBitmapScaler.
ms.assetid: 27fcb17e-bdcd-44cc-9fe6-f93816589b50
title: Funzione IWICImagingFactory_CreateBitmapScaler_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapScaler_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ac831427901de481d313833e4ca8459ccd333384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968247"
---
# <a name="iwicimagingfactory_createbitmapscaler_proxy-function"></a><span data-ttu-id="41873-103">IWICImagingFactory \_ CreateBitmapScaler- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="41873-103">IWICImagingFactory\_CreateBitmapScaler\_Proxy function</span></span>

<span data-ttu-id="41873-104">Funzione proxy per il metodo [**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="41873-104">Proxy function for the [**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="41873-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41873-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapScaler_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapScaler   **ppIBitmapScaler
);
```



## <a name="parameters"></a><span data-ttu-id="41873-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41873-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41873-107">*pFactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41873-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41873-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="41873-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="41873-109">_ppIBitmapScaler \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41873-109">_ppIBitmapScaler\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41873-110">Tipo: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span><span class="sxs-lookup"><span data-stu-id="41873-110">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span></span>

<span data-ttu-id="41873-111">Puntatore che riceve un puntatore a un nuovo [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).</span><span class="sxs-lookup"><span data-stu-id="41873-111">A pointer that receives a pointer to a new [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41873-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41873-112">Return value</span></span>

<span data-ttu-id="41873-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="41873-113">Type: **HRESULT**</span></span>

<span data-ttu-id="41873-114">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="41873-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41873-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41873-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41873-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="41873-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="41873-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41873-117">Requirements</span></span>



| <span data-ttu-id="41873-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="41873-118">Requirement</span></span> | <span data-ttu-id="41873-119">Valore</span><span class="sxs-lookup"><span data-stu-id="41873-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41873-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41873-120">Minimum supported client</span></span><br/> | <span data-ttu-id="41873-121">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41873-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="41873-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41873-122">Minimum supported server</span></span><br/> | <span data-ttu-id="41873-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41873-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="41873-124">DLL</span><span class="sxs-lookup"><span data-stu-id="41873-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41873-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41873-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




