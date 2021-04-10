---
title: Elemento ID (networkSettingsType)
description: Contiene un valore GUID che identifica un profilo di rete.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Utilità di pianificazione elemento ID
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121563"
---
# <a name="id-networksettingstype-element"></a><span data-ttu-id="6f349-104">Elemento ID (networkSettingsType)</span><span class="sxs-lookup"><span data-stu-id="6f349-104">Id (networkSettingsType) Element</span></span>

<span data-ttu-id="6f349-105">Contiene un valore GUID che identifica un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="6f349-105">Contains a GUID value that identifies a network profile.</span></span>

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

<span data-ttu-id="6f349-106">L'elemento **ID** è definito dal tipo complesso [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6f349-106">The **Id** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6f349-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="6f349-107">Parent element</span></span>



| <span data-ttu-id="6f349-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6f349-108">Element</span></span>                                                                                            | <span data-ttu-id="6f349-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="6f349-109">Derived from</span></span>                                                                       | <span data-ttu-id="6f349-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f349-110">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f349-111">**NetworkSettings (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="6f349-111">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="6f349-112">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="6f349-112">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="6f349-113">Contiene le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="6f349-113">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="6f349-114">Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="6f349-114">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6f349-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f349-115">Remarks</span></span>

<span data-ttu-id="6f349-116">Per lo sviluppo in C++, vedere [**la proprietà ID di INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span><span class="sxs-lookup"><span data-stu-id="6f349-116">For C++ development, see [**Id Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span></span>

<span data-ttu-id="6f349-117">Per lo sviluppo di script, vedere [**NetworkSettings.ID**](networksettings-id.md).</span><span class="sxs-lookup"><span data-stu-id="6f349-117">For script development, see [**NetworkSettings.Id**](networksettings-id.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f349-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f349-118">Requirements</span></span>



| <span data-ttu-id="6f349-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f349-119">Requirement</span></span> | <span data-ttu-id="6f349-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6f349-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6f349-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f349-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6f349-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f349-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6f349-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f349-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6f349-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f349-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





