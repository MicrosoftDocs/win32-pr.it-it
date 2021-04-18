---
description: Per impedire che le chiamate non possedute siano presenti nel sistema di telefonia, TAPI rilascia le chiamate segnalate da un provider di servizi se non è in grado di identificare un'applicazione come proprietario iniziale della chiamata.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Chiamate non possedute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307809"
---
# <a name="unowned-calls"></a><span data-ttu-id="4a65f-103">Chiamate non possedute</span><span class="sxs-lookup"><span data-stu-id="4a65f-103">Unowned Calls</span></span>

<span data-ttu-id="4a65f-104">Per impedire che le chiamate non possedute siano presenti nel sistema di telefonia, TAPI rilascia le chiamate segnalate da un provider di servizi se non è in grado di identificare un'applicazione come proprietario iniziale della chiamata.</span><span class="sxs-lookup"><span data-stu-id="4a65f-104">To prevent unowned calls from being in the telephony system, TAPI drops calls that have been signaled up from a service provider if it cannot identify an application to be the initial owner of the call.</span></span> <span data-ttu-id="4a65f-105">In TAPI versione 2,0 e successive, TAPI chiama la funzione [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) per eliminare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="4a65f-105">In TAPI version 2.0 and later, TAPI calls the [**TSPI\_lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) function to drop the call.</span></span>

<span data-ttu-id="4a65f-106">Il provider di servizi può sapere in anticipo se un'applicazione è disponibile o meno per la proprietà di una nuova chiamata.</span><span class="sxs-lookup"><span data-stu-id="4a65f-106">The service provider can know in advance whether or not there is an application available to take ownership of a new call.</span></span> <span data-ttu-id="4a65f-107">TAPI informa sempre il provider di servizi dei tipi di supporto per i quali è disponibile un'applicazione tramite la funzione [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) .</span><span class="sxs-lookup"><span data-stu-id="4a65f-107">TAPI always informs the service provider of the media types for which there is an application available by using the [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) function.</span></span>

<span data-ttu-id="4a65f-108">Se, ad esempio, un provider di servizi determina la presenza di una chiamata attiva sulla riga con la \_ modalità LINEMEDIAMODE INTERACTIVEVOICE, deve controllare il rilevamento dei supporti predefiniti prima di generare i messaggi della [**riga \_ NEWCALL**](line-newcall.md) e [**\_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4a65f-108">For example, if a service provider determines that there is an active call on the line having LINEMEDIAMODE\_INTERACTIVEVOICE mode, it should check the default media detection before generating the [**LINE\_NEWCALL**](line-newcall.md) and [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages.</span></span> <span data-ttu-id="4a65f-109">Se il rilevamento del supporto predefinito indica che nessuna applicazione sta cercando una \_ chiamata LINEMEDIAMODE INTERACTIVEVOICE, il provider di servizi non deve inviare i messaggi perché TAPI lo eliminerà immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4a65f-109">If the default media detection shows that no application is looking for a LINEMEDIAMODE\_INTERACTIVEVOICE call, the service provider should not send the messages because TAPI will immediately drop it.</span></span>

 

 
