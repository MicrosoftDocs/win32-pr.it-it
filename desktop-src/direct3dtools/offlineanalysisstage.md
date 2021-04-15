---
description: Enumerazione utilizzata per indicare le fasi dello stato di avanzamento nell'analisi dei frame.
MS-HAID: vspixengine.OFFLINEANALYSISSTAGE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione OFFLINEANALYSISSTAGE
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85D0288C-113A-4ABE-8EDB-ABB8F009956A
api_name:
- OFFLINEANALYSISSTAGE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf12b70acf70a654fe74b23d4bd3a196467797fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521370"
---
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span data-ttu-id="1d363-103"><span id="vspixengine.offlineanalysisstage"></span>Enumerazione OFFLINEANALYSISSTAGE</span><span class="sxs-lookup"><span data-stu-id="1d363-103"><span id="vspixengine.offlineanalysisstage"></span>OFFLINEANALYSISSTAGE enumeration</span></span>

<span data-ttu-id="1d363-104">Enumerazione utilizzata per indicare le fasi dello stato di avanzamento nell'analisi dei frame.</span><span class="sxs-lookup"><span data-stu-id="1d363-104">An enum used to indicate stages of progress in frame analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d363-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d363-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="1d363-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="1d363-106">Constants</span></span>

<span data-ttu-id="1d363-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**\_NotStarted OfflineAnalysisStage**</span><span class="sxs-lookup"><span data-stu-id="1d363-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage\_NotStarted**</span></span>  
<span data-ttu-id="1d363-108">Analisi del frame non ancora avviata.</span><span class="sxs-lookup"><span data-stu-id="1d363-108">Frame analysis not yet started.</span></span>

<span data-ttu-id="1d363-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**\_Inizializzazione di OfflineAnalysisStage**</span><span class="sxs-lookup"><span data-stu-id="1d363-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**OfflineAnalysisStage\_Initializing**</span></span>  
<span data-ttu-id="1d363-110">Inizializzazione dell'analisi di frame (richiesta rilasciata).</span><span class="sxs-lookup"><span data-stu-id="1d363-110">Frame analysis initializing (request issued).</span></span>

<span data-ttu-id="1d363-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage \_ inizializzazione di \_ LinkOk**</span><span class="sxs-lookup"><span data-stu-id="1d363-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage\_Initializing\_LinkOk**</span></span>  
<span data-ttu-id="1d363-112">Inizializzazione dell'analisi di frame (collegamento stabilita).</span><span class="sxs-lookup"><span data-stu-id="1d363-112">Frame analysis initializing (link established).</span></span>

<span data-ttu-id="1d363-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage \_ inizializzazione di \_ ManifestOk**</span><span class="sxs-lookup"><span data-stu-id="1d363-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage\_Initializing\_ManifestOk**</span></span>  
<span data-ttu-id="1d363-114">Inizializzazione dell'analisi dei frame (il manifesto è stato analizzato correttamente).</span><span class="sxs-lookup"><span data-stu-id="1d363-114">Frame analysis initializing (manifest parsed successfully).</span></span>

<span data-ttu-id="1d363-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage \_ inizializzazione di \_ ToolOk**</span><span class="sxs-lookup"><span data-stu-id="1d363-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage\_Initializing\_ToolOk**</span></span>  
<span data-ttu-id="1d363-116">Inizializzazione dell'analisi dei frame (caricamento dell'analizzatore).</span><span class="sxs-lookup"><span data-stu-id="1d363-116">Frame analysis initializing (analyzer loading).</span></span>

<span data-ttu-id="1d363-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**\_Analisi OfflineAnalysisStage**</span><span class="sxs-lookup"><span data-stu-id="1d363-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage\_Analyzing**</span></span>  
<span data-ttu-id="1d363-118">L'analisi del frame è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1d363-118">Frame analysis is running.</span></span>

<span data-ttu-id="1d363-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**\_AnalysisCompleted OfflineAnalysisStage**</span><span class="sxs-lookup"><span data-stu-id="1d363-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage\_AnalysisCompleted**</span></span>  
<span data-ttu-id="1d363-120">Analisi dei frame completata (evento ' complete ' inviato).</span><span class="sxs-lookup"><span data-stu-id="1d363-120">Frame analysis completed ('complete' event sent).</span></span>

<span data-ttu-id="1d363-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**\_AnalysisCompleted OfflineAnalysisStage \_ riuscito**</span><span class="sxs-lookup"><span data-stu-id="1d363-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage\_AnalysisCompleted\_Successful**</span></span>  
<span data-ttu-id="1d363-122">Analisi del frame completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="1d363-122">Frame analysis completed successfully.</span></span>

<span data-ttu-id="1d363-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ OutputFileExists**</span><span class="sxs-lookup"><span data-stu-id="1d363-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage\_AnalysisCompleted\_OutputFileExists**</span></span>  
<span data-ttu-id="1d363-124">L'analisi del frame è stata completata e il file di output esiste.</span><span class="sxs-lookup"><span data-stu-id="1d363-124">Frame analysis completed and output file exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d363-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d363-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1d363-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d363-126">Header</span></span></p></td><td><span data-ttu-id="1d363-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1d363-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



