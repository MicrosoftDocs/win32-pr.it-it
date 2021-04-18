---
title: Diritti di accesso e sicurezza desktop
description: Sicurezza consente di controllare l'accesso agli oggetti desktop. Per ulteriori informazioni sulla sicurezza, vedere Access-Control Model.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399347"
---
# <a name="desktop-security-and-access-rights"></a>Diritti di accesso e sicurezza desktop

Sicurezza consente di controllare l'accesso agli oggetti desktop. Per altre informazioni sulla sicurezza, vedere [modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).

È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per un oggetto desktop quando si chiama la funzione [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) o [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) . Se si specifica NULL, il desktop ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per un desktop provengono dalla relativa stazione padre della finestra.

Per ottenere o impostare il descrittore di sicurezza di un oggetto della stazione della finestra, chiamare le funzioni [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Quando si chiama la funzione [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) o [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza dell'oggetto.

I diritti di accesso validi per gli oggetti desktop includono i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) e alcuni diritti di accesso specifici per gli oggetti. La tabella seguente elenca i diritti di accesso standard usati da tutti gli oggetti.

| Valore                       | Significato                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elimina (0x00010000L)        | Obbligatorio per eliminare l'oggetto.                                                                                                                                                                                                                                                       |
| \_Controllo Read (0x00020000L) | Obbligatorio per leggere le informazioni nel descrittore di sicurezza per l'oggetto, escluse le informazioni nell'elenco SACL. Per leggere o scrivere il SACL, è necessario richiedere il diritto di accesso alla sicurezza del sistema di accesso \_ \_ . Per ulteriori informazioni, vedere il [diritto di accesso SACL](/windows/desktop/SecAuthZ/sacl-access-right). |
| Sincronizza (0x00100000L)   | Non supportato per oggetti desktop.                                                                                                                                                                                                                                                   |
| SCRITTURA \_ DAC (0x00040000L)    | Obbligatorio per modificare l'elenco DACL nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                               |
| \_Proprietario scrittura (0x00080000L)  | Obbligatorio per modificare il proprietario nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                              |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto.



| Diritto di accesso                       | Descrizione                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| DESKTOP \_ CREATEMENU (0x0004L)      | Necessario per creare un menu sul desktop.                                                   |
| DESKTOP \_ CREATEWINDOW (0x0002L)    | Obbligatorio per creare una finestra sul desktop.                                                 |
| \_Enumerazione desktop (0x0040L)       | Obbligatorio per l'enumerazione del desktop.                                                  |
| DESKTOP \_ HOOKCONTROL (0x0008L)     | Obbligatorio per stabilire uno degli hook di finestra.                                              |
| DESKTOP \_ JOURNALPLAYBACK (0x0020L) | Necessario per eseguire la riproduzione Journal su un desktop.                                          |
| DESKTOP \_ JOURNALRECORD (0x0010L)   | Obbligatorio per eseguire la registrazione Journal su un desktop.                                         |
| DESKTOP \_ READOBJECTS (0x0001L)     | Obbligatorio per leggere gli oggetti sul desktop.                                                    |
| DESKTOP \_ SWITCHDESKTOP (0x0100L)   | Obbligatorio per attivare il desktop mediante la funzione [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) . |
| DESKTOP \_ WRITEOBJECTS (0x0080L)    | Obbligatorio per scrivere oggetti sul desktop.                                                   |



 

Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per un oggetto desktop contenuto nella stazione finestra interattiva della sessione di accesso dell'utente.



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
<td><dl> DESKTOP_ENUMERATE<br />
DESKTOP_READOBJECTS<br />
STANDARD_RIGHTS_READ<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_WRITE<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> DESKTOP_SWITCHDESKTOP<br />
STANDARD_RIGHTS_EXECUTE<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_ENUMERATE<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_READOBJECTS<br />
DESKTOP_SWITCHDESKTOP<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_REQUIRED<br />
</dl></td>
</tr>
</tbody>
</table>



 

È possibile richiedere il \_ \_ diritto di accesso di sicurezza del sistema di accesso a un oggetto desktop se si desidera leggere o scrivere il SACL dell'oggetto. Per altre informazioni, vedere [elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [accesso SACL diritto](/windows/desktop/SecAuthZ/sacl-access-right).

 

 