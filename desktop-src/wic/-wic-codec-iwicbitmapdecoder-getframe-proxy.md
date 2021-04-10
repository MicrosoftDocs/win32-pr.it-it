---
description: Funzione proxy per il metodo GetFrame.
ms.assetid: 31612afa-5017-4ddb-bdf8-25555db35da5
title: Funzione IWICBitmapDecoder_GetFrame_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 996c0f412aafe6063e25a346552f9c257a51eed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343226"
---
# <a name="iwicbitmapdecoder_getframe_proxy-function"></a><span data-ttu-id="b9961-103">\_Funzione proxy GetFrame IWICBitmapDecoder \_</span><span class="sxs-lookup"><span data-stu-id="b9961-103">IWICBitmapDecoder\_GetFrame\_Proxy function</span></span>

<span data-ttu-id="b9961-104">Funzione proxy per il metodo [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) .</span><span class="sxs-lookup"><span data-stu-id="b9961-104">Proxy function for the [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9961-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9961-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrame_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _In_  UINT                  index,
  _Out_ IWICBitmapFrameDecode **ppIBitmapFrame
);
```



## <a name="parameters"></a><span data-ttu-id="b9961-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9961-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9961-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9961-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="b9961-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="b9961-109">Puntatore a questo oggetto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="b9961-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="b9961-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b9961-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9961-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b9961-111">Type: **UINT**</span></span>

<span data-ttu-id="b9961-112">Frame particolare da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b9961-112">The particular frame to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b9961-113">*ppIBitmapFrame* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b9961-113">*ppIBitmapFrame* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9961-114">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span><span class="sxs-lookup"><span data-stu-id="b9961-114">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span></span>

<span data-ttu-id="b9961-115">Puntatore che riceve un puntatore a [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="b9961-115">A pointer that receives a pointer to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9961-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9961-116">Return value</span></span>

<span data-ttu-id="b9961-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b9961-117">Type: **HRESULT**</span></span>

<span data-ttu-id="b9961-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b9961-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9961-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9961-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9961-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b9961-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b9961-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9961-121">Requirements</span></span>



| <span data-ttu-id="b9961-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9961-122">Requirement</span></span> | <span data-ttu-id="b9961-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b9961-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9961-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9961-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b9961-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9961-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b9961-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9961-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b9961-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9961-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b9961-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b9961-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9961-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9961-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




