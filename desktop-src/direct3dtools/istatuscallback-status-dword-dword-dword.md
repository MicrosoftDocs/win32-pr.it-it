---
description: Funzione di callback utilizzata per notificare all'host lo stato di avanzamento dei motori. Questa operazione funge anche da metodo per l'host per determinare che il motore è ancora in esecuzione.
title: 'Metodo IStatusCallback:: status'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304294"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span data-ttu-id="eccd2-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Metodo IStatusCallback:: status</span><span class="sxs-lookup"><span data-stu-id="eccd2-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback::Status method</span></span>

<span data-ttu-id="eccd2-105">Funzione di callback utilizzata per notificare all'host lo stato del motore.</span><span class="sxs-lookup"><span data-stu-id="eccd2-105">A callback function used to notify the host of the engine's progress.</span></span> <span data-ttu-id="eccd2-106">Questa operazione funge anche da metodo per l'host per determinare che il motore è ancora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="eccd2-106">This also serves as a way for the host to determine that the engine is still running.</span></span>

## <a name="syntax"></a><span data-ttu-id="eccd2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eccd2-107">Syntax</span></span>


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a><span data-ttu-id="eccd2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eccd2-108">Parameters</span></span>

<span data-ttu-id="eccd2-109">*dwMillisecondsElapsed* </span><span class="sxs-lookup"><span data-stu-id="eccd2-109">*dwMillisecondsElapsed* </span></span>  
<span data-ttu-id="eccd2-110">Tempo trascorso dall'ultima chiamata allo stato, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="eccd2-110">The time elapsed since the last call to Status, in milliseconds.</span></span>

<span data-ttu-id="eccd2-111">*dwFramesCaptured* </span><span class="sxs-lookup"><span data-stu-id="eccd2-111">*dwFramesCaptured* </span></span>  
<span data-ttu-id="eccd2-112">Numero di frame acquisiti dall'ultima chiamata allo stato.</span><span class="sxs-lookup"><span data-stu-id="eccd2-112">The number of frames that have been captures since the last call to Status.</span></span>

<span data-ttu-id="eccd2-113">*dwFramesElapsed* </span><span class="sxs-lookup"><span data-stu-id="eccd2-113">*dwFramesElapsed* </span></span>  
<span data-ttu-id="eccd2-114">Il numero di fotogrammi trascorsi dall'ultima chiamata allo stato.</span><span class="sxs-lookup"><span data-stu-id="eccd2-114">The number of frames elapsed since the last call to Status.</span></span>

## <a name="return-value"></a><span data-ttu-id="eccd2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eccd2-115">Return value</span></span>

<span data-ttu-id="eccd2-116">Se questo metodo ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="eccd2-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="eccd2-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eccd2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eccd2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eccd2-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="eccd2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eccd2-119">Header</span></span></p></td><td><span data-ttu-id="eccd2-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="eccd2-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="eccd2-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="eccd2-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="eccd2-122">**IStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="eccd2-122">**IStatusCallback**</span></span>](/windows/desktop/direct3dtools/istatuscallback)

 

 
