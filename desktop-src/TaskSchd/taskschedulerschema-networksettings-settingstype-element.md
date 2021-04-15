---
title: Elemento NetworkSettings (settingsType)
description: Contiene le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete. Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento RunOnlyIfNetworkAvailable è impostato su true.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Utilità di pianificazione elemento NetworkSettings
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477464"
---
# <a name="networksettings-settingstype-element"></a><span data-ttu-id="afc11-105">Elemento NetworkSettings (settingsType)</span><span class="sxs-lookup"><span data-stu-id="afc11-105">NetworkSettings (settingsType) Element</span></span>

<span data-ttu-id="afc11-106">Contiene le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="afc11-106">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="afc11-107">Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="afc11-107">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span>

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="afc11-108">L'elemento **NetworkSettings** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="afc11-108">The **NetworkSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="afc11-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="afc11-109">Parent element</span></span>



| <span data-ttu-id="afc11-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="afc11-110">Element</span></span>                                                                      | <span data-ttu-id="afc11-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="afc11-111">Derived from</span></span>                                                         | <span data-ttu-id="afc11-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afc11-112">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="afc11-113">**Impostazioni (taskType)**</span><span class="sxs-lookup"><span data-stu-id="afc11-113">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="afc11-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="afc11-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="afc11-115">Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="afc11-115">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="afc11-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="afc11-116">Remarks</span></span>

<span data-ttu-id="afc11-117">Per lo sviluppo in C++, vedere [**la proprietà NetworkSettings di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span><span class="sxs-lookup"><span data-stu-id="afc11-117">For C++ development, see [**NetworkSettings Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span></span>

<span data-ttu-id="afc11-118">Per lo sviluppo di script, vedere [**TaskSettings. NetworkSettings**](tasksettings-networksettings.md).</span><span class="sxs-lookup"><span data-stu-id="afc11-118">For script development, see [**TaskSettings.NetworkSettings**](tasksettings-networksettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afc11-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afc11-119">Requirements</span></span>



| <span data-ttu-id="afc11-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc11-120">Requirement</span></span> | <span data-ttu-id="afc11-121">Valore</span><span class="sxs-lookup"><span data-stu-id="afc11-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="afc11-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afc11-122">Minimum supported client</span></span><br/> | <span data-ttu-id="afc11-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afc11-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="afc11-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afc11-124">Minimum supported server</span></span><br/> | <span data-ttu-id="afc11-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="afc11-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





