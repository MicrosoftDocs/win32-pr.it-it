---
description: Il metodo SetDelayTime imposta il tempo di ritardo per la descrizione comando associata all'oggetto MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480588"
---
# <a name="setdelaytime"></a><span data-ttu-id="cac16-103">SetDelayTime</span><span class="sxs-lookup"><span data-stu-id="cac16-103">SetDelayTime</span></span>

> [!Note]  
> <span data-ttu-id="cac16-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cac16-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cac16-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="cac16-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cac16-106">Il `SetDelayTime` metodo imposta il tempo di ritardo per la descrizione comando associata all'oggetto **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="cac16-106">The `SetDelayTime` method sets the delay time for the ToolTip associated with the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a><span data-ttu-id="cac16-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cac16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac16-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span><span class="sxs-lookup"><span data-stu-id="cac16-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span></span>
</dt> <dd>

<span data-ttu-id="cac16-109">Specifica il tipo di ritardo come intero.</span><span class="sxs-lookup"><span data-stu-id="cac16-109">Specifies the type of delay as an Integer.</span></span>



| <span data-ttu-id="cac16-110">Valore</span><span class="sxs-lookup"><span data-stu-id="cac16-110">Value</span></span> | <span data-ttu-id="cac16-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cac16-111">Description</span></span>                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac16-112">-1</span><span class="sxs-lookup"><span data-stu-id="cac16-112">-1</span></span>    | <span data-ttu-id="cac16-113">Per reimpostare il valore predefinito di autopop delay, impostare *iNewVal* su-1.</span><span class="sxs-lookup"><span data-stu-id="cac16-113">To reset the autopop delay time to its default value, set *iNewVal* to -1.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="cac16-114">0</span><span class="sxs-lookup"><span data-stu-id="cac16-114">0</span></span>     | <span data-ttu-id="cac16-115">Imposta il periodo di tempo in cui una finestra della descrizione comando rimane visibile se il puntatore è fermo all'interno del rettangolo di delimitazione di uno strumento.</span><span class="sxs-lookup"><span data-stu-id="cac16-115">Set the length of time a ToolTip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span>                                                                                                                         |
| <span data-ttu-id="cac16-116">1</span><span class="sxs-lookup"><span data-stu-id="cac16-116">1</span></span>     | <span data-ttu-id="cac16-117">Imposta il periodo di tempo in cui un puntatore deve rimanere fermo nel rettangolo di delimitazione di uno strumento prima che venga visualizzata la finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="cac16-117">Set the length of time a pointer must remain stationary within a tool's bounding rectangle before the ToolTip window appears.</span></span>                                                                                                                    |
| <span data-ttu-id="cac16-118">2</span><span class="sxs-lookup"><span data-stu-id="cac16-118">2</span></span>     | <span data-ttu-id="cac16-119">Consente di impostare la quantità di tempo necessaria per la visualizzazione delle finestre di descrizione comando successive quando il puntatore viene spostato da uno strumento all'altro.</span><span class="sxs-lookup"><span data-stu-id="cac16-119">Set the length of time it takes for subsequent ToolTip windows to appear as the pointer moves from one tool to another.</span></span>                                                                                                                          |
| <span data-ttu-id="cac16-120">3</span><span class="sxs-lookup"><span data-stu-id="cac16-120">3</span></span>     | <span data-ttu-id="cac16-121">Imposta tutti i tempi di ritardo sulle proporzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="cac16-121">Set all delay times to default proportions.</span></span> <span data-ttu-id="cac16-122">Il tempo di autopop è dieci volte l'ora iniziale e il tempo di ripresentazione è pari a un quinto del tempo iniziale.</span><span class="sxs-lookup"><span data-stu-id="cac16-122">The autopop time is ten times the initial time and the reshow time is one-fifth the initial time.</span></span> <span data-ttu-id="cac16-123">Se questo flag è impostato, utilizzare un valore positivo di iNewVal per specificare il tempo iniziale, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="cac16-123">If this flag is set, use a positive value of iNewVal to specify the initial time, in milliseconds.</span></span> |



 

</dd> <dt>

<span data-ttu-id="cac16-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span><span class="sxs-lookup"><span data-stu-id="cac16-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span></span>
</dt> <dd>

<span data-ttu-id="cac16-125">Specifica il ritardo, in millisecondi, come intero.</span><span class="sxs-lookup"><span data-stu-id="cac16-125">Specifies the delay, in milliseconds, as an Integer.</span></span>



| <span data-ttu-id="cac16-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cac16-126">Value</span></span>                    | <span data-ttu-id="cac16-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cac16-127">Description</span></span>                                                   |
|--------------------------|---------------------------------------------------------------|
| <span data-ttu-id="cac16-128">-1</span><span class="sxs-lookup"><span data-stu-id="cac16-128">-1</span></span>                       | <span data-ttu-id="cac16-129">Imposta il valore predefinito del ritardo specificato in *iDelayType*</span><span class="sxs-lookup"><span data-stu-id="cac16-129">Sets the delay specified in *iDelayType* to its default value</span></span> |
| <span data-ttu-id="cac16-130">qualsiasi altro valore negativo</span><span class="sxs-lookup"><span data-stu-id="cac16-130">any other negative value</span></span> | <span data-ttu-id="cac16-131">Imposta tutti i tipi di ritardo sul valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="cac16-131">Sets all delay types to their default value.</span></span>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac16-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cac16-132">Return Value</span></span>

<span data-ttu-id="cac16-133">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="cac16-133">No return value.</span></span>

 

 



