---
title: Funzione D3DPERF_EndEvent
description: Contrassegna la fine di un evento definito dall'utente. PIX può utilizzare questo evento per attivare un'azione.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104398710"
---
# <a name="d3dperf_endevent-function"></a><span data-ttu-id="ccacb-104">Funzione D3DPERF_EndEvent</span><span class="sxs-lookup"><span data-stu-id="ccacb-104">D3DPERF_EndEvent function</span></span>

<span data-ttu-id="ccacb-105">Contrassegna la fine di un evento definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ccacb-105">Marks the end of a user-defined event.</span></span> <span data-ttu-id="ccacb-106">PIX può utilizzare questo evento per attivare un'azione.</span><span class="sxs-lookup"><span data-stu-id="ccacb-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccacb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccacb-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a><span data-ttu-id="ccacb-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccacb-108">Return value</span></span>

<span data-ttu-id="ccacb-109">Livello della gerarchia in cui l'evento sta per scadere.</span><span class="sxs-lookup"><span data-stu-id="ccacb-109">The level of the hierarchy in which the event is ending.</span></span> <span data-ttu-id="ccacb-110">Se si verifica un errore, questo valore è negativo.</span><span class="sxs-lookup"><span data-stu-id="ccacb-110">If an error occurs, this value is negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccacb-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccacb-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ccacb-112">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="ccacb-112">**Target Platform**</span></span> | <span data-ttu-id="ccacb-113">Windows</span><span class="sxs-lookup"><span data-stu-id="ccacb-113">Windows</span></span> |
| <span data-ttu-id="ccacb-114">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="ccacb-114">**Header**</span></span> | <span data-ttu-id="ccacb-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="ccacb-115">d3d9.h</span></span> |
| <span data-ttu-id="ccacb-116">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="ccacb-116">**Library**</span></span> | <span data-ttu-id="ccacb-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="ccacb-117">d3d9.lib</span></span> |
| <span data-ttu-id="ccacb-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="ccacb-118">**DLL**</span></span> | <span data-ttu-id="ccacb-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="ccacb-119">d3d9.dll</span></span> |