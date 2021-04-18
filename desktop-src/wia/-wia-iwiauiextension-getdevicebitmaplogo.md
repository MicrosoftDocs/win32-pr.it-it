---
description: Ottiene un logo bitmap personalizzato per il dispositivo.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'Metodo IWiaUIExtension:: GetDeviceBitmapLogo (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307349"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a><span data-ttu-id="29dc8-103">Metodo IWiaUIExtension:: GetDeviceBitmapLogo</span><span class="sxs-lookup"><span data-stu-id="29dc8-103">IWiaUIExtension::GetDeviceBitmapLogo method</span></span>

<span data-ttu-id="29dc8-104">Ottiene un logo bitmap personalizzato per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29dc8-104">Gets a custom bitmap logo for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="29dc8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29dc8-105">Syntax</span></span>


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a><span data-ttu-id="29dc8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="29dc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29dc8-107">*bstrDeviceId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29dc8-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29dc8-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="29dc8-108">Type: **BSTR**</span></span>

<span data-ttu-id="29dc8-109">Specifica l'ID dispositivo del dispositivo WIA per il quale deve essere ottenuta l'icona.</span><span class="sxs-lookup"><span data-stu-id="29dc8-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="29dc8-110">*phBitmap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="29dc8-110">*phBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29dc8-111">Tipo: \**HBITMAP \** _</span><span class="sxs-lookup"><span data-stu-id="29dc8-111">Type: \**HBITMAP\** _</span></span>

<span data-ttu-id="29dc8-112">Punta a una posizione di memoria che riceverà un handle per il logo bitmap per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29dc8-112">Points to a memory location that will receive a handle for the bitmap logo for the device.</span></span>

</dd> <dt>

<span data-ttu-id="29dc8-113">_nMaxWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29dc8-113">_nMaxWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29dc8-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="29dc8-114">Type: **ULONG**</span></span>

<span data-ttu-id="29dc8-115">Specifica la larghezza desiderata della bitmap.</span><span class="sxs-lookup"><span data-stu-id="29dc8-115">Specifies the desired width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="29dc8-116">*nMaxHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29dc8-116">*nMaxHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29dc8-117">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="29dc8-117">Type: **ULONG**</span></span>

<span data-ttu-id="29dc8-118">Specifica l'altezza desiderata della bitmap.</span><span class="sxs-lookup"><span data-stu-id="29dc8-118">Specifies the desired height of the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29dc8-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29dc8-119">Return value</span></span>

<span data-ttu-id="29dc8-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="29dc8-120">Type: **HRESULT**</span></span>

<span data-ttu-id="29dc8-121">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="29dc8-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29dc8-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29dc8-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="29dc8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29dc8-123">Requirements</span></span>



| <span data-ttu-id="29dc8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="29dc8-124">Requirement</span></span> | <span data-ttu-id="29dc8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="29dc8-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="29dc8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29dc8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="29dc8-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="29dc8-127">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="29dc8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29dc8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="29dc8-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="29dc8-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="29dc8-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29dc8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="29dc8-131"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="29dc8-131"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




