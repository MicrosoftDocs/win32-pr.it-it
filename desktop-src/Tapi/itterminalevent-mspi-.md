---
description: "Quando il metodo ITTAPIEventNotification:: Event restituisce \\_ un evento TAPI uguale al \\_ terminale te, i metodi esposti dall'interfaccia ITTerminalEvent possono essere utilizzati per recuperare le informazioni relative all'evento terminale che si è verificato, se è presente un MSP."
ms.assetid: 5277776e-0471-41b6-b662-4346a9d237ec
title: ITTerminalEvent (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593b9a7d048db9843825ccde8b22d0585a0c07fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315278"
---
# <a name="itterminalevent-mspi"></a><span data-ttu-id="089c3-103">ITTerminalEvent (MSPI)</span><span class="sxs-lookup"><span data-stu-id="089c3-103">ITTerminalEvent (MSPI)</span></span>

<span data-ttu-id="089c3-104">Quando il metodo [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) restituisce [**un \_ evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) uguale **al \_ terminale te**, i metodi esposti dall'interfaccia **ITTerminalEvent** possono essere utilizzati per recuperare le informazioni relative all'evento terminale che si è verificato, se è presente un MSP.</span><span class="sxs-lookup"><span data-stu-id="089c3-104">When the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method returns [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_TERMINAL**, the methods exposed by the **ITTerminalEvent** interface can be used to retrieve information concerning the terminal event that has occurred, if an MSP exists.</span></span>

<span data-ttu-id="089c3-105">L'interfaccia **ITTerminalEvent** viene implementata da un MSP e non è disponibile se non è presente alcun provider di servizi multimediali associato all'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="089c3-105">The **ITTerminalEvent** interface is implemented by an MSP and is not available if there is no media service provider associated with the address.</span></span> <span data-ttu-id="089c3-106">Per informazioni dettagliate su questa interfaccia, vedere **ITTerminalEvent** nella sezione interfaccia msp.</span><span class="sxs-lookup"><span data-stu-id="089c3-106">Please see **ITTerminalEvent** in the MSP Interface section for details on this interface.</span></span>

 

 



