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
# <a name="interaction-between-winlogon-and-gina"></a>Interazione tra Winlogon e GINA 

[*Winlogon*](../secgloss/w-gly.md) e [*Gina*](../secgloss/g-gly.md) devono comunicare le informazioni di inizializzazione, gestire il monitoraggio e la notifica di [*Secure Attention Sequence*](../secgloss/s-gly.md) (SAS) e consentire attività di disconnessione e arresto. Lo stato di Winlogon determina quale funzione GINA viene chiamata per elaborare qualsiasi evento SAS specificato. Le comunicazioni si verificano nell'ordine indicato di seguito.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Event</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Avvio workstation</td>
<td><ol>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> di Gina per notificare a Gina la versione di Winlogon in uso.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> di Gina per fornire a Gina gli indirizzi delle funzioni di supporto, un handle a Winlogon e per ottenere le informazioni di <a href="/windows/desktop/SecGloss/c-gly"><em>contesto</em></a> per Gina (da usare in tutte le chiamate future a Gina).<br/> Winlogon è nello stato di disconnessione.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>Nessuno è connesso</td>
<td>(GINA monitora i dispositivi per gli eventi SAS).
<ol>
<li>GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> di Winlogon quando è stato ricevuto un evento SAS.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> di Gina, consentendo a Gina di elaborare le informazioni di identificazione e autenticazione di un utente.<br/> Quando l'accesso ha esito positivo, Winlogon si trova nello stato connesso.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>L'utente è connesso</td>
<td>(GINA monitora i dispositivi per gli eventi SAS).
<ol>
<li>GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> di Winlogon quando è stato ricevuto un evento SAS.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di Gina, consentendo a Gina di presentare le opzioni all'utente attualmente connesso.</li>
</ol></td>
</tr>
<tr class="even">
<td>L'utente è connesso e desidera bloccare il computer</td>
<td>(GINA monitora i dispositivi per gli eventi SAS).
<ol>
<li>GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di Gina.</li>
<li>GINA restituisce WLX_SAS_ACTION_LOCK_WKSTA.<br/> Lo stato di Winlogon è bloccato dalla workstation.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>L'utente è connesso, la workstation è bloccata e l'utente desidera sbloccare il computer</td>
<td>(GINA monitora i dispositivi per gli eventi SAS).
<ol>
<li>GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> di Gina.</li>
<li>GINA restituisce WLX_SAS_ACTION_UNLOCK_WKSTA.</li>
</ol></td>
</tr>
<tr class="even">
<td>L'utente è connesso e il programma chiama la funzione <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></td>
<td>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di Gina.</td>
</tr>
<tr class="odd">
<td>L'utente è connesso e vuole disconnettersi tramite SAS</td>
<td>(GINA monitora i dispositivi per gli eventi SAS).
<ol>
<li>GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di Gina.</li>
<li>GINA restituisce WLX_SAS_ACTION_LOGOFF.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di Gina.</li>
</ol></td>
</tr>
<tr class="even">
<td>L'utente ha effettuato l'accesso e vuole disconnettersi e arrestarsi usando <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a></td>
<td><ol>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di Gina.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> di Gina.</li>
</ol></td>
</tr>
<tr class="odd">
<td>L'utente ha effettuato l'accesso e vuole disconnettersi e arrestarsi usando SAS</td>
<td>(GINA monitora i dispositivi per gli eventi SAS).
<ol>
<li>GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di Gina.</li>
<li>GINA restituisce WLX_SAS_ACTION_SHUTDOWN.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di Gina.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> di Gina.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
