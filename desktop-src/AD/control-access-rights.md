---
title: Controllare i diritti di accesso (Ad DS)
description: Tutti gli oggetti in Active Directory Domain Services supportano un set standard di diritti di accesso definiti nell'enumerazione ADS \_ RIGHTS \_ ENUM.
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- Controllare i diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c975ac20cac683e754f1b703bd272356c9b8df8f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881614"
---
# <a name="control-access-rights-ad-ds"></a>Controllare i diritti di accesso (Ad DS)

Tutti gli oggetti in Active Directory Domain Services supportano un set standard di diritti di accesso definiti [**nell'enumerazione ADS \_ RIGHTS \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_rights_enum) Questi diritti di accesso possono essere usati nelle voci di controllo di accesso (ACE) del descrittore di sicurezza di un oggetto per controllare l'accesso all'oggetto. cio, per controllare chi può eseguire operazioni standard, ad esempio la creazione e l'eliminazione di oggetti figlio o la lettura e la scrittura degli attributi dell'oggetto. Tuttavia, per alcune classi di oggetti può essere opportuno controllare l'accesso in modo non supportato dai diritti di accesso standard. Per facilitare questa operazione, Active Directory Domain Services consentire l'estensione del meccanismo di controllo di accesso standard tramite **l'oggetto controlAccessRight.**

I diritti di accesso di controllo vengono usati in tre modi:

-   Per i diritti estesi, ovvero operazioni speciali non coperte dal set standard di diritti di accesso. Ad esempio, alla classe utente può essere concesso un diritto "Invia come" che può essere usato da Exchange, Outlook o qualsiasi altra applicazione di posta elettronica per determinare se un determinato utente può fare in modo che un altro utente invii messaggi di posta elettronica per suo conto. I diritti estesi vengono creati sugli oggetti **controlAccessRight** impostando l'attributo **validAccesses** su uguale al diritto di accesso **\_ ADS RIGHT \_ DS \_ CONTROL \_ ACCESS** (256).
-   Per definire i set di proprietà, per consentire il controllo dell'accesso a un subset degli attributi di un oggetto, anziché solo ai singoli attributi. Usando i diritti di accesso standard, una singola ACE può concedere o negare l'accesso a tutti gli attributi di un oggetto o a un singolo attributo. I diritti di accesso di controllo consentono a una singola ACE di controllare l'accesso a un set di attributi. Ad esempio, la classe utente supporta il set **di proprietà Personal-Information** che include attributi come indirizzo e numero di telefono. I diritti del set di proprietà vengono creati per gli oggetti **controlAccessRight** impostando l'attributo **validAccesses** in modo che contenga sia i diritti di accesso **ACTR \_ DS \_ READ \_ PROP** (16) che i diritti di accesso **ACTRL \_ DS \_ WRITE \_ PROP** (32).
-   Per le scritture convalidate, è necessario che il sistema esempi il controllo dei valori, o convalida, oltre a quello richiesto dallo schema, prima di scrivere un valore in un attributo in un oggetto DS. Ciò garantisce che il valore immesso per l'attributo sia conforme alla semantica richiesta, sia compreso in un intervallo valido di valori o sia sottoposto a un altro controllo speciale che non verrebbe eseguito per una semplice scrittura di basso livello nell'attributo. Una scrittura convalidata è associata a un'autorizzazione speciale distinta dall'autorizzazione "Attributo di scrittura" che consente la scrittura di qualsiasi valore nell'attributo senza alcun controllo &lt; &gt; dei valori eseguito. La scrittura convalidata è l'unico dei tre diritti di accesso di controllo che non possono essere creati come nuovo diritto di accesso di controllo per un'applicazione. Ciò è dovuto al fatto che il sistema esistente non può essere modificato a livello di codice per applicare la convalida. Se nel sistema è stato configurato un diritto di accesso di controllo come scrittura convalidata, l'attributo **validAccesses** negli oggetti **controlAccessRight** conterrà il diritto di accesso **ADS \_ RIGHT \_ DS \_ SELF** (8).

    Nello schema di Active Directory Windows 2000 sono definite solo tre scritture convalidate:

    -   Self-Membership per un oggetto Gruppo, che consente di aggiungere o rimuovere l'account del chiamante, ma nessun altro account, dall'appartenenza a un gruppo.
    -   Autorizzazione Validated-DNS-Host-Name per un oggetto Computer, che consente di impostare un attributo del nome host DNS conforme al nome computer e al nome di dominio.
    -   Autorizzazione SPN convalidata per un oggetto Computer, che consente di impostare un attributo SPN conforme al nome host DNS del computer.

Per praticità, ogni diritto di accesso di controllo è rappresentato da un oggetto **controlAccessRight** nel contenitore Extended-Rights della partizione di configurazione, anche se i set di proprietà e le scritture convalidate non sono considerati diritti estesi. Poiché il contenitore Configuration viene replicato nell'intera foresta, i diritti di controllo vengono propagati in tutti i domini di una foresta. Esistono diversi diritti di accesso di controllo predefiniti e, naturalmente, è anche possibile definire diritti di accesso personalizzati.

Tutti i diritti di accesso di controllo possono essere visualizzati come autorizzazioni nell'editor ACL.

Per altre informazioni e un esempio di codice C++ e Visual Basic che imposta una ACE per controllare l'accesso in lettura/scrittura a un set di proprietà, vedere Codice di esempio per l'impostazione di una [ACE](example-code-for-setting-an-ace-on-a-directory-object.md)in un oggetto directory .

Per altre informazioni sull'uso dei diritti di accesso di controllo per controllare l'accesso a operazioni speciali, vedere:

-   [Creazione di un diritto di accesso di controllo](creating-a-control-access-right.md)
-   [Impostazione di una ACE del diritto di accesso di controllo nell'elenco di controllo di accesso di un oggetto](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [Controllo di un diritto di accesso di controllo nell'ACL di un oggetto](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [Lettura di un set di diritti di accesso di controllo nell'elenco di controllo di accesso di un oggetto](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 
