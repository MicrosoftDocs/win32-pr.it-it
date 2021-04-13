---
description: Funzione proxy per il metodo sepalette.
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: Funzione IWICBitmapEncoder_SetPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 128953cd56c3bea17ec9761a2acf2b8bc89cacfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525927"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="de10f-103">\_Funzione proxy IWICBitmapEncoder Sepalette \_</span><span class="sxs-lookup"><span data-stu-id="de10f-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="de10f-104">Funzione proxy per il metodo [**sepalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="de10f-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de10f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de10f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="de10f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de10f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de10f-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de10f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de10f-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="de10f-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="de10f-109">Puntatore a questo oggetto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="de10f-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="de10f-110">*pIPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de10f-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de10f-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="de10f-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="de10f-112">[_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) da utilizzare come tavolozza globale.</span><span class="sxs-lookup"><span data-stu-id="de10f-112">The [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de10f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de10f-113">Return value</span></span>

<span data-ttu-id="de10f-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="de10f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="de10f-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="de10f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de10f-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de10f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de10f-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="de10f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="de10f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de10f-118">Requirements</span></span>



| <span data-ttu-id="de10f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="de10f-119">Requirement</span></span> | <span data-ttu-id="de10f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="de10f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de10f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de10f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de10f-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de10f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="de10f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de10f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de10f-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de10f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="de10f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="de10f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de10f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de10f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




