---
description: Ottiene un'icona di dispositivo personalizzata.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'Metodo IWiaUIExtension:: GetDeviceIcon (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129407"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="8b5c6-103">Metodo IWiaUIExtension:: GetDeviceIcon</span><span class="sxs-lookup"><span data-stu-id="8b5c6-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="8b5c6-104">Ottiene un'icona di dispositivo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="8b5c6-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b5c6-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="8b5c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b5c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5c6-107">*bstrDeviceId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5c6-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5c6-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8b5c6-108">Type: **BSTR**</span></span>

<span data-ttu-id="8b5c6-109">Specifica l'ID dispositivo del dispositivo WIA per il quale deve essere ottenuta l'icona.</span><span class="sxs-lookup"><span data-stu-id="8b5c6-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="8b5c6-110">*phIcon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b5c6-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5c6-111">Tipo: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="8b5c6-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="8b5c6-112">Punta a una posizione di memoria che riceverà un handle per l'icona del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b5c6-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="8b5c6-113">_nSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5c6-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5c6-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="8b5c6-114">Type: **ULONG**</span></span>

<span data-ttu-id="8b5c6-115">Specifica la dimensione dell'icona desiderata, in pixel.</span><span class="sxs-lookup"><span data-stu-id="8b5c6-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="8b5c6-116">Si presuppone che l'icona sia quadrata, mentre nSize specifica sia la larghezza che l'altezza dell'icona richiesta.</span><span class="sxs-lookup"><span data-stu-id="8b5c6-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5c6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b5c6-117">Return value</span></span>

<span data-ttu-id="8b5c6-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b5c6-118">Type: **HRESULT**</span></span>

<span data-ttu-id="8b5c6-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8b5c6-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b5c6-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b5c6-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5c6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b5c6-121">Requirements</span></span>



| <span data-ttu-id="8b5c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b5c6-122">Requirement</span></span> | <span data-ttu-id="8b5c6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8b5c6-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5c6-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b5c6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8b5c6-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8b5c6-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8b5c6-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b5c6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8b5c6-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b5c6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8b5c6-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b5c6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b5c6-129"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b5c6-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




