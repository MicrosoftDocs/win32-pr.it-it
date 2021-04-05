---
description: Funzione proxy per il metodo HasAlpha.
ms.assetid: 8af9f588-ac22-40c4-8973-9636951cc9e6
title: Funzione IWICPalette_HasAlpha_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_HasAlpha_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f9398b2d570efb41048d88ddeeeb76d62f4ca37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967925"
---
# <a name="iwicpalette_hasalpha_proxy-function"></a><span data-ttu-id="acf92-103">IWICPalette \_ HasAlpha- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="acf92-103">IWICPalette\_HasAlpha\_Proxy function</span></span>

<span data-ttu-id="acf92-104">Funzione proxy per il metodo [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) .</span><span class="sxs-lookup"><span data-stu-id="acf92-104">Proxy function for the [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf92-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acf92-105">Syntax</span></span>


```C++
HRESULT IWICPalette_HasAlpha_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ BOOL        *pfHasAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="acf92-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="acf92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf92-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="acf92-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acf92-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="acf92-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="acf92-109">Puntatore a questo oggetto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="acf92-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="acf92-110">*pfHasAlpha* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="acf92-110">*pfHasAlpha* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acf92-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="acf92-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="acf92-112">Puntatore che riceve `TRUE` se la tavolozza contiene un colore trasparente; in caso contrario, `FALSE` .</span><span class="sxs-lookup"><span data-stu-id="acf92-112">Pointer that receives `TRUE` if the palette contains a transparent color; otherwise, `FALSE`.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf92-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="acf92-113">Return value</span></span>

<span data-ttu-id="acf92-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="acf92-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="acf92-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="acf92-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="acf92-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="acf92-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="acf92-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="acf92-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="acf92-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acf92-118">Requirements</span></span>



| <span data-ttu-id="acf92-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="acf92-119">Requirement</span></span> | <span data-ttu-id="acf92-120">Valore</span><span class="sxs-lookup"><span data-stu-id="acf92-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acf92-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acf92-121">Minimum supported client</span></span><br/> | <span data-ttu-id="acf92-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="acf92-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="acf92-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acf92-123">Minimum supported server</span></span><br/> | <span data-ttu-id="acf92-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="acf92-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="acf92-125">DLL</span><span class="sxs-lookup"><span data-stu-id="acf92-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acf92-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acf92-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




