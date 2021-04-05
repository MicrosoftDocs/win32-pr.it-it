---
description: Funzione proxy per il metodo GetColorCount.
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: Funzione IWICPalette_GetColorCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9518878dd05c6b89152b91863c8996f96b8e6e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883410"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a><span data-ttu-id="3f231-103">IWICPalette \_ GetColorCount- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="3f231-103">IWICPalette\_GetColorCount\_Proxy function</span></span>

<span data-ttu-id="3f231-104">Funzione proxy per il metodo [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) .</span><span class="sxs-lookup"><span data-stu-id="3f231-104">Proxy function for the [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f231-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f231-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="3f231-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f231-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f231-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f231-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f231-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="3f231-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="3f231-109">Puntatore a questo oggetto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="3f231-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f231-110">*pcCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f231-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f231-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="3f231-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="3f231-112">Puntatore che riceve il numero di colori nella tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="3f231-112">Pointer that receives the number of colors in the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f231-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f231-113">Return value</span></span>

<span data-ttu-id="3f231-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3f231-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3f231-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3f231-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f231-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f231-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f231-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3f231-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3f231-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f231-118">Requirements</span></span>



| <span data-ttu-id="3f231-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f231-119">Requirement</span></span> | <span data-ttu-id="3f231-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3f231-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f231-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f231-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3f231-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f231-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3f231-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f231-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3f231-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f231-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3f231-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3f231-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f231-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f231-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




