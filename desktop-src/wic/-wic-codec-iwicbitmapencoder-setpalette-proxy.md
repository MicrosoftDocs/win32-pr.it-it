---
description: IWICBitmapEncoder_SetPalette_Proxy funzione proxy per il metodo SetPalette.
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: IWICBitmapEncoder_SetPalette_Proxy funzione
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
ms.openlocfilehash: 8503698a1e91b86698ba288e56cc65e4447c906e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091179"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="907f1-103">Funzione proxy IWICBitmapEncoder \_ SetPalette \_</span><span class="sxs-lookup"><span data-stu-id="907f1-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="907f1-104">Funzione proxy per il [**metodo SetPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette)</span><span class="sxs-lookup"><span data-stu-id="907f1-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="907f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="907f1-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="907f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="907f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="907f1-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="907f1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="907f1-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="907f1-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="907f1-109">Puntatore a [**questo oggetto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="907f1-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="907f1-110">*pIPalette* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="907f1-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="907f1-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="907f1-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="907f1-112">Oggetto [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) da usare come riquadro globale.</span><span class="sxs-lookup"><span data-stu-id="907f1-112">The [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="907f1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="907f1-113">Return value</span></span>

<span data-ttu-id="907f1-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="907f1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="907f1-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="907f1-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="907f1-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="907f1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="907f1-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="907f1-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="907f1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="907f1-118">Requirements</span></span>



| <span data-ttu-id="907f1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="907f1-119">Requirement</span></span> | <span data-ttu-id="907f1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="907f1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="907f1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="907f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="907f1-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="907f1-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="907f1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="907f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="907f1-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="907f1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="907f1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="907f1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="907f1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="907f1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




