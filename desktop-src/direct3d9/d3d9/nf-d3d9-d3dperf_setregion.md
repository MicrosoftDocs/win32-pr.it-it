---
title: Funzione D3DPERF_SetRegion
description: Contrassegna una serie di frame con il colore e il nome specificati nel file PIXRun. Questa funzione non è attualmente supportata da PIX.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "106299487"
---
# <a name="d3dperf_setregion-function"></a><span data-ttu-id="89da3-104">Funzione D3DPERF_SetRegion</span><span class="sxs-lookup"><span data-stu-id="89da3-104">D3DPERF_SetRegion function</span></span>

<span data-ttu-id="89da3-105">Contrassegna una serie di frame con il colore e il nome specificati nel file PIXRun.</span><span class="sxs-lookup"><span data-stu-id="89da3-105">Mark a series of frames with the specified color and name in the PIXRun file.</span></span> <span data-ttu-id="89da3-106">Questa funzione non è attualmente supportata da PIX.</span><span class="sxs-lookup"><span data-stu-id="89da3-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="89da3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89da3-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="89da3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89da3-108">Parameters</span></span>

`col`

<span data-ttu-id="89da3-109">Colore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="89da3-109">Event color.</span></span> <span data-ttu-id="89da3-110">Si tratta del colore per visualizzare l'evento nella visualizzazione evento.</span><span class="sxs-lookup"><span data-stu-id="89da3-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="89da3-111">Nome evento.</span><span class="sxs-lookup"><span data-stu-id="89da3-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="89da3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89da3-112">Return value</span></span>

<span data-ttu-id="89da3-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="89da3-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89da3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="89da3-114">Remarks</span></span>

<span data-ttu-id="89da3-115">Per semplificare l'analisi, il programma di destinazione può utilizzare il colore per contrassegnare ogni livello di un programma di destinazione.</span><span class="sxs-lookup"><span data-stu-id="89da3-115">To make analysis easier, the target program can use color to mark each level of a target program.</span></span>

## <a name="requirements"></a><span data-ttu-id="89da3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89da3-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="89da3-117">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="89da3-117">**Target Platform**</span></span> | <span data-ttu-id="89da3-118">Windows</span><span class="sxs-lookup"><span data-stu-id="89da3-118">Windows</span></span> |
| <span data-ttu-id="89da3-119">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="89da3-119">**Header**</span></span> | <span data-ttu-id="89da3-120">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="89da3-120">d3d9.h</span></span> |
| <span data-ttu-id="89da3-121">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="89da3-121">**Library**</span></span> | <span data-ttu-id="89da3-122">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="89da3-122">d3d9.lib</span></span> |
| <span data-ttu-id="89da3-123">**DLL**</span><span class="sxs-lookup"><span data-stu-id="89da3-123">**DLL**</span></span> | <span data-ttu-id="89da3-124">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="89da3-124">d3d9.dll</span></span> |