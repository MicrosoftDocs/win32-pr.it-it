---
description: Un ID dispositivo è un identificatore indipendente dall'applicazione per un dispositivo di comunicazione specifico.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Identificatore dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529077"
---
# <a name="device-identifier"></a><span data-ttu-id="4313f-103">Identificatore dispositivo</span><span class="sxs-lookup"><span data-stu-id="4313f-103">Device Identifier</span></span>

<span data-ttu-id="4313f-104">Un *ID dispositivo* è un identificatore indipendente dall'applicazione per un dispositivo di comunicazione specifico.</span><span class="sxs-lookup"><span data-stu-id="4313f-104">A *device ID* is an application-independent identifier for a specific communications device.</span></span> <span data-ttu-id="4313f-105">È in genere necessario solo quando un'applicazione TAPI deve passare parte dell'elaborazione che interessa una sessione di comunicazione con le funzioni di un'API diversa.</span><span class="sxs-lookup"><span data-stu-id="4313f-105">It is typically needed only when a TAPI application needs to hand off part of the processing involving in a communications session to the functions of a different API.</span></span> <span data-ttu-id="4313f-106">Ad esempio, le applicazioni TAPI 2,2 potrebbero non essere in grado di accedere direttamente a un flusso multimediale e potrebbero usare l'API Wave.</span><span class="sxs-lookup"><span data-stu-id="4313f-106">For example, TAPI 2.2 applications may be unable to directly access a media stream and might use the Wave API.</span></span>

<span data-ttu-id="4313f-107">**TAPI 2. x:** Vedere [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="4313f-107">**TAPI 2.x:** See [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="4313f-108">**TAPI 3. x:** Vedere [**ITAddressCapabilities:: Get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* impostato sul membro **AC \_ PERMANENTDEVICEID** della [**\_ funzionalità Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span><span class="sxs-lookup"><span data-stu-id="4313f-108">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* set to the **AC\_PERMANENTDEVICEID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span></span>

 

 
