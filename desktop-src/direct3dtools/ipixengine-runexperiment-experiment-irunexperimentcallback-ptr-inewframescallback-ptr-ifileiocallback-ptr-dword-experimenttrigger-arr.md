---
description: Esegue un esperimento.
MS-HAID: vspixengine.IPixEngine\_RunExperiment\_Experiment\_IRunExperimentCallback\_ptr\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_DWORD\_ExperimentTrigger\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine:: RunExperiment'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A2EEC278-C074-44B3-94DC-E2D9DC770576
api_name:
- IPixEngine.RunExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c656d57dda496b6c1d8c128dc5e832ec40ef13f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124332"
---
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span data-ttu-id="85613-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>Metodo IPixEngine:: RunExperiment</span><span class="sxs-lookup"><span data-stu-id="85613-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine::RunExperiment method</span></span>

<span data-ttu-id="85613-104">Esegue un esperimento.</span><span class="sxs-lookup"><span data-stu-id="85613-104">Runs an experiment.</span></span>

## <a name="syntax"></a><span data-ttu-id="85613-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85613-105">Syntax</span></span>


```C++
HRESULT RunExperiment(
   Experiment               experiment,
   IRunExperimentCallback * pRequestCallback,
   INewFramesCallback*      callbacks,
   IFileIOCallback*         pFileIOCallback,
   DWORD                    triggersCount,
   ExperimentTrigger []     count4_triggersBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="85613-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85613-106">Parameters</span></span>

<span data-ttu-id="85613-107">*esperimento* </span><span class="sxs-lookup"><span data-stu-id="85613-107">*experiment* </span></span>  
<span data-ttu-id="85613-108">Descrive l'esperimento da eseguire.</span><span class="sxs-lookup"><span data-stu-id="85613-108">Describes the experiment to be run.</span></span>

<span data-ttu-id="85613-109">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="85613-109">*pRequestCallback* </span></span>  
<span data-ttu-id="85613-110">Indirizzo di una funzione utilizzata per notificare all'host che il motore ha avviato l'esperimento.</span><span class="sxs-lookup"><span data-stu-id="85613-110">The address of a function used to notify the host that engine has started the experiment.</span></span>

<span data-ttu-id="85613-111">*callback* </span><span class="sxs-lookup"><span data-stu-id="85613-111">*callbacks* </span></span>  
<span data-ttu-id="85613-112">Indirizzo di una funzione utilizzata per notificare all'host che sono stati acquisiti nuovi frame.</span><span class="sxs-lookup"><span data-stu-id="85613-112">The address of a function used to notify the host that new frames have been captured.</span></span>

<span data-ttu-id="85613-113">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="85613-113">*pFileIOCallback* </span></span>  
<span data-ttu-id="85613-114">Indirizzo di una funzione utilizzata per notificare all'host gli errori di i/o di file durante l'analisi.</span><span class="sxs-lookup"><span data-stu-id="85613-114">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="85613-115">*triggersCount* </span><span class="sxs-lookup"><span data-stu-id="85613-115">*triggersCount* </span></span>  
<span data-ttu-id="85613-116">Il numero di trigger nell'esperimento.</span><span class="sxs-lookup"><span data-stu-id="85613-116">The number of triggers in the experiment.</span></span>

<span data-ttu-id="85613-117">*\_triggersBuffer count4* </span><span class="sxs-lookup"><span data-stu-id="85613-117">*count4\_triggersBuffer* </span></span>  
<span data-ttu-id="85613-118">Trigger di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="85613-118">Capture triggers.</span></span>

## <a name="return-value"></a><span data-ttu-id="85613-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85613-119">Return value</span></span>

<span data-ttu-id="85613-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="85613-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85613-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85613-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="85613-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85613-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="85613-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85613-123">Header</span></span></p></td><td><span data-ttu-id="85613-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="85613-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="85613-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="85613-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="85613-126">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="85613-126">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
