---
title: Funzione D3DPERF_SetOptions
description: Imposta le opzioni del profiler specificate dal programma di destinazione.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104472334"
---
# <a name="d3dperf_setoptions-function"></a><span data-ttu-id="477a0-103">Funzione D3DPERF_SetOptions</span><span class="sxs-lookup"><span data-stu-id="477a0-103">D3DPERF_SetOptions function</span></span>

<span data-ttu-id="477a0-104">Imposta le opzioni del profiler specificate dal programma di destinazione.</span><span class="sxs-lookup"><span data-stu-id="477a0-104">Set profiler options specified by the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="477a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="477a0-105">Syntax</span></span>

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a><span data-ttu-id="477a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="477a0-106">Parameters</span></span>

`dwOptions`

<span data-ttu-id="477a0-107">Opzioni utente riconoscibili da PIX.</span><span class="sxs-lookup"><span data-stu-id="477a0-107">User options recognizable by PIX.</span></span> <span data-ttu-id="477a0-108">Impostare questa impostazione su 1 per notificare a PIX che il programma di destinazione non concede l'autorizzazione per la profilatura.</span><span class="sxs-lookup"><span data-stu-id="477a0-108">Set this to 1 to notify PIX that the target program does not give permission to be profiled.</span></span>

## <a name="return-value"></a><span data-ttu-id="477a0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="477a0-109">Return value</span></span>

<span data-ttu-id="477a0-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="477a0-110">This function doesn't return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="477a0-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="477a0-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="477a0-112">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="477a0-112">**Target Platform**</span></span> | <span data-ttu-id="477a0-113">Windows</span><span class="sxs-lookup"><span data-stu-id="477a0-113">Windows</span></span> |
| <span data-ttu-id="477a0-114">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="477a0-114">**Header**</span></span> | <span data-ttu-id="477a0-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="477a0-115">d3d9.h</span></span> |
| <span data-ttu-id="477a0-116">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="477a0-116">**Library**</span></span> | <span data-ttu-id="477a0-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="477a0-117">d3d9.lib</span></span> |
| <span data-ttu-id="477a0-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="477a0-118">**DLL**</span></span> | <span data-ttu-id="477a0-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="477a0-119">d3d9.dll</span></span> |