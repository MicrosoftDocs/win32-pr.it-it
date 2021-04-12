---
description: L'API Fibre Channel virtuale Hyper-V definisce gli elementi di programmazione seguenti.
ms.assetid: B63F0660-4731-405B-9828-C57106E685F8
title: Informazioni di riferimento sull'API Fibre Channel virtuale Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b6d46652bacbc012c85e020b76686b9073970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528212"
---
# <a name="hyper-v-virtual-fibre-channel-api-reference"></a><span data-ttu-id="b2853-103">Informazioni di riferimento sull'API Fibre Channel virtuale Hyper-V</span><span class="sxs-lookup"><span data-stu-id="b2853-103">Hyper-V virtual Fibre Channel API reference</span></span>

<span data-ttu-id="b2853-104">L'API Fibre Channel virtuale Hyper-V definisce gli elementi di programmazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="b2853-104">The Hyper-V virtual Fibre Channel API defines the following programming elements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b2853-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b2853-105">In this section</span></span>



| <span data-ttu-id="b2853-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="b2853-106">Topic</span></span>                                                                                    | <span data-ttu-id="b2853-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2853-107">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2853-108">**\_ExternalFcPort MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-108">**Msvm\_ExternalFcPort**</span></span>](msvm-externalfcport.md)<br/>                           | <span data-ttu-id="b2853-109">Rappresenta una porta di Fibre Channel esterna.</span><span class="sxs-lookup"><span data-stu-id="b2853-109">Represents an external Fibre Channel port.</span></span><br/>                                                          |
| [<span data-ttu-id="b2853-110">**\_FcActiveConnection MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-110">**Msvm\_FcActiveConnection**</span></span>](msvm-fcactiveconnection.md)<br/>                   | <span data-ttu-id="b2853-111">Connette una porta di commutazione all'endpoint Fibre Channel a cui è connessa la porta.</span><span class="sxs-lookup"><span data-stu-id="b2853-111">Connects a switch port to the Fibre Channel endpoint to which the port is connected.</span></span><br/>                |
| [<span data-ttu-id="b2853-112">**\_FcDeviceSAPImplementation MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-112">**Msvm\_FcDeviceSAPImplementation**</span></span>](msvm-fcdevicesapimplementation.md)<br/>     | <span data-ttu-id="b2853-113">Rappresenta un'associazione tra un punto di accesso al servizio e il dispositivo logico che lo implementa.</span><span class="sxs-lookup"><span data-stu-id="b2853-113">Represents an association between a service access point and the logical device that implements it.</span></span><br/> |
| [<span data-ttu-id="b2853-114">**\_FcEndpoint MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-114">**Msvm\_FcEndpoint**</span></span>](msvm-fcendpoint.md)<br/>                                   | <span data-ttu-id="b2853-115">Rappresenta il punto di connessione logico per una porta Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="b2853-115">Represents the logical connection point for a Fibre Channel port.</span></span><br/>                                   |
| [<span data-ttu-id="b2853-116">**\_FcPortAllocationSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-116">**Msvm\_FcPortAllocationSettingData**</span></span>](msvm-fcportallocationsettingdata.md)<br/> | <span data-ttu-id="b2853-117">Rappresenta lo stato configurato di una porta Fibre Channel sintetica o di una porta di commutazione Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="b2853-117">Represents the configured state of a synthetic Fibre Channel port or a Fibre Channel switch port.</span></span><br/>   |
| [<span data-ttu-id="b2853-118">**\_FcSwitchPort MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-118">**Msvm\_FcSwitchPort**</span></span>](msvm-fcswitchport.md)<br/>                               | <span data-ttu-id="b2853-119">Rappresenta una porta sull'opzione di Fibre Channel virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2853-119">Represents a port on the virtual Fibre Channel switch.</span></span><br/>                                              |
| [<span data-ttu-id="b2853-120">**\_SyntheticFcPort MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-120">**Msvm\_SyntheticFcPort**</span></span>](msvm-syntheticfcport.md)<br/>                         | <span data-ttu-id="b2853-121">Rappresenta una porta Fibre Channel sintetica.</span><span class="sxs-lookup"><span data-stu-id="b2853-121">Represents a synthetic Fibre Channel port.</span></span><br/>                                                          |
| [<span data-ttu-id="b2853-122">**\_SyntheticFcPortSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-122">**Msvm\_SyntheticFcPortSettingData**</span></span>](msvm-syntheticfcportsettingdata.md)<br/>   | <span data-ttu-id="b2853-123">Rappresenta lo stato configurato di una porta Fibre Channel sintetica.</span><span class="sxs-lookup"><span data-stu-id="b2853-123">Represents the configured state of a synthetic Fibre Channel port.</span></span><br/>                                  |
| [<span data-ttu-id="b2853-124">**\_VirtualFcSwitch MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-124">**Msvm\_VirtualFcSwitch**</span></span>](msvm-virtualfcswitch.md)<br/>                         | <span data-ttu-id="b2853-125">Rappresenta un'opzione di Fibre Channel virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2853-125">Represents a virtual Fibre Channel switch.</span></span><br/>                                                          |
| [<span data-ttu-id="b2853-126">**\_VirtualFcSwitchSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2853-126">**Msvm\_VirtualFcSwitchSettingData**</span></span>](msvm-virtualfcswitchsettingdata.md)<br/>   | <span data-ttu-id="b2853-127">Rappresenta la configurazione di un'opzione di Fibre Channel virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2853-127">Represents the configuration of a virtual Fibre Channel switch.</span></span><br/>                                     |



 

 

 




