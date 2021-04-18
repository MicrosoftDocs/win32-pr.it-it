---
description: Funzione proxy per il metodo CopyPalette.
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: Funzione IWICBitmapSource_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 792738a6be3966e898527c357c99a8cd6c5cfdb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319127"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="9382a-103">IWICBitmapSource \_ CopyPalette- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="9382a-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="9382a-104">Funzione proxy per il metodo [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="9382a-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9382a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9382a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="9382a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9382a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9382a-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9382a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9382a-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="9382a-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="9382a-109">Puntatore a questo oggetto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="9382a-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="9382a-110">*pIPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9382a-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9382a-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="9382a-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="9382a-112">Tavolozza.</span><span class="sxs-lookup"><span data-stu-id="9382a-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9382a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9382a-113">Return value</span></span>

<span data-ttu-id="9382a-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9382a-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9382a-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9382a-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9382a-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9382a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9382a-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="9382a-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9382a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9382a-118">Requirements</span></span>



| <span data-ttu-id="9382a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9382a-119">Requirement</span></span> | <span data-ttu-id="9382a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9382a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9382a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9382a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9382a-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9382a-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9382a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9382a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9382a-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9382a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9382a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9382a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9382a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9382a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




