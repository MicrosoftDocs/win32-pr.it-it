---
title: Funzione D3DPERF_SetMarker
description: Contrassegnare un evento istantaneo. PIX può utilizzare questo evento per attivare un'azione.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104398709"
---
# <a name="d3dperf_setmarker-function"></a><span data-ttu-id="c3dbe-104">Funzione D3DPERF_SetMarker</span><span class="sxs-lookup"><span data-stu-id="c3dbe-104">D3DPERF_SetMarker function</span></span>

<span data-ttu-id="c3dbe-105">Contrassegnare un evento istantaneo.</span><span class="sxs-lookup"><span data-stu-id="c3dbe-105">Mark an instantaneous event.</span></span> <span data-ttu-id="c3dbe-106">PIX può utilizzare questo evento per attivare un'azione.</span><span class="sxs-lookup"><span data-stu-id="c3dbe-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3dbe-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3dbe-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetMarker(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="c3dbe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3dbe-108">Parameters</span></span>

`col`

<span data-ttu-id="c3dbe-109">Colore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c3dbe-109">Event color.</span></span> <span data-ttu-id="c3dbe-110">Si tratta del colore per visualizzare l'evento nella visualizzazione evento.</span><span class="sxs-lookup"><span data-stu-id="c3dbe-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="c3dbe-111">Nome evento.</span><span class="sxs-lookup"><span data-stu-id="c3dbe-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3dbe-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3dbe-112">Return value</span></span>

<span data-ttu-id="c3dbe-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c3dbe-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3dbe-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3dbe-114">Remarks</span></span>

<span data-ttu-id="c3dbe-115">Gli eventi utente istantanei non racchiudono né raggruppano altri eventi.</span><span class="sxs-lookup"><span data-stu-id="c3dbe-115">Instantaneous user events do not bracket or group other events.</span></span> <span data-ttu-id="c3dbe-116">Ad esempio, quando l'utente genera un'arma in un gioco, è possibile creare un evento *shot generato* da una chiamata **D3DPERF_SetMarker** .</span><span class="sxs-lookup"><span data-stu-id="c3dbe-116">For example, when the user fires a weapon in a game, a *Shot Fired* event could be created by a **D3DPERF_SetMarker** call.</span></span> <span data-ttu-id="c3dbe-117">Per raggruppare più eventi con un unico nome definito dall'utente, usare **D3DPERF_BeginEvent** e **D3DPERF_EndEvent** invece di **D3DPERF_SetMarker**.</span><span class="sxs-lookup"><span data-stu-id="c3dbe-117">To group together multiple events under a single, user-defined name, use **D3DPERF_BeginEvent** and **D3DPERF_EndEvent** rather than **D3DPERF_SetMarker**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3dbe-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3dbe-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c3dbe-119">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="c3dbe-119">**Target Platform**</span></span> | <span data-ttu-id="c3dbe-120">Windows</span><span class="sxs-lookup"><span data-stu-id="c3dbe-120">Windows</span></span> |
| <span data-ttu-id="c3dbe-121">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="c3dbe-121">**Header**</span></span> | <span data-ttu-id="c3dbe-122">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="c3dbe-122">d3d9.h</span></span> |
| <span data-ttu-id="c3dbe-123">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="c3dbe-123">**Library**</span></span> | <span data-ttu-id="c3dbe-124">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="c3dbe-124">d3d9.lib</span></span> |
| <span data-ttu-id="c3dbe-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="c3dbe-125">**DLL**</span></span> | <span data-ttu-id="c3dbe-126">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="c3dbe-126">d3d9.dll</span></span> |