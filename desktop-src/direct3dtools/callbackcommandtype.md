---
description: Enumerazione utilizzata per la comunicazione tra il motore di acquisizione e un host, ad esempio Visual Studio Diagnostica della grafica.
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione CallbackCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 78E0CD6C-5264-4F66-BAB9-20DC9C0C1EC1
api_name:
- CallbackCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ac33267677ae95f6a3d5f893b84d6566e564cddd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124662"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span data-ttu-id="9142f-103"><span id="vspixengine.callbackcommandtype"></span>Enumerazione CallbackCommandType</span><span class="sxs-lookup"><span data-stu-id="9142f-103"><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType enumeration</span></span>

<span data-ttu-id="9142f-104">Enumerazione utilizzata per la comunicazione tra il motore di acquisizione e un host, ad esempio Visual Studio Diagnostica della grafica.</span><span class="sxs-lookup"><span data-stu-id="9142f-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="9142f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9142f-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="9142f-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="9142f-106">Constants</span></span>

<span data-ttu-id="9142f-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span><span class="sxs-lookup"><span data-stu-id="9142f-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span></span>  
<span data-ttu-id="9142f-108">Risultati di BeginCommunication.</span><span class="sxs-lookup"><span data-stu-id="9142f-108">Results from BeginCommunication.</span></span>

<span data-ttu-id="9142f-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span><span class="sxs-lookup"><span data-stu-id="9142f-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span></span>  
<span data-ttu-id="9142f-110">Errori.</span><span class="sxs-lookup"><span data-stu-id="9142f-110">Errors.</span></span>

<span data-ttu-id="9142f-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span><span class="sxs-lookup"><span data-stu-id="9142f-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span></span>  
<span data-ttu-id="9142f-112">Avvisi.</span><span class="sxs-lookup"><span data-stu-id="9142f-112">Warnings.</span></span>

<span data-ttu-id="9142f-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span><span class="sxs-lookup"><span data-stu-id="9142f-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span></span>  
<span data-ttu-id="9142f-114">Messaggi.</span><span class="sxs-lookup"><span data-stu-id="9142f-114">Messages.</span></span>

<span data-ttu-id="9142f-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span><span class="sxs-lookup"><span data-stu-id="9142f-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span></span>  
<span data-ttu-id="9142f-116">Risultato di RunExperiment.</span><span class="sxs-lookup"><span data-stu-id="9142f-116">Result from RunExperiment.</span></span>

<span data-ttu-id="9142f-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span><span class="sxs-lookup"><span data-stu-id="9142f-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span></span>  
<span data-ttu-id="9142f-118">Risultato di RunAction.</span><span class="sxs-lookup"><span data-stu-id="9142f-118">Result from RunAction.</span></span>

<span data-ttu-id="9142f-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="9142f-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span></span>  
<span data-ttu-id="9142f-120">Valore che indica un callback da chiamare quando nuovi frame sono stati acquisiti e pronti per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9142f-120">A value that indicates a callback to be called when new frames have been captured and ready to display.</span></span>

<span data-ttu-id="9142f-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span><span class="sxs-lookup"><span data-stu-id="9142f-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span></span>  
<span data-ttu-id="9142f-122">Risultati di una versione precedente di BeginCommunication usata in Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9142f-122">Results from an older version of BeginCommunication used on Windows 7 and Windows 8.</span></span>

<span data-ttu-id="9142f-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="9142f-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span></span>  
<span data-ttu-id="9142f-124">Risultato di RunExperiementProgress.</span><span class="sxs-lookup"><span data-stu-id="9142f-124">Result from RunExperiementProgress.</span></span>

## <a name="requirements"></a><span data-ttu-id="9142f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9142f-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9142f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9142f-126">Header</span></span></p></td><td><span data-ttu-id="9142f-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9142f-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



