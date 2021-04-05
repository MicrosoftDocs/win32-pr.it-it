---
title: Proprietà TaskSettings. NetworkSettings
description: Per gli script, ottiene o imposta l'oggetto impostazioni di rete che contiene un identificatore e un nome del profilo di rete.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Utilità di pianificazione proprietà NetworkSettings
- Utilità di pianificazione proprietà NetworkSettings, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà NetworkSettings
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740426"
---
# <a name="tasksettingsnetworksettings-property"></a><span data-ttu-id="911b9-106">Proprietà TaskSettings. NetworkSettings</span><span class="sxs-lookup"><span data-stu-id="911b9-106">TaskSettings.NetworkSettings property</span></span>

<span data-ttu-id="911b9-107">Per gli script, ottiene o imposta l'oggetto impostazioni di rete che contiene un identificatore e un nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="911b9-107">For scripting, gets or sets the network settings object that contains a network profile identifier and name.</span></span> <span data-ttu-id="911b9-108">Se la proprietà [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) di [**TaskSettings**](tasksettings.md) è **true** e un propfile di rete viene specificato nella proprietà **NetworkSettings** , l'attività verrà eseguita solo se il profilo di rete specificato è disponibile.</span><span class="sxs-lookup"><span data-stu-id="911b9-108">If the [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) property of [**TaskSettings**](tasksettings.md) is **True** and a network propfile is specified in the **NetworkSettings** property, then the task will run only if the specified network profile is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="911b9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="911b9-109">Syntax</span></span>


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a><span data-ttu-id="911b9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="911b9-110">Property value</span></span>

<span data-ttu-id="911b9-111">Oggetto [**NetworkSettings**](networksettings.md) che contiene un identificatore e un nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="911b9-111">A [**NetworkSettings**](networksettings.md) object that contains a network profile identifier and name.</span></span>

## <a name="requirements"></a><span data-ttu-id="911b9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="911b9-112">Requirements</span></span>



| <span data-ttu-id="911b9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="911b9-113">Requirement</span></span> | <span data-ttu-id="911b9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="911b9-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="911b9-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="911b9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="911b9-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="911b9-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="911b9-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="911b9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="911b9-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="911b9-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="911b9-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="911b9-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="911b9-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="911b9-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="911b9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="911b9-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="911b9-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="911b9-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="911b9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="911b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="911b9-124">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="911b9-124">**TaskSettings**</span></span>](tasksettings.md)
</dt> <dt>

[<span data-ttu-id="911b9-125">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="911b9-125">**NetworkSettings**</span></span>](networksettings.md)
</dt> </dl>

 

 





