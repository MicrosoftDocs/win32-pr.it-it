---
description: L'eliminazione o la disconnessione di una sessione termina la comunicazione. L'applicazione può inviare le informazioni utente utente al momento della disconnessione, se il provider di servizi lo supporta.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Rilascia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966568"
---
# <a name="drop"></a><span data-ttu-id="bf4ac-104">Rilascia</span><span class="sxs-lookup"><span data-stu-id="bf4ac-104">Drop</span></span>

<span data-ttu-id="bf4ac-105">L'eliminazione o la disconnessione di una sessione termina la comunicazione.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-105">Dropping or disconnecting a session terminates communication.</span></span> <span data-ttu-id="bf4ac-106">L'applicazione può inviare le informazioni utente utente al momento della disconnessione, se il provider di servizi lo supporta.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-106">The application has the option of sending user-user information at the time of the disconnect, if the service provider supports it.</span></span>

<span data-ttu-id="bf4ac-107">I motivi usuali per eliminare una sessione sono che un utente ha richiesto una disconnessione o l'altra estremità della sessione è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-107">The usual reasons for dropping a session is a user has requested a disconnect or the other end of the session has dropped.</span></span> <span data-ttu-id="bf4ac-108">Un'operazione DROP può essere chiamata anche quando TAPI offre una sessione per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-108">A drop operation may also be called when TAPI offers a session to the application.</span></span> <span data-ttu-id="bf4ac-109">Se il provider di servizi supporta questo, l'effetto è che l'applicazione rifiuta la chiamata.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-109">If the service provider supports this, the effect is that the application rejects the call.</span></span>

<span data-ttu-id="bf4ac-110">Quando si richiama un'operazione DROP, le sessioni correlate possono anche essere interessate.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-110">When invoking a drop operation, related sessions can sometimes be affected as well.</span></span> <span data-ttu-id="bf4ac-111">Ad esempio, l'eliminazione di una chiamata di conferenza può eliminare tutti i singoli partecipanti.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-111">For example, dropping a conference call can drop all individual participants.</span></span> <span data-ttu-id="bf4ac-112">I messaggi di modifica dello stato vengono inviati all'applicazione per tutte le chiamate il cui stato è interessato.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-112">State change messages are sent to the application for all calls whose state is affected.</span></span>

<span data-ttu-id="bf4ac-113">In varie configurazioni Bridged o party-line quando più entità si trovano nella chiamata, un'operazione DROP potrebbe non cancellare effettivamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-113">In various bridged or party-line configurations when multiple parties are on the call, a drop operation may not actually clear the call.</span></span> <span data-ttu-id="bf4ac-114">In caso di Bridge, ad esempio, la chiamata potrebbe non essere eliminata perché lo stato di altre stazioni della chiamata può governare.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-114">For example, in a bridged situation, the call may not be dropped because the status of other stations on the call may govern.</span></span> <span data-ttu-id="bf4ac-115">Al contrario, la chiamata può essere semplicemente cambiata nello stato inattivo rimanendo connesso ad altre stazioni.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-115">Instead, the call may simply be changed to the inactive state while remaining connected at other stations.</span></span>

<span data-ttu-id="bf4ac-116">In seguito a un'operazione DROP, l'identificatore di sessione e la maggior parte delle risorse associate alla sessione rimarranno utilizzabili per la maggior parte delle operazioni di query.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-116">Following a drop operation, the session identifier and most resources associated with the session will remain usable for most query operations.</span></span> <span data-ttu-id="bf4ac-117">Quando un'applicazione non richiede più queste risorse, deve [terminare la sessione](terminate-a-session-ovr.md) per evitare perdite di memoria.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-117">When an application no longer requires these resources, it must [terminate the session](terminate-a-session-ovr.md) in order to avoid memory leaks.</span></span>

<span data-ttu-id="bf4ac-118">**TAPI 2. x:** Vedere [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="bf4ac-118">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span></span>

<span data-ttu-id="bf4ac-119">**TAPI 3. x:** Vedere [**ITBasicCallControl::D Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="bf4ac-119">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
