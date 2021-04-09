---
description: Questo metodo restituisce un'interfaccia che fornisce l'accesso ai dati video.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'Metodo IVideoFrameNative:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966685"
---
# <a name="ivideoframenativegetdata-method"></a><span data-ttu-id="5ba49-103">Metodo IVideoFrameNative:: GetData</span><span class="sxs-lookup"><span data-stu-id="5ba49-103">IVideoFrameNative::GetData method</span></span>

<span data-ttu-id="5ba49-104">Questo metodo restituisce un'interfaccia che fornisce l'accesso ai dati video.</span><span class="sxs-lookup"><span data-stu-id="5ba49-104">This method returns an interface that provides access to the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ba49-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ba49-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="5ba49-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ba49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ba49-107">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ba49-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba49-108">IID dell'interfaccia da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5ba49-108">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5ba49-109">*PPV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ba49-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba49-110">Quando questo metodo viene restituito correttamente, contiene il puntatore a interfaccia richiesto nel parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="5ba49-110">When this method returns successfully, contains the interface pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ba49-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ba49-111">Return value</span></span>

<span data-ttu-id="5ba49-112">Restituisce \_ OK se il completamento è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5ba49-112">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="5ba49-113">Restituisce E \_ nointerface se non è possibile trovare l'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="5ba49-113">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ba49-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ba49-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ba49-115">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="5ba49-115">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



