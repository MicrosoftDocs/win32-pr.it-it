---
title: Diritti di accesso e sicurezza di Windows Station
description: Sicurezza consente di controllare l'accesso agli oggetti di Windows Station. Per ulteriori informazioni sulla sicurezza, vedere Access-Control Model.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299880"
---
# <a name="window-station-security-and-access-rights"></a>Diritti di accesso e sicurezza di Windows Station

Sicurezza consente di controllare l'accesso agli oggetti di Windows Station. Per altre informazioni sulla sicurezza, vedere [modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).

È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per un oggetto della stazione della finestra quando si chiama la funzione [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) . Se si specifica NULL, la finestra stazione ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per una stazione della finestra provengono dal token primario o di rappresentazione del creatore.

Per ottenere o impostare il descrittore di sicurezza di un oggetto della stazione della finestra, chiamare le funzioni [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Quando si chiama la funzione [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza dell'oggetto.

I diritti di accesso validi per gli oggetti Window Station includono i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) e alcuni diritti di accesso specifici per gli oggetti. La tabella seguente elenca i diritti di accesso standard usati da tutti gli oggetti.

| Valore                       | Significato                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elimina (0x00010000L)        | Obbligatorio per eliminare l'oggetto.                                                                                                                                                                                                                                                       |
| \_Controllo Read (0x00020000L) | Obbligatorio per leggere le informazioni nel descrittore di sicurezza per l'oggetto, escluse le informazioni nell'elenco SACL. Per leggere o scrivere il SACL, è necessario richiedere il diritto di accesso alla sicurezza del sistema di accesso \_ \_ . Per ulteriori informazioni, vedere il [diritto di accesso SACL](/windows/desktop/SecAuthZ/sacl-access-right). |
| Sincronizza (0x00100000L)   | Non supportato per gli oggetti di Windows Station.                                                                                                                                                                                                                                            |
| SCRITTURA \_ DAC (0x00040000L)    | Obbligatorio per modificare l'elenco DACL nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                               |
| \_Proprietario scrittura (0x00080000L)  | Obbligatorio per modificare il proprietario nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                              |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto.



| Diritto di accesso                        | Descrizione                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WINSTA \_ tutti gli \_ accessi (0x37F)         | Tutti i diritti di accesso possibili per la stazione di finestra.                                                                                                                                                                                                                            |
| WINSTA \_ ACCESSCLIPBOARD (0x0004L)   | Obbligatorio per utilizzare gli Appunti.                                                                                                                                                                                                                                                |
| WINSTA \_ ACCESSGLOBALATOMS (0x0020L) | Obbligatorio per modificare gli atomi globali.                                                                                                                                                                                                                                          |
| WINSTA \_ CREATEDESKTOP (0x0008L)     | Obbligatorio per creare nuovi oggetti desktop sulla stazione di finestra.                                                                                                                                                                                                                 |
| WINSTA \_ ENUMDESKTOPS (0x0001L)      | Obbligatorio per enumerare gli oggetti desktop esistenti.                                                                                                                                                                                                                               |
| \_Enumerazione winsta (0x0100L)         | Obbligatorio perché la stazione della finestra venga enumerata.                                                                                                                                                                                                                             |
| WINSTA \_ EXITWINDOWS (0x0040L)       | Obbligatorio per chiamare correttamente la funzione [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) . Le stazioni della finestra possono essere condivise dagli utenti e questo tipo di accesso può impedire ad altri utenti di una stazione di finestra di disconnettersi dal proprietario della stazione di finestra. |
| WINSTA \_ diritti ReadAttributes (0x0002L)    | Obbligatorio per leggere gli attributi di un oggetto della stazione di finestra. Questo attributo include le impostazioni relative ai colori e ad altre proprietà della stazione della finestra globale.                                                                                                                                |
| WINSTA \_ READSCREEN (0x0200L)        | Obbligatorio per accedere al contenuto della schermata.                                                                                                                                                                                                                                           |
| WINSTA \_ WRITEATTRIBUTES (0x0010L)   | Obbligatorio per modificare gli attributi di un oggetto della stazione di finestra. Gli attributi includono impostazioni colore e altre proprietà globali della stazione di finestra.                                                                                                                               |



 

Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per l'oggetto Interactive Window Station, ovvero la stazione della finestra assegnata alla sessione di accesso dell'utente interattivo.



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



 

Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per un oggetto finestra stazione non interattiva. Il sistema assegna stazioni della finestra non interattive a tutte le sessioni di accesso diverse da quelle dell'utente interattivo.



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



 

\_ \_ Se si desidera leggere o scrivere il SACL dell'oggetto, è possibile richiedere il diritto di accesso alla sicurezza del sistema di accesso a un oggetto di Windows Station. Per altre informazioni, vedere [elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [accesso SACL diritto](/windows/desktop/SecAuthZ/sacl-access-right).

 

 