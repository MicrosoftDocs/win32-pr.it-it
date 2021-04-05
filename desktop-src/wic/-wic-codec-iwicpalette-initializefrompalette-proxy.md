---
description: Funzione proxy per il metodo InitializeFromPalette.
ms.assetid: e7156cae-8d59-4dbd-8845-0e892e10107b
title: Funzione IWICPalette_InitializeFromPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 130c135d3c32135aeefd25fe8799e50c0b5ec855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884653"
---
# <a name="iwicpalette_initializefrompalette_proxy-function"></a><span data-ttu-id="d7746-103">IWICPalette \_ InitializeFromPalette- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="d7746-103">IWICPalette\_InitializeFromPalette\_Proxy function</span></span>

<span data-ttu-id="d7746-104">Funzione proxy per il metodo [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) .</span><span class="sxs-lookup"><span data-stu-id="d7746-104">Proxy function for the [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7746-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7746-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromPalette_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ IWICPalette *pIMILPalette
);
```



## <a name="parameters"></a><span data-ttu-id="d7746-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7746-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7746-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7746-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7746-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="d7746-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="d7746-109">Puntatore a questo oggetto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="d7746-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="d7746-110">*pIMILPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7746-110">*pIMILPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7746-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="d7746-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="d7746-112">Puntatore alla tavolozza di origine.</span><span class="sxs-lookup"><span data-stu-id="d7746-112">Pointer to the source palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7746-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7746-113">Return value</span></span>

<span data-ttu-id="d7746-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d7746-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d7746-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d7746-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7746-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7746-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7746-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d7746-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d7746-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7746-118">Requirements</span></span>



| <span data-ttu-id="d7746-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7746-119">Requirement</span></span> | <span data-ttu-id="d7746-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d7746-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7746-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7746-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7746-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7746-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d7746-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7746-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7746-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7746-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d7746-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d7746-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7746-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7746-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




