---
title: Funzione D3DPERF_BeginEvent
description: Contrassegna l'inizio di un evento definito dall'utente. PIX può utilizzare questo evento per attivare un'azione.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104398708"
---
# <a name="d3dperf_beginevent-function"></a><span data-ttu-id="cb2e5-104">Funzione D3DPERF_BeginEvent</span><span class="sxs-lookup"><span data-stu-id="cb2e5-104">D3DPERF_BeginEvent function</span></span>

<span data-ttu-id="cb2e5-105">Contrassegna l'inizio di un evento definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-105">Marks the beginning of a user-defined event.</span></span> <span data-ttu-id="cb2e5-106">PIX può utilizzare questo evento per attivare un'azione.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb2e5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb2e5-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_BeginEvent(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="cb2e5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb2e5-108">Parameters</span></span>

`col`

<span data-ttu-id="cb2e5-109">Colore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-109">Event color.</span></span> <span data-ttu-id="cb2e5-110">Si tratta del colore per visualizzare l'evento nella visualizzazione evento.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="cb2e5-111">Nome evento.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb2e5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb2e5-112">Return value</span></span>

<span data-ttu-id="cb2e5-113">Il livello in base zero della gerarchia da cui viene avviato l'evento.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-113">The zero-based level of the hierarchy that this event is starting in.</span></span> <span data-ttu-id="cb2e5-114">Se si verifica un errore, il valore restituito sarà negativo.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-114">If an error occurs, the return value will be negative.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb2e5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb2e5-115">Remarks</span></span>

<span data-ttu-id="cb2e5-116">Gli eventi definiti dall'utente raggruppano altri eventi in modo significativo per il programma di destinazione in modo che possano essere rappresentati meglio negli strumenti di profilatura delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-116">User-defined events group together other events in a way that is meaningful to the target program so that they can be better represented in performance profiling tools.</span></span> <span data-ttu-id="cb2e5-117">Ad esempio, un evento di *spazio di disegno* può racchiudere un numero di chiamate Direct3D che gestiscono il disegno di una spaziatura in un gioco.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-117">For example, a *Draw Spaceship* event might bracket a number of Direct3D calls that handle drawing a spaceship in a game.</span></span> <span data-ttu-id="cb2e5-118">Gli eventi possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-118">Events can be nested.</span></span>

<span data-ttu-id="cb2e5-119">Ogni chiamata di **D3DPERF_BeginEvent** deve avere una chiamata **D3DPERF_EndEvent** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-119">Each **D3DPERF_BeginEvent** call should have a matching **D3DPERF_EndEvent** call.</span></span> <span data-ttu-id="cb2e5-120">Gli eventi istantanei, che non sono racchiusi tra altri eventi, devono essere etichettati usando **D3DPERF_SetMarker** anziché **D3DPERF_BeginEvent** e **D3DPERF_EndEvent**.</span><span class="sxs-lookup"><span data-stu-id="cb2e5-120">Instantaneous events (which do not bracket other events) should be labeled by using **D3DPERF_SetMarker** rather than by **D3DPERF_BeginEvent** and **D3DPERF_EndEvent**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb2e5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb2e5-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cb2e5-122">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="cb2e5-122">**Target Platform**</span></span> | <span data-ttu-id="cb2e5-123">Windows</span><span class="sxs-lookup"><span data-stu-id="cb2e5-123">Windows</span></span> |
| <span data-ttu-id="cb2e5-124">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="cb2e5-124">**Header**</span></span> | <span data-ttu-id="cb2e5-125">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="cb2e5-125">d3d9.h</span></span> |
| <span data-ttu-id="cb2e5-126">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="cb2e5-126">**Library**</span></span> | <span data-ttu-id="cb2e5-127">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="cb2e5-127">d3d9.lib</span></span> |
| <span data-ttu-id="cb2e5-128">**DLL**</span><span class="sxs-lookup"><span data-stu-id="cb2e5-128">**DLL**</span></span> | <span data-ttu-id="cb2e5-129">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="cb2e5-129">d3d9.dll</span></span> |