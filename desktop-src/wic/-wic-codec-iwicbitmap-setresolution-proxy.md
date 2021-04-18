---
description: Funzione proxy per il metodo di risoluzione.
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: Funzione IWICBitmap_SetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eef599147a67986c6b9853f7a67e53a15be68e00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306685"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="a38c4-103">IWICBitmap- \_ \_ funzione proxy di risoluzione</span><span class="sxs-lookup"><span data-stu-id="a38c4-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="a38c4-104">Funzione proxy per il metodo di [**risoluzione**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="a38c4-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a38c4-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="a38c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a38c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a38c4-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a38c4-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38c4-108">Tipo: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="a38c4-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="a38c4-109">Puntatore a questo oggetto [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="a38c4-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="a38c4-110">*DpiX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a38c4-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38c4-111">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="a38c4-111">Type: **double**</span></span>

<span data-ttu-id="a38c4-112">Risoluzione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="a38c4-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="a38c4-113">*DpiY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a38c4-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38c4-114">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="a38c4-114">Type: **double**</span></span>

<span data-ttu-id="a38c4-115">Risoluzione verticale.</span><span class="sxs-lookup"><span data-stu-id="a38c4-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a38c4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a38c4-116">Return value</span></span>

<span data-ttu-id="a38c4-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a38c4-117">Type: **HRESULT**</span></span>

<span data-ttu-id="a38c4-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a38c4-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a38c4-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a38c4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a38c4-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a38c4-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a38c4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a38c4-121">Requirements</span></span>



| <span data-ttu-id="a38c4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a38c4-122">Requirement</span></span> | <span data-ttu-id="a38c4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a38c4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a38c4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a38c4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a38c4-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a38c4-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a38c4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a38c4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a38c4-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a38c4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a38c4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a38c4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a38c4-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a38c4-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




