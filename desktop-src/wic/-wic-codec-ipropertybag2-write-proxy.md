---
description: 'Funzione proxy di Windows Imaging Component (WIC) per IPropertyBag2:: Write.'
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: Funzione IPropertyBag2_Write_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343251"
---
# <a name="ipropertybag2_write_proxy-function"></a><span data-ttu-id="098a6-103">\_Funzione proxy di scrittura IPropertyBag2 \_</span><span class="sxs-lookup"><span data-stu-id="098a6-103">IPropertyBag2\_Write\_Proxy function</span></span>

<span data-ttu-id="098a6-104">Funzione proxy di Windows Imaging Component (WIC) per IPropertyBag2:: Write.</span><span class="sxs-lookup"><span data-stu-id="098a6-104">Windows Imaging Component (WIC) proxy function for IPropertyBag2::Write.</span></span>

## <a name="syntax"></a><span data-ttu-id="098a6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="098a6-105">Syntax</span></span>


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="098a6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="098a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="098a6-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="098a6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098a6-108">Tipo: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="098a6-108">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="098a6-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="098a6-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="098a6-110">_cProperties \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="098a6-110">_cProperties\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098a6-111">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="098a6-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="098a6-112">*ppropBag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="098a6-112">*ppropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098a6-113">Tipo: \**[Campo PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="098a6-113">Type: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85))\** _</span></span>

</dd> <dt>

<span data-ttu-id="098a6-114">_pvarValue \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="098a6-114">_pvarValue\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098a6-115">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="098a6-115">Type: \**VARIANT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="098a6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="098a6-116">Return value</span></span>

<span data-ttu-id="098a6-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="098a6-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="098a6-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="098a6-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="098a6-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="098a6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="098a6-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="098a6-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="098a6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="098a6-121">Requirements</span></span>



| <span data-ttu-id="098a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="098a6-122">Requirement</span></span> | <span data-ttu-id="098a6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="098a6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="098a6-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="098a6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="098a6-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="098a6-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="098a6-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="098a6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="098a6-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="098a6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="098a6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="098a6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="098a6-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="098a6-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

