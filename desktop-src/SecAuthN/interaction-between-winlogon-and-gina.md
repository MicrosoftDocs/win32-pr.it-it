---
description: Winlogon e GINA devono comunicare le informazioni di inizializzazione, gestire il monitoraggio e la notifica della sequenza di attenzione sicura e consentire le attività di disconnessione e arresto.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interazione tra Winlogon e GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824c658e4f19b14de339b569a8c9d17992c1b60bb5d4d526de949ce76cd1554d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482361"
---
# <a name="interaction-between-winlogon-and-gina"></a>Interazione tra Winlogon e GINA 

[*Winlogon e*](../secgloss/w-gly.md) [*GINA*](../secgloss/g-gly.md) devono comunicare le informazioni di inizializzazione, gestire il monitoraggio e la notifica della sequenza di attenzione sicura [*e*](../secgloss/s-gly.md) consentire le attività di disconnessione e arresto. Lo stato di Winlogon determina quale funzione GINA viene chiamata per elaborare qualsiasi evento di firma di accesso condiviso specificato. Le comunicazioni vengono eseguite nell'ordine indicato qui.

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
<td>Avvio della workstation</td>
<td><ol>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> di GINA per notificare a GINA la versione di Winlogon in uso.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> di GINA per assegnare a GINA gli indirizzi delle funzioni <a href="/windows/desktop/SecGloss/c-gly"><em></em></a> di supporto, un handle per Winlogon e per ottenere le informazioni di contesto per l'istanza di GINA (da usare in tutte le chiamate future a GINA).<br/> Winlogon è nello stato disconnesso.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>Nessuno è connesso</td>
<td>(l'applicazione GINA monitora i dispositivi per gli eventi di firma di accesso condiviso).
<ol>
<li>L'applicazione GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> di Winlogon quando viene ricevuto un evento di firma di accesso condiviso.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> di GINA, consentendo a GINA di elaborare le informazioni di identificazione e autenticazione di un utente.<br/> Quando l'accesso ha esito positivo, Winlogon è nello stato connesso.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>L'utente è connesso</td>
<td>(l'applicazione GINA monitora i dispositivi per gli eventi di firma di accesso condiviso).
<ol>
<li>L'applicazione GINA chiama la funzione <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> di Winlogon quando viene ricevuto un evento di firma di accesso condiviso.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di GINA, consentendo a GINA di presentare opzioni all'utente attualmente connesso.</li>
</ol></td>
</tr>
<tr class="even">
<td>L'utente è connesso e vuole bloccare il computer</td>
<td>(l'applicazione GINA monitora i dispositivi per gli eventi di firma di accesso condiviso).
<ol>
<li>GINA chiama la <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>funzione WlxSasNotify.</strong></a></li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di GINA.</li>
<li>L'oggetto GINA restituisce WLX_SAS_ACTION_LOCK_WKSTA.<br/> Winlogon è nello stato bloccato dalla workstation.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>L'utente è connesso, la workstation è bloccata e l'utente vuole sbloccare il computer</td>
<td>(l'applicazione GINA monitora i dispositivi per gli eventi di firma di accesso condiviso).
<ol>
<li>GINA chiama la <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>funzione WlxSasNotify.</strong></a></li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS di GINA.</strong></a></li>
<li>L'oggetto GINA restituisce WLX_SAS_ACTION_UNLOCK_WKSTA.</li>
</ol></td>
</tr>
<tr class="even">
<td>L'utente è connesso e il programma chiama la <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>funzione ExitWindowsEx</strong></a></td>
<td>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di GINA.</td>
</tr>
<tr class="odd">
<td>L'utente è connesso e vuole disconnettersi usando la firma di accesso condiviso</td>
<td>(l'applicazione GINA monitora i dispositivi per gli eventi di firma di accesso condiviso).
<ol>
<li>GINA chiama la <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>funzione WlxSasNotify.</strong></a></li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di GINA.</li>
<li>L'oggetto GINA restituisce WLX_SAS_ACTION_LOGOFF.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di GINA.</li>
</ol></td>
</tr>
<tr class="even">
<td>L'utente è connesso e vuole disconnettersi e arrestarlo usando <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a></td>
<td><ol>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di GINA.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> di GINA.</li>
</ol></td>
</tr>
<tr class="odd">
<td>L'utente è connesso e vuole disconnettersi e arrestarlo usando la firma di accesso condiviso</td>
<td>(l'applicazione GINA monitora i dispositivi per gli eventi di firma di accesso condiviso).
<ol>
<li>GINA chiama la <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>funzione WlxSasNotify.</strong></a></li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> di GINA.</li>
<li>L'oggetto GINA restituisce WLX_SAS_ACTION_SHUTDOWN.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> di GINA.</li>
<li>Winlogon chiama la funzione <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> di GINA.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
