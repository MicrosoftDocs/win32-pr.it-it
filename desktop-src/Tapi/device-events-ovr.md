---
description: TAPI risponde alle modifiche apportate ai dispositivi, ad esempio un telefono che ha avviato la suoneria o un modem che è stato rimosso mediante l'attivazione di eventi del dispositivo.
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: Eventi dispositivo (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f5508e74424a13117facc1c4c370144ecd46de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751626"
---
# <a name="device-events-telephony-api"></a><span data-ttu-id="bd3d4-103">Eventi dispositivo (API di telefonia)</span><span class="sxs-lookup"><span data-stu-id="bd3d4-103">Device Events (Telephony API)</span></span>

<span data-ttu-id="bd3d4-104">TAPI risponde alle modifiche apportate ai dispositivi, ad esempio un telefono che ha avviato la suoneria o un modem che è stato rimosso mediante l'attivazione di eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd3d4-104">TAPI responds to device changes such as a phone that has started ringing or a modem that has been removed by firing device events.</span></span> <span data-ttu-id="bd3d4-105">Un'applicazione TAPI deve rispondere a un evento del dispositivo eseguendo una query per la modifica specifica che si è verificata e quindi intraprendendo un'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="bd3d4-105">A TAPI application should respond to a device event by querying for the specific change that has occurred and then taking appropriate action.</span></span> <span data-ttu-id="bd3d4-106">Un'applicazione può schermare gli eventi che riceveranno tramite la [notifica degli eventi](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="bd3d4-106">An application may screen for events it will receive using [event notification](event-notification.md).</span></span>

<span data-ttu-id="bd3d4-107">**TAPI 2. x:** Le applicazioni ricevono la notifica degli eventi del dispositivo usando il messaggio di [**riga \_ LINEDEVSTATE**](./line-linedevstate.md) .</span><span class="sxs-lookup"><span data-stu-id="bd3d4-107">**TAPI 2.x:** Applications receive notification of device events using the [**LINE\_LINEDEVSTATE**](./line-linedevstate.md) message.</span></span> <span data-ttu-id="bd3d4-108">Lo stato corrente di un indirizzo viene determinato chiamando [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), che restituisce le informazioni in una struttura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="bd3d4-108">The current status of an address is determined by calling [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), which returns its information in a [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="bd3d4-109">Lo stato di un dispositivo a linee aperte specificato viene ottenuto chiamando [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), che restituisce le informazioni in una struttura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="bd3d4-109">The status of a specified open line device is obtained by calling [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), which returns its information in a [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure.</span></span>

<span data-ttu-id="bd3d4-110">**TAPI 3. x:** Le applicazioni ricevono una notifica degli [**\_ eventi di indirizzo**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , che viene elaborata tramite l'interfaccia [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) .</span><span class="sxs-lookup"><span data-stu-id="bd3d4-110">**TAPI 3.x:** Applications receive an [**ADDRESS\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) notification, which is processed using the [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) interface.</span></span> <span data-ttu-id="bd3d4-111">Il [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) può quindi essere usato per ottenere informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="bd3d4-111">The [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) can then be used to acquire more detail information.</span></span>

 

 
