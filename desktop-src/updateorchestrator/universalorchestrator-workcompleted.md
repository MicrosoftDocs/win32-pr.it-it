---
title: IUniversalOrchestrator::WorkCompleted
description: Chiama l'agente di orchestrazione universale per indicare che il lavoro è completato
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320075"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a><span data-ttu-id="bd996-103">Metodo IUniversalOrchestrator:: WorkCompleted</span><span class="sxs-lookup"><span data-stu-id="bd996-103">IUniversalOrchestrator::WorkCompleted method</span></span>

> [!NOTE] 
> <span data-ttu-id="bd996-104">Questa API appartiene all'API dell'agente di orchestrazione universale.</span><span class="sxs-lookup"><span data-stu-id="bd996-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="bd996-105">Consente ai client di informare l'agente di orchestrazione universale che il lavoro pianificato in precedenza è stato completato e arrestare i callback per eseguire il lavoro fino alla successiva chiamata pianificata.</span><span class="sxs-lookup"><span data-stu-id="bd996-105">Allows clients to inform Universal Orchestrator that the previously scheduled work has been completed and stop callbacks to perform work until the next successful ScheduleWork call.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd996-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd996-106">Syntax</span></span>

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a><span data-ttu-id="bd996-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd996-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="bd996-108">Stringa univoca che identifica tutte le chiamate da questo client specifico.</span><span class="sxs-lookup"><span data-stu-id="bd996-108">A unique string that identifies all calls from this specific client.</span></span>

`workCompleted`

<span data-ttu-id="bd996-109">**True** se il lavoro è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="bd996-109">**TRUE** if the work successfully completed.</span></span> <span data-ttu-id="bd996-110">In caso contrario, **false** se il tentativo di lavoro ha avuto esito negativo e deve essere ritentato in futuro.</span><span class="sxs-lookup"><span data-stu-id="bd996-110">Otherwise, **FALSE** if the work attempt failed and should be retried in the future.</span></span> 

## <a name="return-value"></a><span data-ttu-id="bd996-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd996-111">Return value</span></span>
<span data-ttu-id="bd996-112">Se questo metodo ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="bd996-112">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="bd996-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd996-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd996-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd996-114">Requirements</span></span>

| <span data-ttu-id="bd996-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd996-115">Requirement</span></span> | <span data-ttu-id="bd996-116">Versione</span><span class="sxs-lookup"><span data-stu-id="bd996-116">Version</span></span> |
|---|---|
| <span data-ttu-id="bd996-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd996-117">Minimum supported client</span></span> | <span data-ttu-id="bd996-118">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="bd996-118">Windows 10 1903</span></span> |
|   |   |



 

 



