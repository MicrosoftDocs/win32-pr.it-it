---
description: Questo metodo restituisce un'interfaccia che consente di accedere ai dati audio.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'Metodo IAudioFrameNative:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129238"
---
# <a name="iaudioframenativegetdata-method"></a><span data-ttu-id="ad226-103">Metodo IAudioFrameNative:: GetData</span><span class="sxs-lookup"><span data-stu-id="ad226-103">IAudioFrameNative::GetData method</span></span>

<span data-ttu-id="ad226-104">Questo metodo restituisce un'interfaccia che consente di accedere ai dati audio.</span><span class="sxs-lookup"><span data-stu-id="ad226-104">This method returns an interface that provides access to the audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad226-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad226-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="ad226-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad226-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad226-107">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad226-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad226-108">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="ad226-108">Type: **REFIID**</span></span>

<span data-ttu-id="ad226-109">IID dell'interfaccia da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ad226-109">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ad226-110">*PPV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ad226-110">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad226-111">Tipo: \**LPVOID \** _</span><span class="sxs-lookup"><span data-stu-id="ad226-111">Type: \**LPVOID\** _</span></span>

<span data-ttu-id="ad226-112">Quando questo metodo viene restituito correttamente, contiene il puntatore a interfaccia richiesto nel parametro _riid \*.</span><span class="sxs-lookup"><span data-stu-id="ad226-112">When this method returns successfully, contains the interface pointer requested in _riid\* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad226-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad226-113">Return value</span></span>

<span data-ttu-id="ad226-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad226-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad226-115">Restituisce \_ OK se il completamento è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ad226-115">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="ad226-116">Restituisce E \_ nointerface se non è possibile trovare l'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="ad226-116">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad226-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad226-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad226-118">**IAudioFrameNative**</span><span class="sxs-lookup"><span data-stu-id="ad226-118">**IAudioFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



