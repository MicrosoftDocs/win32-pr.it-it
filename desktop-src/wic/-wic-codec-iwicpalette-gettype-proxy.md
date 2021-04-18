---
description: Funzione proxy per il metodo GetType.
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: Funzione IWICPalette_GetType_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: faa027a6366965b232a988daeab063fd902f7805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314888"
---
# <a name="iwicpalette_gettype_proxy-function"></a><span data-ttu-id="b7f44-103">\_Funzione proxy GetType IWICPalette \_</span><span class="sxs-lookup"><span data-stu-id="b7f44-103">IWICPalette\_GetType\_Proxy function</span></span>

<span data-ttu-id="b7f44-104">Funzione proxy per il metodo [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) .</span><span class="sxs-lookup"><span data-stu-id="b7f44-104">Proxy function for the [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f44-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7f44-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a><span data-ttu-id="b7f44-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7f44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7f44-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7f44-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7f44-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="b7f44-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="b7f44-109">Puntatore a questo oggetto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="b7f44-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="b7f44-110">*pePaletteType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b7f44-110">*pePaletteType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7f44-111">Tipo: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype) \** _</span><span class="sxs-lookup"><span data-stu-id="b7f44-111">Type: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)\** _</span></span>

<span data-ttu-id="b7f44-112">Puntatore che riceve il tipo di tavolozza di bimtap.</span><span class="sxs-lookup"><span data-stu-id="b7f44-112">Pointer that receives the palette type of the bimtap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7f44-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7f44-113">Return value</span></span>

<span data-ttu-id="b7f44-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b7f44-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b7f44-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b7f44-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7f44-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7f44-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7f44-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b7f44-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f44-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7f44-118">Requirements</span></span>



| <span data-ttu-id="b7f44-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f44-119">Requirement</span></span> | <span data-ttu-id="b7f44-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b7f44-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f44-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f44-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f44-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7f44-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b7f44-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f44-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f44-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7f44-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b7f44-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b7f44-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7f44-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7f44-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




