---
description: Questo metodo restituisce un dispositivo associato ai dati video.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'Metodo IVideoFrameNative:: GetDevice'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401657"
---
# <a name="ivideoframenativegetdevice-method"></a><span data-ttu-id="a90f5-103">Metodo IVideoFrameNative:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="a90f5-103">IVideoFrameNative::GetDevice method</span></span>

<span data-ttu-id="a90f5-104">Questo metodo restituisce un dispositivo associato ai dati video.</span><span class="sxs-lookup"><span data-stu-id="a90f5-104">This method returns a device associated with the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a90f5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a90f5-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="a90f5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a90f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a90f5-107">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a90f5-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a90f5-108">IID del dispositivo da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a90f5-108">The IID of the device to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a90f5-109">*PPV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a90f5-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a90f5-110">Quando questo metodo viene restituito correttamente, contiene il puntatore del dispositivo richiesto nel parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="a90f5-110">When this method returns successfully, contains the device pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a90f5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a90f5-111">Return value</span></span>

<span data-ttu-id="a90f5-112">Restituisce \_ OK se il completamento è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a90f5-112">Returns S\_OK on successful completion.</span></span>

## <a name="see-also"></a><span data-ttu-id="a90f5-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a90f5-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a90f5-114">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="a90f5-114">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



