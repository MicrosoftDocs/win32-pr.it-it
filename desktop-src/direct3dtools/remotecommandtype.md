---
description: Enumerazione utilizzata per la comunicazione tra il motore di acquisizione e un host, ad esempio Visual Studio Diagnostica della grafica.
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione RemoteCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B517F70C-2BFB-42E7-8597-AC5915AB2DE0
api_name:
- RemoteCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63b94ace0818e2057a87c0f3962bb3967843bcfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049036"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span data-ttu-id="b9c2b-103"><span id="vspixengine.remotecommandtype"></span>Enumerazione RemoteCommandType</span><span class="sxs-lookup"><span data-stu-id="b9c2b-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType enumeration</span></span>

<span data-ttu-id="b9c2b-104">Enumerazione utilizzata per la comunicazione tra il motore di acquisizione e un host, ad esempio Visual Studio Diagnostica della grafica.</span><span class="sxs-lookup"><span data-stu-id="b9c2b-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c2b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9c2b-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="b9c2b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="b9c2b-106">Constants</span></span>

<span data-ttu-id="b9c2b-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span><span class="sxs-lookup"><span data-stu-id="b9c2b-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span></span>  
<span data-ttu-id="b9c2b-108">Avvia la comunicazione.</span><span class="sxs-lookup"><span data-stu-id="b9c2b-108">Starts communication.</span></span>

<span data-ttu-id="b9c2b-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span><span class="sxs-lookup"><span data-stu-id="b9c2b-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span></span>  
<span data-ttu-id="b9c2b-110">Avvia una sessione di acquisizione Diagnostica della grafica (un esperimento).</span><span class="sxs-lookup"><span data-stu-id="b9c2b-110">Starts a Graphics Diagnostics capture session (an experiment).</span></span>

<span data-ttu-id="b9c2b-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span><span class="sxs-lookup"><span data-stu-id="b9c2b-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span></span>  
<span data-ttu-id="b9c2b-112">Avvia un'acquisizione (identica alla schermata di stampa).</span><span class="sxs-lookup"><span data-stu-id="b9c2b-112">Starts a capture (same as hitting print screen).</span></span> <span data-ttu-id="b9c2b-113">Inviato da un host durante l'acquisizione di un frame.</span><span class="sxs-lookup"><span data-stu-id="b9c2b-113">Sent by a host when capturing a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9c2b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9c2b-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b9c2b-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9c2b-115">Header</span></span></p></td><td><span data-ttu-id="b9c2b-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b9c2b-116">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



