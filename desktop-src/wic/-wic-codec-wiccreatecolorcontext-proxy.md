---
description: Funzione proxy per la creazione di un IWICColorContext.
ms.assetid: 66348ef2-3056-4ec7-84ad-6e022e320a33
title: Funzione WICCreateColorContext_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorContext_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e4861bb1ccb275edc38163335e0da5d26441a334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313421"
---
# <a name="wiccreatecolorcontext_proxy-function"></a><span data-ttu-id="c2095-103">\_Funzione proxy WICCreateColorContext</span><span class="sxs-lookup"><span data-stu-id="c2095-103">WICCreateColorContext\_Proxy function</span></span>

<span data-ttu-id="c2095-104">Funzione proxy per la creazione di un [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="c2095-104">Proxy function for creating an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2095-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2095-105">Syntax</span></span>


```C++
HRESULT WICCreateColorContext_Proxy(
  _In_ IWICImagingFactory *THIS_PTR,
       IWICColorContext   ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="c2095-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2095-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2095-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2095-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2095-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="c2095-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

<span data-ttu-id="c2095-109">Puntatore a questo oggetto [_ *IWICImagingFactory* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) .</span><span class="sxs-lookup"><span data-stu-id="c2095-109">Pointer to this [_ *IWICImagingFactory*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="c2095-110">*ppIColorContext*</span><span class="sxs-lookup"><span data-stu-id="c2095-110">*ppIColorContext*</span></span> 
</dt> <dd>

<span data-ttu-id="c2095-111">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span><span class="sxs-lookup"><span data-stu-id="c2095-111">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2095-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2095-112">Return value</span></span>

<span data-ttu-id="c2095-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c2095-113">Type: **HRESULT**</span></span>

<span data-ttu-id="c2095-114">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c2095-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2095-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2095-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2095-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c2095-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c2095-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2095-117">Requirements</span></span>



| <span data-ttu-id="c2095-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2095-118">Requirement</span></span> | <span data-ttu-id="c2095-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c2095-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2095-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2095-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2095-121">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2095-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c2095-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2095-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2095-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2095-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c2095-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c2095-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2095-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2095-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




