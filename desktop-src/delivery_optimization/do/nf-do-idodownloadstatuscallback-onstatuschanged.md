---
title: 'Metodo IDODownloadStatusCallback:: OnStatusChange'
description: Chiama l'implementazione di questo metodo ogni volta che viene modificato lo stato del download.
keywords:
- 'Metodo IDODownloadStatusCallback:: OnStatusChange'
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104046146"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a><span data-ttu-id="548a8-104">Metodo IDODownloadStatusCallback:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="548a8-104">IDODownloadStatusCallback::OnStatusChange method</span></span>

<span data-ttu-id="548a8-105">Chiama l'implementazione di questo metodo ogni volta che viene modificato lo stato del download.</span><span class="sxs-lookup"><span data-stu-id="548a8-105">DO calls your implementation of this method any time a download status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="548a8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="548a8-106">Syntax</span></span>

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="548a8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="548a8-107">Parameters</span></span>

`download`

<span data-ttu-id="548a8-108">Puntatore all'interfaccia **IDODownload** il cui stato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="548a8-108">An pointer to the **IDODownload** interface whose status changed.</span></span>

`status`

<span data-ttu-id="548a8-109">Puntatore a una struttura **DO_DOWNLOAD_STATUS** contenente lo stato del download.</span><span class="sxs-lookup"><span data-stu-id="548a8-109">A pointer to a **DO_DOWNLOAD_STATUS** structure containing the download's status.</span></span>

## <a name="return-value"></a><span data-ttu-id="548a8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="548a8-110">Return Value</span></span>

<span data-ttu-id="548a8-111">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="548a8-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="548a8-112">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="548a8-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="548a8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="548a8-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="548a8-114">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="548a8-114">**Minimum supported client**</span></span> | <span data-ttu-id="548a8-115">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="548a8-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="548a8-116">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="548a8-116">**Minimum supported server**</span></span> | <span data-ttu-id="548a8-117">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="548a8-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="548a8-118">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="548a8-118">**Header**</span></span> | <span data-ttu-id="548a8-119">Do. h</span><span class="sxs-lookup"><span data-stu-id="548a8-119">Do.h</span></span> |
