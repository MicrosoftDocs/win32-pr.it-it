---
title: Elemento Name (networkSettingsType)
description: Contiene il nome di un profilo di rete. Il nome viene usato a scopo di visualizzazione.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Utilità di pianificazione elemento Name
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518070"
---
# <a name="name-networksettingstype-element"></a><span data-ttu-id="dfc11-105">Elemento Name (networkSettingsType)</span><span class="sxs-lookup"><span data-stu-id="dfc11-105">Name (networkSettingsType) Element</span></span>

<span data-ttu-id="dfc11-106">Contiene il nome di un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="dfc11-106">Contains the name of a network profile.</span></span> <span data-ttu-id="dfc11-107">Il nome viene usato a scopo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="dfc11-107">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

<span data-ttu-id="dfc11-108">L'elemento **Name** è definito dal tipo complesso [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="dfc11-108">The **Name** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dfc11-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="dfc11-109">Parent element</span></span>



| <span data-ttu-id="dfc11-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="dfc11-110">Element</span></span>                                                                                            | <span data-ttu-id="dfc11-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="dfc11-111">Derived from</span></span>                                                                       | <span data-ttu-id="dfc11-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfc11-112">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfc11-113">**NetworkSettings (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="dfc11-113">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="dfc11-114">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="dfc11-114">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="dfc11-115">Contiene le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="dfc11-115">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="dfc11-116">Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="dfc11-116">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dfc11-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfc11-117">Remarks</span></span>

<span data-ttu-id="dfc11-118">Per lo sviluppo in C++, vedere [**proprietà Name di INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span><span class="sxs-lookup"><span data-stu-id="dfc11-118">For C++ development, see [**Name Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span></span>

<span data-ttu-id="dfc11-119">Per lo sviluppo di script, vedere [**NetworkSettings.Name**](networksettings-name.md).</span><span class="sxs-lookup"><span data-stu-id="dfc11-119">For script development, see [**NetworkSettings.Name**](networksettings-name.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfc11-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfc11-120">Requirements</span></span>



| <span data-ttu-id="dfc11-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfc11-121">Requirement</span></span> | <span data-ttu-id="dfc11-122">Valore</span><span class="sxs-lookup"><span data-stu-id="dfc11-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dfc11-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfc11-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dfc11-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfc11-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dfc11-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfc11-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dfc11-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dfc11-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





