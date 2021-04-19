---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Esegue una query dell'agente di orchestrazione universale per determinare se il periodo post-configurazione è stato superato.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320072"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a><span data-ttu-id="0a151-103">Metodo IUniversalOrchestrator:: HasMoratoriumPassed</span><span class="sxs-lookup"><span data-stu-id="0a151-103">IUniversalOrchestrator::HasMoratoriumPassed method</span></span>

> [!NOTE] 
> <span data-ttu-id="0a151-104">Questa API appartiene all'API dell'agente di orchestrazione universale.</span><span class="sxs-lookup"><span data-stu-id="0a151-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="0a151-105">Consente ai client di determinare se l'agente di orchestrazione universale funziona immediatamente dopo l'esperienza predefinita del nuovo dispositivo, il che limita i tentativi di lavoro per ridurre al minimo l'interruzione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0a151-105">Allows clients to determine if Universal Orchestrator is operating immediately after the new device Out of Box Experience, which limits work attempts to minimize user interruption.</span></span> 

## <a name="syntax"></a><span data-ttu-id="0a151-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a151-106">Syntax</span></span>

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a><span data-ttu-id="0a151-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a151-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="0a151-108">Stringa univoca che identifica tutte le chiamate da questo client specifico.</span><span class="sxs-lookup"><span data-stu-id="0a151-108">A unique string that identifies all calls from this specific client.</span></span>

`hasMoratoriumPassed`

<span data-ttu-id="0a151-109">Parametro di output in cui è archiviato il risultato della query.</span><span class="sxs-lookup"><span data-stu-id="0a151-109">Output parameter that stores the result of the query.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a151-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a151-110">Return value</span></span>
<span data-ttu-id="0a151-111">Se questo metodo ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="0a151-111">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="0a151-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a151-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a151-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a151-113">Requirements</span></span>

| <span data-ttu-id="0a151-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a151-114">Requirement</span></span> | <span data-ttu-id="0a151-115">Versione</span><span class="sxs-lookup"><span data-stu-id="0a151-115">Version</span></span> |
|---|---|
| <span data-ttu-id="0a151-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a151-116">Minimum supported client</span></span> | <span data-ttu-id="0a151-117">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="0a151-117">Windows 10 1903</span></span> |
|   |   |



 

 



