---
title: Elemento NetworkProfileName (settingsType)
description: Contiene il nome di un profilo di rete. Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento RunOnlyIfNetworkAvailable è impostato su true. Il nome viene usato a scopo di visualizzazione.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Utilità di pianificazione elemento NetworkProfileName
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742159"
---
# <a name="networkprofilename-settingstype-element"></a><span data-ttu-id="10329-106">Elemento NetworkProfileName (settingsType)</span><span class="sxs-lookup"><span data-stu-id="10329-106">NetworkProfileName (settingsType) Element</span></span>

<span data-ttu-id="10329-107">Contiene il nome di un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="10329-107">Contains the name of a network profile.</span></span> <span data-ttu-id="10329-108">Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="10329-108">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="10329-109">Il nome viene usato a scopo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="10329-109">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="10329-110">L'elemento **NetworkProfileName** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="10329-110">The **NetworkProfileName** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="10329-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="10329-111">Parent element</span></span>



| <span data-ttu-id="10329-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="10329-112">Element</span></span>                                                                      | <span data-ttu-id="10329-113">Derivato da</span><span class="sxs-lookup"><span data-stu-id="10329-113">Derived from</span></span>                                                         | <span data-ttu-id="10329-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10329-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="10329-115">**Impostazioni (taskType)**</span><span class="sxs-lookup"><span data-stu-id="10329-115">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="10329-116">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="10329-116">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="10329-117">Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="10329-117">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="10329-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10329-118">Requirements</span></span>



| <span data-ttu-id="10329-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="10329-119">Requirement</span></span> | <span data-ttu-id="10329-120">Valore</span><span class="sxs-lookup"><span data-stu-id="10329-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="10329-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10329-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10329-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10329-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="10329-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10329-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10329-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10329-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





