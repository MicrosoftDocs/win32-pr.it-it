---
title: Impostazione e modifica delle password utente con il provider LDAP
description: Per impostare una password utente, utilizzare il metodo IADsUser. sepassword.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- ADSI del provider LDAP, oggetto utente, impostazione delle password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5488146de271ac1108a904cd85163fad9d7dd205
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339222"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Impostazione e modifica delle password utente con il provider LDAP

Per impostare una password utente, utilizzare il metodo [**IADsUser. sepassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .

Il provider LDAP per Active Directory usa uno dei tre processi per impostare la password (le directory LDAP di terze parti, ad esempio iPlanet, non usano questo processo di autenticazione della password). Il metodo può variare in base alla configurazione di rete. I metodi set password si verificano nell'ordine seguente:

-   In primo luogo, il provider LDAP tenta di usare LDAP su una connessione SSL a 128 bit. Per il corretto funzionamento di LDAP SSL, il server LDAP deve avere installato il certificato di autenticazione server appropriato e i client che eseguono il codice ADSI devono considerare attendibile l'autorità che ha emesso tali certificati. Sia il server che il client devono supportare la crittografia a 128 bit.
-   In secondo luogo, se la connessione SSL ha esito negativo, il provider LDAP tenta di utilizzare Kerberos. In Windows 2000, Kerberos potrebbe non supportare l'autenticazione tra foreste. Miglioramenti successivi a Kerberos supportano l'autenticazione tra foreste.
-   Terzo, se Kerberos ha esito negativo, il provider LDAP tenta una chiamata API [**NetUserSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) . Nelle versioni precedenti, ADSI ha chiamato **NetUserSetInfo** nel contesto di sicurezza in cui il thread era in esecuzione e non il contesto di sicurezza specificato nella chiamata a [**IADsOpenDSObject. OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject). Nelle versioni successive questa operazione è stata modificata in modo che il provider LDAP ADSI rappresenti l'utente specificato nella chiamata **OpenDSObject** quando chiama **NetUserSetInfo**.

Per modificare la password di un utente, usare il metodo [**IADsUser. ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) . Come per la password, questo metodo può usare più processi per modificare [**la password.**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) I metodi di modifica della password si verificano nell'ordine seguente:

-   In primo luogo, il provider LDAP tenta di usare LDAP su una connessione SSL a 128 bit.
-   In secondo luogo, se la connessione 128-SSL ha esito negativo, il provider LDAP tenta una chiamata API [**NetUserChangePassword**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) . Come per la [**password**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), nelle versioni precedenti il provider LDAP ADSI rappresenta le credenziali utente passate tramite il metodo [**IADsOpenDSObject. OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

 

 