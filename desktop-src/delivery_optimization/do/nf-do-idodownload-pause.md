---
title: IDODownload::P metodo ause
description: Sospende il download.
keywords:
- IDODownload::P metodo ause
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7239253238b0d9b7e606329b10f05b3645b7e16
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104117249"
---
# <a name="idodownloadpause-method"></a><span data-ttu-id="e72d1-104">IDODownload::P metodo ause</span><span class="sxs-lookup"><span data-stu-id="e72d1-104">IDODownload::Pause method</span></span>

<span data-ttu-id="e72d1-105">Sospende il download.</span><span class="sxs-lookup"><span data-stu-id="e72d1-105">Pauses the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="e72d1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e72d1-106">Syntax</span></span>

```cpp
HRESULT Pause();
```

## <a name="return-value"></a><span data-ttu-id="e72d1-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e72d1-107">Return Value</span></span>

<span data-ttu-id="e72d1-108">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="e72d1-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="e72d1-109">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="e72d1-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="e72d1-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e72d1-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e72d1-111">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="e72d1-111">**Minimum supported client**</span></span> | <span data-ttu-id="e72d1-112">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="e72d1-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e72d1-113">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="e72d1-113">**Minimum supported server**</span></span> | <span data-ttu-id="e72d1-114">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="e72d1-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e72d1-115">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e72d1-115">**Header**</span></span> | <span data-ttu-id="e72d1-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="e72d1-116">Do.h</span></span> |
