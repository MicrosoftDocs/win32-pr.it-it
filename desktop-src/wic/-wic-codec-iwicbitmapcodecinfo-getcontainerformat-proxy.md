---
description: IWICBitmapCodecInfo_GetContainerFormat_Proxy funzione proxy per il metodo GetContainerFormat.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086369"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="00228-103">Funzione proxy IWICBitmapCodecInfo \_ GetContainerFormat \_</span><span class="sxs-lookup"><span data-stu-id="00228-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="00228-104">Funzione proxy per il [**metodo GetContainerFormat.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat)</span><span class="sxs-lookup"><span data-stu-id="00228-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00228-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00228-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="00228-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00228-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00228-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00228-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00228-108">Tipo: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span><span class="sxs-lookup"><span data-stu-id="00228-108">Type: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span></span>

<span data-ttu-id="00228-109">Puntatore a [**questo oggetto IWICBitmapCodecInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)</span><span class="sxs-lookup"><span data-stu-id="00228-109">Pointer to this [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="00228-110">*pguidContainerFormat* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="00228-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00228-111">Tipo: **\* GUID**</span><span class="sxs-lookup"><span data-stu-id="00228-111">Type: **GUID\***</span></span>

<span data-ttu-id="00228-112">Puntatore che riceve il GUID del contenitore.</span><span class="sxs-lookup"><span data-stu-id="00228-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00228-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00228-113">Return value</span></span>

<span data-ttu-id="00228-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00228-114">Type: **HRESULT**</span></span>

<span data-ttu-id="00228-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="00228-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00228-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="00228-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00228-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="00228-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="00228-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00228-118">Requirements</span></span>



| <span data-ttu-id="00228-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00228-119">Requirement</span></span> | <span data-ttu-id="00228-120">Valore</span><span class="sxs-lookup"><span data-stu-id="00228-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00228-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00228-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00228-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="00228-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="00228-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00228-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00228-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="00228-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="00228-125">DLL</span><span class="sxs-lookup"><span data-stu-id="00228-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00228-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="00228-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




