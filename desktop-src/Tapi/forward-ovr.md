---
description: L'invio è la deviazione di una sessione in ingresso a un indirizzo di destinazione diverso.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Inoltra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879262"
---
# <a name="forward"></a><span data-ttu-id="9a6b5-103">Inoltra</span><span class="sxs-lookup"><span data-stu-id="9a6b5-103">Forward</span></span>

<span data-ttu-id="9a6b5-104">L'invio è la deviazione di una sessione in ingresso a un indirizzo di destinazione diverso.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-104">Forwarding is the deflection of an incoming session to a different destination address.</span></span> <span data-ttu-id="9a6b5-105">TAPI consente a un'applicazione di specificare un elenco di condizioni di invio per un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-105">TAPI allows an application to specify a list of forwarding conditions for an address.</span></span> <span data-ttu-id="9a6b5-106">Le condizioni di inoltri possono essere con granularità fine come una destinazione e una [**modalità di invio**](./lineforwardmode--constants.md) diverse per ogni indirizzo del chiamante.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-106">Forwarding conditions can be as finely grained as a different destination and [**forwarding mode**](./lineforwardmode--constants.md) for each caller address.</span></span>

<span data-ttu-id="9a6b5-107">L'operazione di invio può essere usata anche per implementare una funzionalità selettiva di non disturbo, tramite l'invio di alcuni chiamanti alla posta vocale e consentire ad altri di provare il completamento.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-107">The forwarding operation can also be used to implement a selective do-not-disturb feature, by forwarding some callers to voice mail and allowing others to attempt completion.</span></span>

<span data-ttu-id="9a6b5-108">L'operazione di invio può inoltre annullare eventuali inoltri attualmente in vigore.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-108">The forwarding operation can also cancel any forwarding currently in effect.</span></span>

<span data-ttu-id="9a6b5-109">Alcuni provider di servizi richiedono che un'applicazione crei una chiamata di consultazione prima di un'operazione di invio.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-109">Some service providers require that an application create a consultation call prior to a forwarding operation.</span></span> <span data-ttu-id="9a6b5-110">All'operazione di invio viene quindi passato un puntatore alla chiamata di consultazione.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-110">The forwarding operation is then passed a pointer to the consultation call.</span></span>

<span data-ttu-id="9a6b5-111">Non tutti i provider di servizi supportano l'utilizzo di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-111">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="9a6b5-112">**TAPI 2. x:** Per impostare [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) in modo da ottenere [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), modificare il messaggio di notifica della [**riga \_ ADDRESSSTATE**](./line-addressstate.md) con LINEADDRESSSTATE \_ in futuro.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-112">**TAPI 2.x:** To set [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) to get [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), change the [**LINE\_ADDRESSSTATE**](./line-addressstate.md) notification message with LINEADDRESSSTATE\_FORWARD.</span></span>

<span data-ttu-id="9a6b5-113">**TAPI 3. x:** Vedere [**ITAddress:: inoltr**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress:: Get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), Change Notification: [**ITADDRESSEVENT:: Get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) con AE \_ in futuro.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-113">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get\_CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), change notification: [**ITAddressEvent::get\_Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE\_FORWARD.</span></span>

> [!Note]  
> <span data-ttu-id="9a6b5-114">Potrebbe non essere possibile per un provider di servizi conoscere sempre l'avanzamento per un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-114">It may be impossible for a service provider to know at all times what forwarding is in effect for an address.</span></span> <span data-ttu-id="9a6b5-115">L'invio può essere annullato o modificato in modo che non comporti notifiche al provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="9a6b5-115">Forwarding can be canceled or changed in ways that do not result in notification to the service provider.</span></span>

 

 

 
