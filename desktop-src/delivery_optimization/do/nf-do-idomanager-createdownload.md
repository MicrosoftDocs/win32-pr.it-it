---
title: 'Metodo IDOManager:: CreateDownload'
description: Crea un nuovo download.
keywords:
- 'Metodo IDOManager:: CreateDownload'
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398354"
---
# <a name="idomanagercreatedownload-method"></a><span data-ttu-id="f8f3d-104">Metodo IDOManager:: CreateDownload</span><span class="sxs-lookup"><span data-stu-id="f8f3d-104">IDOManager::CreateDownload method</span></span>

<span data-ttu-id="f8f3d-105">Crea un nuovo download.</span><span class="sxs-lookup"><span data-stu-id="f8f3d-105">Creates a new download.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f3d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8f3d-106">Syntax</span></span>

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a><span data-ttu-id="f8f3d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8f3d-107">Parameters</span></span>

`download`

<span data-ttu-id="f8f3d-108">Indirizzo di un puntatore di interfaccia **IDODownload** .</span><span class="sxs-lookup"><span data-stu-id="f8f3d-108">The address of an **IDODownload** interface pointer.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8f3d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8f3d-109">Return Value</span></span>

<span data-ttu-id="f8f3d-110">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f8f3d-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="f8f3d-111">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="f8f3d-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f3d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8f3d-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f8f3d-113">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="f8f3d-113">**Minimum supported client**</span></span> | <span data-ttu-id="f8f3d-114">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8f3d-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="f8f3d-115">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="f8f3d-115">**Minimum supported server**</span></span> | <span data-ttu-id="f8f3d-116">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="f8f3d-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="f8f3d-117">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="f8f3d-117">**Header**</span></span> | <span data-ttu-id="f8f3d-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="f8f3d-118">Do.h</span></span> |
