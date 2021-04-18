---
description: Funzione proxy per il metodo InitializeCustom.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: Funzione IWICPalette_InitializeCustom_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3b64daf458a6b916f0f9e2ba23e135d6c7328a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317255"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a><span data-ttu-id="582d0-103">IWICPalette \_ InitializeCustom- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="582d0-103">IWICPalette\_InitializeCustom\_Proxy function</span></span>

<span data-ttu-id="582d0-104">Funzione proxy per il metodo [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) .</span><span class="sxs-lookup"><span data-stu-id="582d0-104">Proxy function for the [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="582d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="582d0-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a><span data-ttu-id="582d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="582d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="582d0-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="582d0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="582d0-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="582d0-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="582d0-109">Puntatore a questo oggetto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="582d0-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="582d0-110">*pColors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="582d0-110">*pColors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="582d0-111">Tipo: \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="582d0-111">Type: \**WICColor\** _</span></span>

<span data-ttu-id="582d0-112">Puntatore alla matrice di colori.</span><span class="sxs-lookup"><span data-stu-id="582d0-112">Pointer to the color array.</span></span>

</dd> <dt>

<span data-ttu-id="582d0-113">_colorCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="582d0-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="582d0-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="582d0-114">Type: **UINT**</span></span>

<span data-ttu-id="582d0-115">Il numero di colori in *pColors*.</span><span class="sxs-lookup"><span data-stu-id="582d0-115">The number of colors in *pColors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="582d0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="582d0-116">Return value</span></span>

<span data-ttu-id="582d0-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="582d0-117">Type: **HRESULT**</span></span>

<span data-ttu-id="582d0-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="582d0-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="582d0-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="582d0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="582d0-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="582d0-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="582d0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="582d0-121">Requirements</span></span>



| <span data-ttu-id="582d0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="582d0-122">Requirement</span></span> | <span data-ttu-id="582d0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="582d0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582d0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="582d0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="582d0-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="582d0-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="582d0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="582d0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="582d0-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="582d0-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="582d0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="582d0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="582d0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="582d0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




