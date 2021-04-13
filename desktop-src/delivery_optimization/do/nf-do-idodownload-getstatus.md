---
title: 'Metodo IDODownload:: GetStatus'
description: Recupera un puntatore a una struttura **DO_DOWNLOAD_STATUS** che riflette lo stato corrente del download.
keywords:
- 'Metodo IDODownload:: GetStatus'
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398356"
---
# <a name="idodownloadgetstatus-method"></a><span data-ttu-id="41d22-104">Metodo IDODownload:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="41d22-104">IDODownload::GetStatus method</span></span>

<span data-ttu-id="41d22-105">Recupera un puntatore a una struttura **DO_DOWNLOAD_STATUS** che riflette lo stato corrente del download.</span><span class="sxs-lookup"><span data-stu-id="41d22-105">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d22-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41d22-106">Syntax</span></span>

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="41d22-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="41d22-107">Parameters</span></span>

`status`

<span data-ttu-id="41d22-108">Puntatore a una struttura **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="41d22-108">A pointer to a **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="return-value"></a><span data-ttu-id="41d22-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41d22-109">Return Value</span></span>

<span data-ttu-id="41d22-110">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="41d22-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="41d22-111">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="41d22-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="41d22-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41d22-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="41d22-113">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="41d22-113">**Minimum supported client**</span></span> | <span data-ttu-id="41d22-114">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="41d22-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="41d22-115">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="41d22-115">**Minimum supported server**</span></span> | <span data-ttu-id="41d22-116">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="41d22-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="41d22-117">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="41d22-117">**Header**</span></span> | <span data-ttu-id="41d22-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="41d22-118">Do.h</span></span> |
