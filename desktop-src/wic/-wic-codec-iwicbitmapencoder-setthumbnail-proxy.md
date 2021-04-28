---
description: IWICBitmapEncoder_SetThumbnail_Proxy funzione proxy per il metodo SetThumbnail.
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: IWICBitmapEncoder_SetThumbnail_Proxy funzione
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
ms.openlocfilehash: a7666fffbac7813db8021daf38ebae9c4e68c57a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100599"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="71eb9-103">Funzione proxy IWICBitmapEncoder \_ SetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="71eb9-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="71eb9-104">Funzione proxy per il [**metodo SetThumbnail.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)</span><span class="sxs-lookup"><span data-stu-id="71eb9-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="71eb9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71eb9-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="71eb9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="71eb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71eb9-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71eb9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71eb9-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="71eb9-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="71eb9-109">Puntatore a [**questo oggetto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="71eb9-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="71eb9-110">*pIThumbnail* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="71eb9-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71eb9-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="71eb9-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="71eb9-112">Oggetto [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) da impostare come anteprima globale.</span><span class="sxs-lookup"><span data-stu-id="71eb9-112">The [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71eb9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71eb9-113">Return value</span></span>

<span data-ttu-id="71eb9-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="71eb9-114">Type: **HRESULT**</span></span>

<span data-ttu-id="71eb9-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="71eb9-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71eb9-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="71eb9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="71eb9-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="71eb9-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="71eb9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71eb9-118">Requirements</span></span>



| <span data-ttu-id="71eb9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="71eb9-119">Requirement</span></span> | <span data-ttu-id="71eb9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="71eb9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71eb9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71eb9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="71eb9-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="71eb9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="71eb9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71eb9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="71eb9-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="71eb9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="71eb9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="71eb9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71eb9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="71eb9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




