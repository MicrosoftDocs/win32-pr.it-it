---
description: Funzione proxy per il metodo Initialize.
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: Funzione IWICBitmapClipper_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapClipper_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 83c41b8802546b36ad309306ecc83a34c5d3a0c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128967"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="73a40-103">IWICBitmapClipper \_ Inizializza la \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="73a40-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="73a40-104">Funzione proxy per il metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) .</span><span class="sxs-lookup"><span data-stu-id="73a40-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a40-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73a40-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="73a40-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="73a40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73a40-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73a40-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a40-108">Tipo: \**[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) \** _</span><span class="sxs-lookup"><span data-stu-id="73a40-108">Type: \**[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\** _</span></span>

<span data-ttu-id="73a40-109">Puntatore a questo oggetto [_ *IWICBitmapClipper* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="73a40-109">Pointer to this [_ *IWICBitmapClipper*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="73a40-110">*pISource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73a40-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a40-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="73a40-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="73a40-112">Origine della bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="73a40-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="73a40-113">_prc \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73a40-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a40-114">Tipo: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="73a40-114">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="73a40-115">Rettangolo dell'origine bitmap da ritagliare.</span><span class="sxs-lookup"><span data-stu-id="73a40-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73a40-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73a40-116">Return value</span></span>

<span data-ttu-id="73a40-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="73a40-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="73a40-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="73a40-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73a40-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73a40-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73a40-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="73a40-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="73a40-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73a40-121">Requirements</span></span>



| <span data-ttu-id="73a40-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="73a40-122">Requirement</span></span> | <span data-ttu-id="73a40-123">Valore</span><span class="sxs-lookup"><span data-stu-id="73a40-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73a40-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73a40-124">Minimum supported client</span></span><br/> | <span data-ttu-id="73a40-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73a40-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="73a40-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73a40-126">Minimum supported server</span></span><br/> | <span data-ttu-id="73a40-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73a40-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="73a40-128">DLL</span><span class="sxs-lookup"><span data-stu-id="73a40-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73a40-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73a40-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




