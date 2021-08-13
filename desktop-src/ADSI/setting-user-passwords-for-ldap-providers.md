---
title: Impostazione e modifica delle password utente con il provider LDAP
description: Per impostare una password utente, usare il metodo IADsUser.SetPassword.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- Provider LDAP ADSI,oggetto utente,impostazione password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbbd0439a011575fbc9278dbe506d46db2210ce03d807ea74097499cb764b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690526"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Impostazione e modifica delle password utente con il provider LDAP

Per impostare una password utente, usare il [**metodo IADsUser.SetPassword.**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)

Il provider LDAP per Active Directory usa uno dei tre processi per impostare la password. Le directory LDAP di terze parti, ad esempio iPlanet, non usano questo processo di autenticazione della password. Il metodo può variare in base alla configurazione di rete. I metodi di impostazione della password si verificano nell'ordine seguente:

-   In primo luogo, il provider LDAP tenta di usare LDAP su una connessione SSL a 128 bit. Per il corretto funzionamento di SSL LDAP, nel server LDAP deve essere installato il certificato di autenticazione server appropriato e i client che eseguono il codice ADSI devono considerare attendibile l'autorità che ha emesso tali certificati. Sia il server che il client devono supportare la crittografia a 128 bit.
-   In secondo momento, se la connessione SSL ha esito negativo, il provider LDAP tenta di usare Kerberos. In Windows 2000, Kerberos potrebbe non supportare l'autenticazione tra foreste. I miglioramenti successivi di Kerberos supportano l'autenticazione tra foreste.
-   In terzo caso, se Kerberos ha esito negativo, il provider LDAP tenta una chiamata API [**NetUserSetInfo.**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) Nelle versioni precedenti, ADSI chiama **NetUserSetInfo** nel contesto di sicurezza in cui era in esecuzione il thread e non il contesto di sicurezza specificato nella chiamata a [**IADsOpenDSObject.OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject). Nelle versioni successive questa impostazione è stata modificata in modo che il provider ADSI LDAP rappresentasse l'utente specificato nella chiamata **OpenDSObject** quando chiama **NetUserSetInfo.**

Per modificare una password utente, usare il [**metodo IADsUser.ChangePassword.**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) Analogamente [**a SetPassword,**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)questo metodo può usare più processi per modificare la password. I metodi di modifica della password si verificano nell'ordine seguente:

-   In primo luogo, il provider LDAP tenta di usare LDAP su una connessione SSL a 128 bit.
-   In secondo momento, se la connessione 128-SSL ha esito negativo, il provider LDAP tenta una chiamata API [**NetUserChangePassword.**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) Analogamente [**a SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), nelle versioni precedenti il provider ADSI LDAP rappresenta le credenziali utente passate usando il metodo [**IADsOpenDSObject.OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o la funzione [**ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)

 

 