---
title: Proprietà SystemMonitor. ReadOnly
description: Recupera o imposta un valore che determina se un utente può modificare i valori delle proprietà del controllo.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Proprietà di sola lettura SysMon
- Proprietà ReadOnly SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà ReadOnly
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964179"
---
# <a name="systemmonitorreadonly-property"></a><span data-ttu-id="b49be-106">Proprietà SystemMonitor. ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b49be-106">SystemMonitor.ReadOnly property</span></span>

<span data-ttu-id="b49be-107">Recupera o imposta un valore che determina se un utente può modificare i valori delle proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="b49be-107">Retrieves or sets a value that determines whether a user can modify the property values of the control.</span></span>

<span data-ttu-id="b49be-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b49be-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b49be-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b49be-109">Syntax</span></span>


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b49be-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b49be-110">Property value</span></span>

<span data-ttu-id="b49be-111">True se non si desidera che l'utente modifichi i valori delle proprietà del controllo; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="b49be-111">True if you do not want the user to modify the property values of the control; otherwise, false.</span></span> <span data-ttu-id="b49be-112">Il valore predefinito è false, ovvero gli utenti possono modificare i valori delle proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="b49be-112">The default value is false, meaning that users can modify the property values of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b49be-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b49be-113">Remarks</span></span>

<span data-ttu-id="b49be-114">Quando il valore di questa proprietà è true, vengono applicate le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b49be-114">When the value of this property is True, the following conditions are in effect:</span></span>

-   <span data-ttu-id="b49be-115">L'utente non può utilizzare il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="b49be-115">The user cannot use the context menu.</span></span>
-   <span data-ttu-id="b49be-116">I seguenti pulsanti della barra degli strumenti sono disabilitati:</span><span class="sxs-lookup"><span data-stu-id="b49be-116">The following toolbar buttons are disabled:</span></span>
    -   <span data-ttu-id="b49be-117">Nuovo insieme di contatori</span><span class="sxs-lookup"><span data-stu-id="b49be-117">New Counter Set</span></span>
    -   <span data-ttu-id="b49be-118">Visualizza attività corrente</span><span class="sxs-lookup"><span data-stu-id="b49be-118">View Current Activity</span></span>
    -   <span data-ttu-id="b49be-119">Visualizzazione dei dati dei file di log</span><span class="sxs-lookup"><span data-stu-id="b49be-119">View Log File Data</span></span>
    -   <span data-ttu-id="b49be-120">Add</span><span class="sxs-lookup"><span data-stu-id="b49be-120">Add</span></span>
    -   <span data-ttu-id="b49be-121">Delete</span><span class="sxs-lookup"><span data-stu-id="b49be-121">Delete</span></span>
    -   <span data-ttu-id="b49be-122">Incolla elenco contatori</span><span class="sxs-lookup"><span data-stu-id="b49be-122">Paste Counter List</span></span>
    -   <span data-ttu-id="b49be-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b49be-123">Properties</span></span>

<span data-ttu-id="b49be-124">Si noti che questa proprietà ha effetto solo sulla capacità dell'utente di modificare i valori delle proprietà tramite l'interfaccia utente, ma non impedisce di modificare a livello di codice i valori delle proprietà o i contatori.</span><span class="sxs-lookup"><span data-stu-id="b49be-124">Note that this property affects only the user's ability to modify property values through the user interface, it does not prevent you from programmatically modifying property values or counters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49be-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b49be-125">Requirements</span></span>



| <span data-ttu-id="b49be-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b49be-126">Requirement</span></span> | <span data-ttu-id="b49be-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b49be-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b49be-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b49be-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b49be-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b49be-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b49be-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b49be-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b49be-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b49be-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b49be-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b49be-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b49be-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b49be-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b49be-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b49be-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b49be-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="b49be-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





