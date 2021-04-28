---
description: IWICBitmapClipper_Initialize_Proxy funzione proxy per il metodo Initialize.
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: IWICBitmapClipper_Initialize_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapClipper_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ce3c745d27928765fdfdf664c423f7e2146cbd5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086389"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="e3719-103">Funzione proxy di inizializzazione IWICBitmapClipper \_ \_</span><span class="sxs-lookup"><span data-stu-id="e3719-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="e3719-104">Funzione proxy per il [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize)</span><span class="sxs-lookup"><span data-stu-id="e3719-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3719-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3719-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="e3719-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3719-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3719-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3719-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3719-108">Tipo: **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span><span class="sxs-lookup"><span data-stu-id="e3719-108">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span></span>

<span data-ttu-id="e3719-109">Puntatore a [**questo oggetto IWICBitmapClipper.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)</span><span class="sxs-lookup"><span data-stu-id="e3719-109">Pointer to this [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="e3719-110">*pISource* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e3719-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3719-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="e3719-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="e3719-112">Origine bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="e3719-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="e3719-113">*prc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e3719-113">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3719-114">Tipo: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***</span><span class="sxs-lookup"><span data-stu-id="e3719-114">Type: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\***</span></span>

<span data-ttu-id="e3719-115">Rettangolo dell'origine bitmap da ritagliare.</span><span class="sxs-lookup"><span data-stu-id="e3719-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3719-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3719-116">Return value</span></span>

<span data-ttu-id="e3719-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e3719-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e3719-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3719-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3719-119">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="e3719-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3719-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e3719-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e3719-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3719-121">Requirements</span></span>



| <span data-ttu-id="e3719-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3719-122">Requirement</span></span> | <span data-ttu-id="e3719-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e3719-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3719-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3719-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e3719-125">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e3719-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e3719-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3719-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e3719-127">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3719-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e3719-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e3719-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3719-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3719-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




