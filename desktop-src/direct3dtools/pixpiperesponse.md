---
description: Enumerazione utilizzata per inviare risposte dal motore di acquisizione a Diagnostica della grafica.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione PixPipeResponse
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09ab253be5e02cc7329195016a406758b7a82e2b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304026"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span data-ttu-id="8fe97-103"><span id="vspixengine.pixpiperesponse"></span>Enumerazione PixPipeResponse</span><span class="sxs-lookup"><span data-stu-id="8fe97-103"><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse enumeration</span></span>

<span data-ttu-id="8fe97-104">Enumerazione utilizzata per inviare risposte dal motore di acquisizione a Diagnostica della grafica.</span><span class="sxs-lookup"><span data-stu-id="8fe97-104">An enum used to send responses from the capture engine to Graphics Diagnostics.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe97-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fe97-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="8fe97-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="8fe97-106">Constants</span></span>

<span data-ttu-id="8fe97-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NUOVI \_ dati \_ disponibili**</span><span class="sxs-lookup"><span data-stu-id="8fe97-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NEW\_DATA\_AVAILABLE**</span></span>  
<span data-ttu-id="8fe97-108">Risposta che indica che i nuovi dati sono stati scritti nel log di grafica ed è pronto per essere letti.</span><span class="sxs-lookup"><span data-stu-id="8fe97-108">A response which indicates that new data has been written to the graphics log and is ready to be read.</span></span>

<span data-ttu-id="8fe97-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**\_dati esperimento**</span><span class="sxs-lookup"><span data-stu-id="8fe97-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**EXPERIMENT\_DATA**</span></span>  
<span data-ttu-id="8fe97-110">Risposta che indica le informazioni di configurazione relative alla sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="8fe97-110">A response which indicates configuration information about the capture session.</span></span>

<span data-ttu-id="8fe97-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span><span class="sxs-lookup"><span data-stu-id="8fe97-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span></span>  
<span data-ttu-id="8fe97-112">Risposta che indica che il motore di acquisizione ha rilevato un errore.</span><span class="sxs-lookup"><span data-stu-id="8fe97-112">A response which indicates that the capture engine has encountered an error.</span></span>

<span data-ttu-id="8fe97-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="8fe97-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span></span>  
<span data-ttu-id="8fe97-114">Risposta che indica che il motore di acquisizione ha avviato l'acquisizione di informazioni grafiche.</span><span class="sxs-lookup"><span data-stu-id="8fe97-114">A response which indicates that the capture engine has started capturing graphics information.</span></span> <span data-ttu-id="8fe97-115">Questa operazione non indica che i dati sono ancora disponibili per essere esaminati.</span><span class="sxs-lookup"><span data-stu-id="8fe97-115">This does not indicate that data is available to be examined yet.</span></span>

<span data-ttu-id="8fe97-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**dati PARZIALi \_**</span><span class="sxs-lookup"><span data-stu-id="8fe97-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**PARTIAL\_DATA**</span></span>  
<span data-ttu-id="8fe97-117">Risposta che indica che i dati parziali sono stati scritti nel log di grafica.</span><span class="sxs-lookup"><span data-stu-id="8fe97-117">A response which indicates that partial data has been written to the graphics log.</span></span>

<span data-ttu-id="8fe97-118"><span id="READY"></span><span id="ready"></span>**PRONTO**</span><span class="sxs-lookup"><span data-stu-id="8fe97-118"><span id="READY"></span><span id="ready"></span>**READY**</span></span>  
<span data-ttu-id="8fe97-119">Risposta che indica che il motore di acquisizione è pronto per iniziare ad acquisire le informazioni grafiche.</span><span class="sxs-lookup"><span data-stu-id="8fe97-119">A response which indicates that the capture engine is ready to start capturing graphics information.</span></span>

<span data-ttu-id="8fe97-120"><span id="DONE"></span><span id="done"></span>**ESEGUITA**</span><span class="sxs-lookup"><span data-stu-id="8fe97-120"><span id="DONE"></span><span id="done"></span>**DONE**</span></span>  
<span data-ttu-id="8fe97-121">Interno</span><span class="sxs-lookup"><span data-stu-id="8fe97-121">Internal</span></span>

<span data-ttu-id="8fe97-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span><span class="sxs-lookup"><span data-stu-id="8fe97-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span></span>  
<span data-ttu-id="8fe97-123">Risposta che indica che è stata avviata un'acquisizione di frame.</span><span class="sxs-lookup"><span data-stu-id="8fe97-123">A response which indicates that a frame capture has started.</span></span>

<span data-ttu-id="8fe97-124"><span id="STATUS"></span><span id="status"></span>**STATO**</span><span class="sxs-lookup"><span data-stu-id="8fe97-124"><span id="STATUS"></span><span id="status"></span>**STATUS**</span></span>  
<span data-ttu-id="8fe97-125">Risposta che indica le informazioni sullo stato relative all'app acquisita; ad esempio, framerate.</span><span class="sxs-lookup"><span data-stu-id="8fe97-125">A response which indicates status information about the app being captured; for example, framerate.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe97-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fe97-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8fe97-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fe97-127">Header</span></span></p></td><td><span data-ttu-id="8fe97-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8fe97-128">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



