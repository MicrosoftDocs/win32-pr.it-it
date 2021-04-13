---
description: Funzione proxy per il metodo sepalette.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: Funzione IWICBitmap_SetPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d683dda81d52818bfc7d878d044af9b4e09869b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525939"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="ba0d7-103">\_Funzione proxy IWICBitmap Sepalette \_</span><span class="sxs-lookup"><span data-stu-id="ba0d7-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="ba0d7-104">Funzione proxy per il metodo [**sepalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="ba0d7-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0d7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba0d7-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="ba0d7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba0d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba0d7-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba0d7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0d7-108">Tipo: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="ba0d7-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="ba0d7-109">Puntatore a questo oggetto [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="ba0d7-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d7-110">*pIPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba0d7-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0d7-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="ba0d7-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="ba0d7-112">Tavolozza da utilizzare per la conversione.</span><span class="sxs-lookup"><span data-stu-id="ba0d7-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba0d7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba0d7-113">Return value</span></span>

<span data-ttu-id="ba0d7-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ba0d7-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ba0d7-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ba0d7-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba0d7-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba0d7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba0d7-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ba0d7-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0d7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba0d7-118">Requirements</span></span>



| <span data-ttu-id="ba0d7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba0d7-119">Requirement</span></span> | <span data-ttu-id="ba0d7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ba0d7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0d7-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba0d7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba0d7-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba0d7-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ba0d7-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba0d7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba0d7-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba0d7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ba0d7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ba0d7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba0d7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba0d7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




