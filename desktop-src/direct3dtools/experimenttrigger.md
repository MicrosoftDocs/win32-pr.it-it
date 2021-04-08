---
description: Rappresenta le informazioni sul trigger dell'esperimento.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura ExperimentTrigger
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876441"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span data-ttu-id="b4447-103"><span id="vspixengine.experimenttrigger"></span>Struttura ExperimentTrigger</span><span class="sxs-lookup"><span data-stu-id="b4447-103"><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger structure</span></span>

<span data-ttu-id="b4447-104">Rappresenta le informazioni sul trigger dell'esperimento.</span><span class="sxs-lookup"><span data-stu-id="b4447-104">Represents experiment trigger information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4447-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4447-105">Syntax</span></span>


```C++
} ExperimentTrigger;
```

## <a name="members"></a><span data-ttu-id="b4447-106">Members</span><span class="sxs-lookup"><span data-stu-id="b4447-106">Members</span></span>

<span data-ttu-id="b4447-107">**type**</span><span class="sxs-lookup"><span data-stu-id="b4447-107">**type**</span></span>  
<span data-ttu-id="b4447-108">Tipo di esperimento (acquisizione) attivato.</span><span class="sxs-lookup"><span data-stu-id="b4447-108">The kind of experiment (capture) triggered.</span></span>

<span data-ttu-id="b4447-109">**key**</span><span class="sxs-lookup"><span data-stu-id="b4447-109">**key**</span></span>  
<span data-ttu-id="b4447-110">Quando il tipo è uguale a EXPERIMENTTRIGGERTYPE:: KEY, la chiave usata per attivare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b4447-110">When type is equal to EXPERIMENTTRIGGERTYPE::KEY, the key used to trigger capture.</span></span>

<span data-ttu-id="b4447-111">**NumeroFrame**</span><span class="sxs-lookup"><span data-stu-id="b4447-111">**frameNumber**</span></span>  
<span data-ttu-id="b4447-112">Quando il tipo è uguale a EXPERIMENTTRIGGERTYPE:: NUMEROFRAME, il numero di frame che attiverà l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b4447-112">When type is equal to EXPERIMENTTRIGGERTYPE::FRAMENUMBER, the frame number that will trigger capture.</span></span>

<span data-ttu-id="b4447-113">**captureCount**</span><span class="sxs-lookup"><span data-stu-id="b4447-113">**captureCount**</span></span>  
<span data-ttu-id="b4447-114">Numero di frame sequenziali da acquisire.</span><span class="sxs-lookup"><span data-stu-id="b4447-114">The number of sequential frames to capture.</span></span>

<span data-ttu-id="b4447-115">**actionIID**</span><span class="sxs-lookup"><span data-stu-id="b4447-115">**actionIID**</span></span>  
<span data-ttu-id="b4447-116">ID dell'evento di azione (screenshot, acquisizione frame e così via).</span><span class="sxs-lookup"><span data-stu-id="b4447-116">The ID of the action event (screenshot, frame capture, etc).</span></span>

<span data-ttu-id="b4447-117">**actionPlayload**</span><span class="sxs-lookup"><span data-stu-id="b4447-117">**actionPlayload**</span></span>  
<span data-ttu-id="b4447-118">Puntatore al payload dell'evento di azione.</span><span class="sxs-lookup"><span data-stu-id="b4447-118">A pointer to the action event payload.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4447-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4447-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b4447-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4447-120">Header</span></span></p></td><td><span data-ttu-id="b4447-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b4447-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



