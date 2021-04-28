---
description: "Metodo IWiaUIExtension::GetDeviceIcon: ottiene un'icona del dispositivo personalizzata."
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: Metodo IWiaUIExtension::GetDeviceIcon (Wiadevd.h)
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
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116659"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="475a4-103">Metodo IWiaUIExtension::GetDeviceIcon</span><span class="sxs-lookup"><span data-stu-id="475a4-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="475a4-104">Ottiene un'icona del dispositivo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="475a4-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="475a4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="475a4-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="475a4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="475a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="475a4-107">*bstrDeviceId* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="475a4-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="475a4-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="475a4-108">Type: **BSTR**</span></span>

<span data-ttu-id="475a4-109">Specifica l'ID dispositivo del dispositivo WIA per il quale è necessario ottenere l'icona.</span><span class="sxs-lookup"><span data-stu-id="475a4-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-110">*phIcon* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="475a4-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="475a4-111">Tipo: **HICON \***</span><span class="sxs-lookup"><span data-stu-id="475a4-111">Type: **HICON\***</span></span>

<span data-ttu-id="475a4-112">Punta a una posizione di memoria che riceverà un handle per l'icona per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="475a4-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="475a4-113">*nSize* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="475a4-113">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="475a4-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="475a4-114">Type: **ULONG**</span></span>

<span data-ttu-id="475a4-115">Specifica le dimensioni dell'icona desiderate, in pixel.</span><span class="sxs-lookup"><span data-stu-id="475a4-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="475a4-116">Si presuppone che l'icona sia quadrata e che nSize specifichi sia la larghezza che l'altezza dell'icona richiesta.</span><span class="sxs-lookup"><span data-stu-id="475a4-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="475a4-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="475a4-117">Return value</span></span>

<span data-ttu-id="475a4-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="475a4-118">Type: **HRESULT**</span></span>

<span data-ttu-id="475a4-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="475a4-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="475a4-120">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="475a4-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="475a4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="475a4-121">Requirements</span></span>



| <span data-ttu-id="475a4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="475a4-122">Requirement</span></span> | <span data-ttu-id="475a4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="475a4-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="475a4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="475a4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="475a4-125">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="475a4-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="475a4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="475a4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="475a4-127">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="475a4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="475a4-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="475a4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="475a4-129"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="475a4-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




