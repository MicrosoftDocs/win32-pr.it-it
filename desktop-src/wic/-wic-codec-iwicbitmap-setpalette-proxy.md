---
description: IWICBitmap_SetPalette_Proxy funzione proxy per il metodo SetPalette.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: IWICBitmap_SetPalette_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc8d6181cf9fe9313755fd52d54319f266f4cae6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086409"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="78de8-103">Funzione proxy IWICBitmap \_ SetPalette \_</span><span class="sxs-lookup"><span data-stu-id="78de8-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="78de8-104">Funzione proxy per il [**metodo SetPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)</span><span class="sxs-lookup"><span data-stu-id="78de8-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78de8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78de8-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="78de8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="78de8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78de8-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78de8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78de8-108">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="78de8-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="78de8-109">Puntatore a [**questo oggetto IWICBitmap.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)</span><span class="sxs-lookup"><span data-stu-id="78de8-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="78de8-110">*pIPalette* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="78de8-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78de8-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="78de8-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="78de8-112">Tavolozza da utilizzare per la conversione.</span><span class="sxs-lookup"><span data-stu-id="78de8-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78de8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78de8-113">Return value</span></span>

<span data-ttu-id="78de8-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="78de8-114">Type: **HRESULT**</span></span>

<span data-ttu-id="78de8-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="78de8-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78de8-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="78de8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="78de8-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="78de8-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="78de8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78de8-118">Requirements</span></span>



| <span data-ttu-id="78de8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="78de8-119">Requirement</span></span> | <span data-ttu-id="78de8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="78de8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78de8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78de8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="78de8-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="78de8-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="78de8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78de8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="78de8-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="78de8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="78de8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="78de8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78de8-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="78de8-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




