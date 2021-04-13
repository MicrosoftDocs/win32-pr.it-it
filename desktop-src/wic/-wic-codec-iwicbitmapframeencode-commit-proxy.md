---
description: Funzione proxy per il metodo commit.
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: Funzione IWICBitmapFrameEncode_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0da0cb95a13148082d8263f622bb4089a7c9bd30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343206"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="dadd6-103">\_ \_ Funzione proxy commit IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="dadd6-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="dadd6-104">Funzione proxy per il metodo [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) .</span><span class="sxs-lookup"><span data-stu-id="dadd6-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dadd6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dadd6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="dadd6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dadd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dadd6-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dadd6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadd6-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="dadd6-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="dadd6-109">Puntatore a questo oggetto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="dadd6-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dadd6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dadd6-110">Return value</span></span>

<span data-ttu-id="dadd6-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dadd6-111">Type: **HRESULT**</span></span>

<span data-ttu-id="dadd6-112">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dadd6-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dadd6-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dadd6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dadd6-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="dadd6-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dadd6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dadd6-115">Requirements</span></span>



| <span data-ttu-id="dadd6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dadd6-116">Requirement</span></span> | <span data-ttu-id="dadd6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="dadd6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dadd6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dadd6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dadd6-119">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dadd6-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dadd6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dadd6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dadd6-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dadd6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dadd6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="dadd6-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dadd6-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dadd6-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




