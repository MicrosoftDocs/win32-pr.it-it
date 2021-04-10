---
description: TSPI include una serie di operazioni che avviano la durata di un handle di chiamata.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Risposte asincrone rispetto agli eventi sui nuovi handle di chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883246"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a><span data-ttu-id="d0fb1-103">Risposte asincrone rispetto agli eventi sui nuovi handle di chiamata</span><span class="sxs-lookup"><span data-stu-id="d0fb1-103">Async Replies versus Events on New Call Handles</span></span>

<span data-ttu-id="d0fb1-104">TSPI include una serie di operazioni che avviano la durata di un handle di chiamata.</span><span class="sxs-lookup"><span data-stu-id="d0fb1-104">TSPI includes a number of operations that start the lifetime of a call handle.</span></span> <span data-ttu-id="d0fb1-105">Se il provider di servizi restituisce l'ESITo positivo di tale operazione, deve compilare l'handle opaco di tipo **HDRVCALL**, che usa per la nuova chiamata prima che venga restituito.</span><span class="sxs-lookup"><span data-stu-id="d0fb1-105">If the service provider returns SUCCESS for such an operation, it must fill in the opaque handle of type **HDRVCALL**, which it uses for the new call before it returns.</span></span> <span data-ttu-id="d0fb1-106">TAPI non esegue mai operazioni sulla chiamata prima della ricezione [*del \_ processo di completamento*](/windows/win32/api/tspi/nc-tspi-async_completion) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d0fb1-106">TAPI never performs operations on the call before the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) has been received.</span></span> <span data-ttu-id="d0fb1-107">Se il provider di servizi restituisce un errore, l'handle diventa automaticamente non valido (ovvero senza [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span><span class="sxs-lookup"><span data-stu-id="d0fb1-107">If the service provider returns FAILURE, the handle automatically becomes invalid (that is, without [**TSPI\_lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span></span> <span data-ttu-id="d0fb1-108">In pratica, TAPI considera l'handle come "non ancora valido" fino al completamento asincrono.</span><span class="sxs-lookup"><span data-stu-id="d0fb1-108">In effect, TAPI treats the handle as "not yet valid" until the asynchronous completion.</span></span>

<span data-ttu-id="d0fb1-109">Il provider di servizi deve anche considerare l'handle come "non ancora valido" fino a quando non viene ricevuta la procedura di [*completamento \_*](/windows/win32/api/tspi/nc-tspi-async_completion) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d0fb1-109">The service provider must also treat the handle as "not yet valid" until after the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) is received.</span></span> <span data-ttu-id="d0fb1-110">In altre parole, non deve eseguire alcuna funzione [*di \_ evento line*](/windows/win32/api/tspi/nc-tspi-lineevent) per la nuova chiamata o includerla nei conteggi delle chiamate nei messaggi o nelle strutture dei dati di stato per la riga.</span><span class="sxs-lookup"><span data-stu-id="d0fb1-110">In other words, it must not issue any [*Line\_Event*](/windows/win32/api/tspi/nc-tspi-lineevent) functions for the new call or include it in call counts in messages or status data structures for the line.</span></span>

<span data-ttu-id="d0fb1-111">Il livello TAPI è conforme anche a queste restrizioni del ciclo di vita; un nuovo handle di chiamata non viene restituito né valido fino a quando non viene inviato il messaggio di [**\_ risposta alla riga**](./line-reply.md) corrispondente e nessun evento per la nuova chiamata viene recapitato all'applicazione fino al termine del messaggio di risposta della riga \_ .</span><span class="sxs-lookup"><span data-stu-id="d0fb1-111">The TAPI level also conforms to these life cycle restrictions; a new call handle is not returned or valid until the matching [**LINE\_REPLY**](./line-reply.md) message, and no events for the new call are delivered to the application until after the LINE\_REPLY message.</span></span>

<span data-ttu-id="d0fb1-112">Di seguito sono riportate le operazioni TSPI a cui si applica questo principio di "durata iniziale":</span><span class="sxs-lookup"><span data-stu-id="d0fb1-112">The TSPI operations to which this "start lifetime" principle applies are the following:</span></span>

-   [<span data-ttu-id="d0fb1-113">**\_LINECOMPLETETRANSFER TSPI**</span><span class="sxs-lookup"><span data-stu-id="d0fb1-113">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="d0fb1-114">**\_LINEFORWARD TSPI**</span><span class="sxs-lookup"><span data-stu-id="d0fb1-114">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="d0fb1-115">**\_LINEMAKECALL TSPI**</span><span class="sxs-lookup"><span data-stu-id="d0fb1-115">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="d0fb1-116">**\_LINEPICKUP TSPI**</span><span class="sxs-lookup"><span data-stu-id="d0fb1-116">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="d0fb1-117">**\_LINEPREPAREADDTOCONFERENCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="d0fb1-117">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="d0fb1-118">**\_LINESETUPCONFERENCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="d0fb1-118">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="d0fb1-119">**\_LINESETUPTRANSFER TSPI**</span><span class="sxs-lookup"><span data-stu-id="d0fb1-119">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="d0fb1-120">**\_LINEUNPARK TSPI**</span><span class="sxs-lookup"><span data-stu-id="d0fb1-120">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
