---
title: 'IUniversalOrchestrator:: scheduled'
description: Chiama l'agente di orchestrazione universale per pianificare il lavoro
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320074"
---
# <a name="iuniversalorchestratorschedulework-method"></a><span data-ttu-id="8f67b-103">Metodo IUniversalOrchestrator:: Schedulement</span><span class="sxs-lookup"><span data-stu-id="8f67b-103">IUniversalOrchestrator::ScheduleWork method</span></span>

> [!NOTE] 
> <span data-ttu-id="8f67b-104">Questa API appartiene all'API dell'agente di orchestrazione universale.</span><span class="sxs-lookup"><span data-stu-id="8f67b-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="8f67b-105">Consente ai client di informare l'agente di orchestrazione universale che il lavoro è in sospeso e fornire un file binario che verrà chiamato dall'agente di orchestrazione universale per eseguire il lavoro di aggiornamento in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="8f67b-105">Allows clients to inform Universal Orchestrator that work is pending and provide a binary that will be called by Universal Orchestrator to perform the update work at a later time.</span></span>

<span data-ttu-id="8f67b-106">Il file binario di callback deve essere firmato con un certificato Microsoft valido e il chiamante deve richiamare la chiamata pianificata dal contesto di sistema.</span><span class="sxs-lookup"><span data-stu-id="8f67b-106">The callback binary must be signed with a valid Microsoft certificate, and the caller must be invoking the ScheduleWork call from SYSTEM context.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f67b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f67b-107">Syntax</span></span>

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a><span data-ttu-id="8f67b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f67b-108">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="8f67b-109">Stringa univoca che identifica tutte le chiamate da questo client specifico.</span><span class="sxs-lookup"><span data-stu-id="8f67b-109">A unique string that identifies all calls from this specific client.</span></span>

`cmdLine`

<span data-ttu-id="8f67b-110">Percorso completo del file binario di callback che verrà richiamato dall'agente di orchestrazione universale per eseguire il lavoro.</span><span class="sxs-lookup"><span data-stu-id="8f67b-110">The full path to the callback binary that will be invoked by Universal Orchestrator to perform work.</span></span>

`startArg`

<span data-ttu-id="8f67b-111">Parametri da passare al file binario di callback per indicare che l'avvio è richiesto.</span><span class="sxs-lookup"><span data-stu-id="8f67b-111">Parameters to pass to the callback binary to indicate Start is requested.</span></span>

`pauseArg`

<span data-ttu-id="8f67b-112">*(facoltativo)* Parametri da passare al file binario di callback per indicare che la pausa è richiesta.</span><span class="sxs-lookup"><span data-stu-id="8f67b-112">*(optional)* Parameters to pass to the callback binary to indicate Pause is requested.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f67b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f67b-113">Return value</span></span>
<span data-ttu-id="8f67b-114">Se questo metodo ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="8f67b-114">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="8f67b-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f67b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f67b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f67b-116">Requirements</span></span>

| <span data-ttu-id="8f67b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f67b-117">Requirement</span></span> | <span data-ttu-id="8f67b-118">Versione</span><span class="sxs-lookup"><span data-stu-id="8f67b-118">Version</span></span> |
|---|---|
| <span data-ttu-id="8f67b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f67b-119">Minimum supported client</span></span> | <span data-ttu-id="8f67b-120">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="8f67b-120">Windows 10 1903</span></span> |
|   |   |



 

 



