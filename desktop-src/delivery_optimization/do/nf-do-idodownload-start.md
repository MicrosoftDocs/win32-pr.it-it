---
title: 'Metodo IDODownload:: Start'
description: Avvia o riprende un download.
keywords:
- 'Metodo IDODownload:: Start'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321124"
---
# <a name="idodownloadstart-method"></a><span data-ttu-id="550dd-104">Metodo IDODownload:: Start</span><span class="sxs-lookup"><span data-stu-id="550dd-104">IDODownload::Start method</span></span>

<span data-ttu-id="550dd-105">Avvia o riprende un download, passando intervalli facoltativi come puntatore alla struttura [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) .</span><span class="sxs-lookup"><span data-stu-id="550dd-105">Starts or resumes a download, passing optional ranges as a pointer to [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="550dd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="550dd-106">Syntax</span></span>

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a><span data-ttu-id="550dd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="550dd-107">Parameters</span></span>

`ranges`

<span data-ttu-id="550dd-108">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="550dd-108">Optional.</span></span> <span data-ttu-id="550dd-109">Puntatore a una struttura di [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (per scaricare solo intervalli specifici del file).</span><span class="sxs-lookup"><span data-stu-id="550dd-109">A pointer to a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure (to download only specific ranges of the file).</span></span> <span data-ttu-id="550dd-110">Passare `nullptr` per scaricare l'intero file.</span><span class="sxs-lookup"><span data-stu-id="550dd-110">Pass `nullptr` to download the entire file.</span></span>

## <a name="return-value"></a><span data-ttu-id="550dd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="550dd-111">Return Value</span></span>

<span data-ttu-id="550dd-112">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="550dd-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="550dd-113">In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="550dd-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="550dd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="550dd-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="550dd-115">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="550dd-115">**Minimum supported client**</span></span> | <span data-ttu-id="550dd-116">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="550dd-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="550dd-117">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="550dd-117">**Minimum supported server**</span></span> | <span data-ttu-id="550dd-118">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="550dd-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="550dd-119">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="550dd-119">**Header**</span></span> | <span data-ttu-id="550dd-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="550dd-120">Do.h</span></span> |
