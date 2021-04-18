---
title: 'Metodo IDODownload:: Finalize'
description: Completa il download.
keywords:
- 'Metodo IDODownload:: Finalize'
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 6befc9a7e64fb0963d45257d68d6bb8d2ba7a2cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299305"
---
# <a name="idodownloadfinalize-method"></a><span data-ttu-id="48a97-104">Metodo IDODownload:: Finalize</span><span class="sxs-lookup"><span data-stu-id="48a97-104">IDODownload::Finalize method</span></span>

<span data-ttu-id="48a97-105">Completa il download.</span><span class="sxs-lookup"><span data-stu-id="48a97-105">Finalizes the download.</span></span> <span data-ttu-id="48a97-106">Una volta finalizzato, un download non può essere ripreso chiamando **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="48a97-106">Once finalized, a download cannot be resumed by calling **Start**.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a97-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48a97-107">Syntax</span></span>

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a><span data-ttu-id="48a97-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48a97-108">Return Value</span></span>

<span data-ttu-id="48a97-109">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="48a97-109">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="48a97-110">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="48a97-110">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="48a97-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48a97-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="48a97-112">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="48a97-112">**Minimum supported client**</span></span> | <span data-ttu-id="48a97-113">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="48a97-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="48a97-114">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="48a97-114">**Minimum supported server**</span></span> | <span data-ttu-id="48a97-115">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="48a97-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="48a97-116">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="48a97-116">**Header**</span></span> | <span data-ttu-id="48a97-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="48a97-117">Do.h</span></span> |
