---
description: IWICBitmapFlipRotator_Initialize_Proxy funzione proxy per il metodo Initialize.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4a260d6e60c0ffdeb05aa064ae8abbb38818ac8c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091159"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="76225-103">Funzione IWICBitmapFlipRotator \_ Initialize \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="76225-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="76225-104">Funzione proxy per il [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize)</span><span class="sxs-lookup"><span data-stu-id="76225-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="76225-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76225-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="76225-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="76225-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76225-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76225-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76225-108">Tipo: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span><span class="sxs-lookup"><span data-stu-id="76225-108">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span></span>

<span data-ttu-id="76225-109">Puntatore a [**questo oggetto IWICBitmapFlipRotator.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)</span><span class="sxs-lookup"><span data-stu-id="76225-109">Pointer to this [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="76225-110">*pISource* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="76225-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76225-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="76225-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="76225-112">Origine bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="76225-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="76225-113">*opzioni* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="76225-113">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76225-114">Tipo: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="76225-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="76225-115">[**WICBitmapTransformOptions per**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) capovolgere o ruotare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="76225-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76225-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76225-116">Return value</span></span>

<span data-ttu-id="76225-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="76225-117">Type: **HRESULT**</span></span>

<span data-ttu-id="76225-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="76225-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76225-119">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="76225-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="76225-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="76225-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="76225-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76225-121">Requirements</span></span>



| <span data-ttu-id="76225-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="76225-122">Requirement</span></span> | <span data-ttu-id="76225-123">Valore</span><span class="sxs-lookup"><span data-stu-id="76225-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76225-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76225-124">Minimum supported client</span></span><br/> | <span data-ttu-id="76225-125">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="76225-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="76225-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76225-126">Minimum supported server</span></span><br/> | <span data-ttu-id="76225-127">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="76225-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="76225-128">DLL</span><span class="sxs-lookup"><span data-stu-id="76225-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76225-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="76225-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




