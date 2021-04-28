---
description: IWICBitmapFrameEncode_Commit_Proxy funzione proxy per il metodo Commit.
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: IWICBitmapFrameEncode_Commit_Proxy funzione
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
ms.openlocfilehash: 0f8ab87860c77cf58f73491a1fb5fc1b658ed67f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091119"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="0a7b3-103">Funzione proxy commit IWICBitmapFrameEncode \_ \_</span><span class="sxs-lookup"><span data-stu-id="0a7b3-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="0a7b3-104">Funzione proxy per il [**metodo Commit.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)</span><span class="sxs-lookup"><span data-stu-id="0a7b3-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a7b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a7b3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="0a7b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a7b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a7b3-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a7b3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a7b3-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="0a7b3-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="0a7b3-109">Puntatore a [**questo oggetto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="0a7b3-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a7b3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a7b3-110">Return value</span></span>

<span data-ttu-id="0a7b3-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0a7b3-111">Type: **HRESULT**</span></span>

<span data-ttu-id="0a7b3-112">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0a7b3-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a7b3-113">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0a7b3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a7b3-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="0a7b3-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0a7b3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a7b3-115">Requirements</span></span>



| <span data-ttu-id="0a7b3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a7b3-116">Requirement</span></span> | <span data-ttu-id="0a7b3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0a7b3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7b3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a7b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0a7b3-119">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0a7b3-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0a7b3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a7b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0a7b3-121">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a7b3-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0a7b3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0a7b3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a7b3-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a7b3-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




