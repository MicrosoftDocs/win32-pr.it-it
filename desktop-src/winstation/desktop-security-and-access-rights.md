---
title: Desktop Security and Access Rights
description: La sicurezza consente di controllare l'accesso agli oggetti desktop. Per altre informazioni sulla sicurezza, vedere Access-Control modello.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805a9b5b3db70bf496d467b774dc7c959030b43d6f89d40aabd0336540b7e56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346691"
---
# <a name="desktop-security-and-access-rights"></a>Desktop Security and Access Rights

La sicurezza consente di controllare l'accesso agli oggetti desktop. Per altre informazioni sulla sicurezza, vedere [Modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).

È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per un oggetto desktop quando si chiama la [**funzione CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) o [**CreateDesktopEx.**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) Se si specifica NULL, il desktop ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per un desktop provengono dalla relativa stazione della finestra padre.

Per ottenere o impostare il descrittore di sicurezza di un oggetto stazione finestra, chiamare le [**funzioni GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) [**e SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

Quando si chiama la [**funzione OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) o [**OpenInputDesktop,**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza dell'oggetto.

I diritti di accesso validi per gli oggetti desktop includono i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) e alcuni diritti di accesso specifici degli oggetti. Nella tabella seguente sono elencati i diritti di accesso standard usati da tutti gli oggetti.

| Valore                       | Significato                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE (0x00010000L)        | Obbligatorio per eliminare l'oggetto.                                                                                                                                                                                                                                                       |
| CONTROLLO \_ LETTURA (0x00020000L) | Obbligatorio per leggere le informazioni nel descrittore di sicurezza per l'oggetto, senza includere le informazioni nel SACL. Per leggere o scrivere il SACL, è necessario richiedere il diritto di accesso ACCESS \_ SYSTEM \_ SECURITY. Per altre informazioni, vedere [Diritto di accesso SACL.](/windows/desktop/SecAuthZ/sacl-access-right) |
| SYNCHRONIZE (0x00100000L)   | Non supportato per gli oggetti desktop.                                                                                                                                                                                                                                                   |
| APPLICAZIONE \_ LIVELLO DATI WRITE (0x00040000L)    | Obbligatorio per modificare l'elenco DACL nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                               |
| WRITE \_ OWNER (0x00080000L)  | Obbligatorio per modificare il proprietario nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                              |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto.



| Diritto di accesso                       | Descrizione                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| CREATEMENU \_ DESKTOP (0x0004L)      | Obbligatorio per creare un menu sul desktop.                                                   |
| DESKTOP \_ CREATEWINDOW (0x0002L)    | Obbligatorio per creare una finestra sul desktop.                                                 |
| DESKTOP \_ ENUMERATE (0x0040L)       | Obbligatorio per l'enumerazione del desktop.                                                  |
| DESKTOP \_ HOOKCONTROL (0x0008L)     | Obbligatorio per stabilire uno degli hook della finestra.                                              |
| DESKTOP \_ JOURNALPLAYBACK (0x0020L) | Obbligatorio per eseguire la riproduzione del journal su un desktop.                                          |
| DESKTOP \_ JOURNALRECORD (0x0010L)   | Obbligatorio per eseguire la registrazione journal su un desktop.                                         |
| \_READOBJECTS DESKTOP (0x0001L)     | Obbligatorio per leggere gli oggetti sul desktop.                                                    |
| COMMUTATORE \_ DESKTOPDESKTOP (0x0100L)   | Obbligatorio per attivare il desktop usando [**la funzione SwitchDesktop.**](/windows/win32/api/winuser/nf-winuser-switchdesktop) |
| \_DESKTOP WRITEOBJECTS (0x0080L)    | Obbligatorio per scrivere oggetti sul desktop.                                                   |



 

Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per un oggetto desktop contenuto nella stazione della finestra interattiva della sessione di accesso dell'utente.



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



 

È possibile richiedere il diritto di accesso ACCESS SYSTEM SECURITY a un oggetto desktop se si vuole leggere o scrivere il \_ \_ SACL dell'oggetto. Per altre informazioni, vedere [Elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e Diritto di accesso [SACL.](/windows/desktop/SecAuthZ/sacl-access-right)

 

 