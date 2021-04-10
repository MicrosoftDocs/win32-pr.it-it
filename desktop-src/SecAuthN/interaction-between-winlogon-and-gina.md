---
description: Winlogon e GINA devono comunicare le informazioni di inizializzazione, gestire il monitoraggio e la notifica di Secure Attention Sequence (SAS) e consentire attività di disconnessione e arresto.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interazione tra Winlogon e GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058139"
---
# <a name="interaction-between-winlogon-and-gina"></a><span data-ttu-id="6dcf5-103">Interazione tra Winlogon e GINA </span><span class="sxs-lookup"><span data-stu-id="6dcf5-103">Interaction Between Winlogon and GINA</span></span>

<span data-ttu-id="6dcf5-104">[*Winlogon*](../secgloss/w-gly.md) e [*Gina*](../secgloss/g-gly.md) devono comunicare le informazioni di inizializzazione, gestire il monitoraggio e la notifica di [*Secure Attention Sequence*](../secgloss/s-gly.md) (SAS) e consentire attività di disconnessione e arresto.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-104">[*Winlogon*](../secgloss/w-gly.md) and the [*GINA*](../secgloss/g-gly.md) must communicate initialization information, handle [*secure attention sequence*](../secgloss/s-gly.md) (SAS) monitoring and notification, and permit logoff and shutdown activities.</span></span> <span data-ttu-id="6dcf5-105">Lo stato di Winlogon determina quale funzione GINA viene chiamata per elaborare qualsiasi evento SAS specificato.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-105">The state of Winlogon determines which GINA function is called to process any given SAS event.</span></span> <span data-ttu-id="6dcf5-106">Le comunicazioni si verificano nell'ordine indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-106">Communications occur in the order shown here.</span></span>

> [!Note]  
> <span data-ttu-id="6dcf5-107">Le DLL GINA vengono ignorate in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-107">GINA DLLs are ignored in Windows Vista.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dcf5-108">Event</span><span class="sxs-lookup"><span data-stu-id="6dcf5-108">Event</span></span></th>
<th><span data-ttu-id="6dcf5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dcf5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dcf5-110">Avvio workstation</span><span class="sxs-lookup"><span data-stu-id="6dcf5-110">Workstation boot</span></span></td>
<td><ol>
<li><span data-ttu-id="6dcf5-111">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> di Gina per notificare a Gina la versione di Winlogon in uso.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-111">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> function to notify the GINA about the version of Winlogon in use.</span></span></li>
<li><span data-ttu-id="6dcf5-112">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> di Gina per fornire a Gina gli indirizzi delle funzioni di supporto, un handle a Winlogon e per ottenere le informazioni di <a href="/windows/desktop/SecGloss/c-gly"><em>contesto</em></a> per Gina (da usare in tutte le chiamate future a Gina).</span><span class="sxs-lookup"><span data-stu-id="6dcf5-112">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> function to give the GINA the addresses of the support functions, a handle to Winlogon, and to obtain the <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> information for the GINA (to be used in all future calls to the GINA).</span></span><br/> <span data-ttu-id="6dcf5-113">Winlogon è nello stato di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-113">Winlogon is in the logged-out state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dcf5-114">Nessuno è connesso</span><span class="sxs-lookup"><span data-stu-id="6dcf5-114">No one is logged on</span></span></td>
<td><span data-ttu-id="6dcf5-115">(GINA monitora i dispositivi per gli eventi SAS).</span><span class="sxs-lookup"><span data-stu-id="6dcf5-115">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="6dcf5-116">GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> di Winlogon quando è stato ricevuto un evento SAS.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-116">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="6dcf5-117">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> di Gina, consentendo a Gina di elaborare le informazioni di identificazione e autenticazione di un utente.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-117">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> function, allowing the GINA to process a user's identification and authentication information.</span></span><br/> <span data-ttu-id="6dcf5-118">Quando l'accesso ha esito positivo, Winlogon si trova nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-118">When logon is successful, Winlogon is in the logged-on state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dcf5-119">L'utente è connesso</span><span class="sxs-lookup"><span data-stu-id="6dcf5-119">The user is logged on</span></span></td>
<td><span data-ttu-id="6dcf5-120">(GINA monitora i dispositivi per gli eventi SAS).</span><span class="sxs-lookup"><span data-stu-id="6dcf5-120">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="6dcf5-121">GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> di Winlogon quando è stato ricevuto un evento SAS.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-121">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="6dcf5-122">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di Gina, consentendo a Gina di presentare le opzioni all'utente attualmente connesso.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-122">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function, allowing the GINA to present options to the user who is currently logged on.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dcf5-123">L'utente è connesso e desidera bloccare il computer</span><span class="sxs-lookup"><span data-stu-id="6dcf5-123">The user is logged on and wants to lock computer</span></span></td>
<td><span data-ttu-id="6dcf5-124">(GINA monitora i dispositivi per gli eventi SAS).</span><span class="sxs-lookup"><span data-stu-id="6dcf5-124">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="6dcf5-125">GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6dcf5-125">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-126">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-126">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-127">GINA restituisce WLX_SAS_ACTION_LOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-127">The GINA returns WLX_SAS_ACTION_LOCK_WKSTA.</span></span><br/> <span data-ttu-id="6dcf5-128">Lo stato di Winlogon è bloccato dalla workstation.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-128">Winlogon is in the workstation-locked state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dcf5-129">L'utente è connesso, la workstation è bloccata e l'utente desidera sbloccare il computer</span><span class="sxs-lookup"><span data-stu-id="6dcf5-129">The user is logged on, the workstation is locked, and the user wants to unlock computer</span></span></td>
<td><span data-ttu-id="6dcf5-130">(GINA monitora i dispositivi per gli eventi SAS).</span><span class="sxs-lookup"><span data-stu-id="6dcf5-130">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="6dcf5-131">GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6dcf5-131">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-132">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-132">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-133">GINA restituisce WLX_SAS_ACTION_UNLOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-133">The GINA returns WLX_SAS_ACTION_UNLOCK_WKSTA.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dcf5-134">L'utente è connesso e il programma chiama la funzione <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="6dcf5-134">The user is logged on, and the program calls the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> function</span></span></td>
<td><span data-ttu-id="6dcf5-135">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-135">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dcf5-136">L'utente è connesso e vuole disconnettersi tramite SAS</span><span class="sxs-lookup"><span data-stu-id="6dcf5-136">The user is logged on and wants to log off by using SAS</span></span></td>
<td><span data-ttu-id="6dcf5-137">(GINA monitora i dispositivi per gli eventi SAS).</span><span class="sxs-lookup"><span data-stu-id="6dcf5-137">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="6dcf5-138">GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6dcf5-138">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-139">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-139">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-140">GINA restituisce WLX_SAS_ACTION_LOGOFF.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-140">The GINA returns WLX_SAS_ACTION_LOGOFF.</span></span></li>
<li><span data-ttu-id="6dcf5-141">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-141">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dcf5-142">L'utente ha effettuato l'accesso e vuole disconnettersi e arrestarsi usando <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="6dcf5-142">The user is logged on and wants to log off and shut down by using <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="6dcf5-143">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-143">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-144">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-144">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dcf5-145">L'utente ha effettuato l'accesso e vuole disconnettersi e arrestarsi usando SAS</span><span class="sxs-lookup"><span data-stu-id="6dcf5-145">The user is logged on and wants to log off and shut down by using SAS</span></span></td>
<td><span data-ttu-id="6dcf5-146">(GINA monitora i dispositivi per gli eventi SAS).</span><span class="sxs-lookup"><span data-stu-id="6dcf5-146">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="6dcf5-147">GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6dcf5-147">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-148">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-148">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-149">GINA restituisce WLX_SAS_ACTION_SHUTDOWN.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-149">The GINA returns WLX_SAS_ACTION_SHUTDOWN.</span></span></li>
<li><span data-ttu-id="6dcf5-150">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-150">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="6dcf5-151">Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> di Gina.</span><span class="sxs-lookup"><span data-stu-id="6dcf5-151">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
