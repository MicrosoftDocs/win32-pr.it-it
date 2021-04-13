---
description: Funzione proxy per il metodo sethumbnail.
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: Funzione IWICBitmapEncoder_SetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d2670dae0d8ba9eeda7ca1d6dce5d3957dc59b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484764"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="c83ce-103">IWICBitmapEncoder \_ \_ funzione proxy di anteprima</span><span class="sxs-lookup"><span data-stu-id="c83ce-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="c83ce-104">Funzione proxy per il metodo [**sethumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="c83ce-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c83ce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c83ce-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="c83ce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c83ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c83ce-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c83ce-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c83ce-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="c83ce-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="c83ce-109">Puntatore a questo oggetto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="c83ce-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="c83ce-110">*pIThumbnail* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c83ce-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c83ce-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="c83ce-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="c83ce-112">[_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) da impostare come anteprima globale.</span><span class="sxs-lookup"><span data-stu-id="c83ce-112">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c83ce-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c83ce-113">Return value</span></span>

<span data-ttu-id="c83ce-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c83ce-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c83ce-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c83ce-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c83ce-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c83ce-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c83ce-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c83ce-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c83ce-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c83ce-118">Requirements</span></span>



| <span data-ttu-id="c83ce-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c83ce-119">Requirement</span></span> | <span data-ttu-id="c83ce-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c83ce-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c83ce-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83ce-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c83ce-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c83ce-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c83ce-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83ce-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c83ce-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c83ce-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c83ce-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c83ce-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c83ce-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c83ce-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




