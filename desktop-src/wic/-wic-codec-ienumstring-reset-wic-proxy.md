---
description: 'Funzione proxy di Windows Imaging Component (WIC) per IEnumString:: Reset.'
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: Funzione IEnumString_Reset_WIC_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306687"
---
# <a name="ienumstring_reset_wic_proxy-function"></a><span data-ttu-id="76b08-103">IEnumString \_ Reimposta \_ la \_ funzione proxy WIC</span><span class="sxs-lookup"><span data-stu-id="76b08-103">IEnumString\_Reset\_WIC\_Proxy function</span></span>

<span data-ttu-id="76b08-104">Funzione proxy di Windows Imaging Component (WIC) per IEnumString:: Reset.</span><span class="sxs-lookup"><span data-stu-id="76b08-104">Windows Imaging Component (WIC) proxy function for IEnumString::Reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="76b08-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76b08-105">Syntax</span></span>


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="76b08-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="76b08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76b08-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76b08-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76b08-108">Tipo: \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="76b08-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="76b08-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="76b08-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="76b08-110">_celt \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76b08-110">_celt\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76b08-111">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="76b08-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="76b08-112">*rgelt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76b08-112">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76b08-113">Tipo: \**LPOLESTR \** _</span><span class="sxs-lookup"><span data-stu-id="76b08-113">Type: \**LPOLESTR\** _</span></span>

</dd> <dt>

<span data-ttu-id="76b08-114">_pceltFetched \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76b08-114">_pceltFetched\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76b08-115">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="76b08-115">Type: \**ULONG\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76b08-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76b08-116">Return value</span></span>

<span data-ttu-id="76b08-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="76b08-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="76b08-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="76b08-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76b08-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76b08-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="76b08-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="76b08-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="76b08-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76b08-121">Requirements</span></span>



| <span data-ttu-id="76b08-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="76b08-122">Requirement</span></span> | <span data-ttu-id="76b08-123">Valore</span><span class="sxs-lookup"><span data-stu-id="76b08-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76b08-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76b08-124">Minimum supported client</span></span><br/> | <span data-ttu-id="76b08-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76b08-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="76b08-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76b08-126">Minimum supported server</span></span><br/> | <span data-ttu-id="76b08-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76b08-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="76b08-128">DLL</span><span class="sxs-lookup"><span data-stu-id="76b08-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76b08-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76b08-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




