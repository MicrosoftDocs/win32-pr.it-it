---
title: Sicurezza e diritti di accesso di Window Station
description: La sicurezza consente di controllare l'accesso agli oggetti stazione finestra. Per altre informazioni sulla sicurezza, vedere Access-Control modello.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e3b6871fe0e465b4394e871537fbb8ca07f6439577833d61a7fe0c3106685f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435996"
---
# <a name="window-station-security-and-access-rights"></a>Sicurezza e diritti di accesso di Window Station

La sicurezza consente di controllare l'accesso agli oggetti stazione finestra. Per altre informazioni sulla sicurezza, vedere [Modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).

È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per un oggetto stazione finestra quando si chiama la [**funzione CreateWindowStation.**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) Se si specifica NULL, la stazione finestra ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per una stazione finestra provengono dal token primario o di rappresentazione dell'autore.

Per ottenere o impostare il descrittore di sicurezza di un oggetto stazione finestra, chiamare le [**funzioni GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) [**e SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

Quando si chiama la [**funzione OpenWindowStation,**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza dell'oggetto.

I diritti di accesso validi per gli oggetti window station includono i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) e alcuni diritti di accesso specifici degli oggetti. Nella tabella seguente sono elencati i diritti di accesso standard usati da tutti gli oggetti.

| Valore                       | Significato                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE (0x00010000L)        | Obbligatorio per eliminare l'oggetto.                                                                                                                                                                                                                                                       |
| CONTROLLO \_ LETTURA (0x00020000L) | Obbligatorio per leggere le informazioni nel descrittore di sicurezza per l'oggetto, senza includere le informazioni nel SACL. Per leggere o scrivere il SACL, è necessario richiedere il diritto di accesso ACCESS \_ SYSTEM \_ SECURITY. Per altre informazioni, vedere [Diritto di accesso SACL.](/windows/desktop/SecAuthZ/sacl-access-right) |
| SYNCHRONIZE (0x00100000L)   | Non supportato per gli oggetti stazione finestra.                                                                                                                                                                                                                                            |
| APPLICAZIONE \_ LIVELLO DATI WRITE (0x00040000L)    | Obbligatorio per modificare l'elenco DACL nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                               |
| WRITE \_ OWNER (0x00080000L)  | Obbligatorio per modificare il proprietario nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                              |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto.



| Diritto di accesso                        | Descrizione                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WINSTA \_ ALL \_ ACCESS (0x37F)         | Tutti i diritti di accesso possibili per la stazione finestra.                                                                                                                                                                                                                            |
| WINSTA \_ ACCESSCLIPBOARD (0x0004L)   | Obbligatorio per usare gli Appunti.                                                                                                                                                                                                                                                |
| WINSTA \_ ACCESSGLOBALATOMS (0x0020L) | Obbligatorio per modificare gli atomi globali.                                                                                                                                                                                                                                          |
| WINSTA \_ CREATEDESKTOP (0x0008L)     | Obbligatorio per creare nuovi oggetti desktop nella stazione della finestra.                                                                                                                                                                                                                 |
| WINSTA \_ ENUMDESKTOPS (0x0001L)      | Obbligatorio per enumerare gli oggetti desktop esistenti.                                                                                                                                                                                                                               |
| WINSTA \_ ENUMERATE (0x0100L)         | Obbligatorio per l'enumerazione della stazione finestra.                                                                                                                                                                                                                             |
| WINSTA \_ EXITWINDOWS (0x0040L)       | Obbligatorio per chiamare correttamente [**la funzione ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) [**o ExitWindowsEx.**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) Le stazioni finestra possono essere condivise dagli utenti e questo tipo di accesso può impedire ad altri utenti di una stazione finestra di disconnettersi dal proprietario della stazione finestra. |
| WINSTA \_ READATTRIBUTES (0x0002L)    | Obbligatorio per leggere gli attributi di un oggetto stazione finestra. Questo attributo include le impostazioni dei colori e altre proprietà globali della stazione della finestra.                                                                                                                                |
| WINSTA \_ READSCREEN (0x0200L)        | Obbligatorio per accedere al contenuto dello schermo.                                                                                                                                                                                                                                           |
| WINSTA \_ WRITEATTRIBUTES (0x0010L)   | Obbligatorio per modificare gli attributi di un oggetto stazione finestra. Gli attributi includono le impostazioni dei colori e altre proprietà globali della stazione della finestra.                                                                                                                               |



 

Di seguito sono riportati i diritti di accesso [generici](/windows/desktop/SecAuthZ/generic-access-rights) per l'oggetto stazione finestra interattiva, ovvero la stazione finestra assegnata alla sessione di accesso dell'utente interattivo.



<table>
<thead>
<tr class="header">
<th>Diritto di accesso</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per un oggetto stazione finestra non interattivo. Il sistema assegna stazioni finestra non interattive a tutte le sessioni di accesso diverse da quelle dell'utente interattivo.



<table>
<thead>
<tr class="header">
<th>Diritto di accesso</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

È possibile richiedere il diritto di accesso ACCESS SYSTEM SECURITY a un oggetto stazione finestra se si vuole leggere o scrivere il \_ \_ SACL dell'oggetto. Per altre informazioni, vedere [Elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e Diritto di accesso [SACL.](/windows/desktop/SecAuthZ/sacl-access-right)

 

 