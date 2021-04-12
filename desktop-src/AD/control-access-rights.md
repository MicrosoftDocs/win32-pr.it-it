---
title: Controllo dei diritti di accesso (AD DS)
description: Tutti gli oggetti in Active Directory Domain Services supportano un set standard di diritti di accesso definiti nell' \_ enumerazione ADS Rights \_ enum.
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- Controllo dei diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 048c4aa685e0c569ef2ac762dcf17366a2394826
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472643"
---
# <a name="control-access-rights-ad-ds"></a>Controllo dei diritti di accesso (AD DS)

Tutti gli oggetti in Active Directory Domain Services supportano un set standard di diritti di accesso definiti nell'enumerazione [**Ads \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum) . Questi diritti di accesso possono essere usati nelle voci di controllo di accesso (ACE) del descrittore di sicurezza di un oggetto per controllare l'accesso all'oggetto. ovvero per controllare gli utenti che possono eseguire operazioni standard, ad esempio la creazione e l'eliminazione di oggetti figlio, la lettura e la scrittura degli attributi degli oggetti. Tuttavia, per alcune classi di oggetti, potrebbe essere auspicabile controllare l'accesso in modo non supportato dai diritti di accesso standard. Per semplificare questa operazione, Active Directory Domain Services consentire l'estensione del meccanismo di controllo di accesso standard tramite l'oggetto **controlAccessRight** .

I diritti di accesso di controllo vengono usati in tre modi:

-   Per i diritti estesi, che sono operazioni speciali non coperte dal set standard di diritti di accesso. Ad esempio, alla classe utente può essere concesso un diritto "Invia come" che può essere utilizzato da Exchange, Outlook o qualsiasi altra applicazione di posta elettronica, per determinare se un utente specifico può inviare un altro utente per loro conto. Per gli oggetti **controlAccessRight** vengono creati diritti estesi impostando l'attributo **validAccesses** in modo che corrisponda al diritto di accesso per il **\_ \_ \_ controllo DS \_ ADS** (256).
-   Per la definizione di set di proprietà, per consentire il controllo dell'accesso a un subset di attributi di un oggetto, anziché solo ai singoli attributi. Con i diritti di accesso standard, una singola voce ACE può concedere o negare l'accesso a tutti gli attributi di un oggetto o a un singolo attributo. I diritti di accesso di controllo consentono a una singola voce ACE di controllare l'accesso a un set di attributi. Ad esempio, la classe utente supporta il set di proprietà **Personal-Information** che include attributi quali via e numero di telefono. I diritti del set di proprietà vengono creati negli oggetti **controlAccessRight** impostando l'attributo **validAccesses** in modo da contenere sia i diritti di accesso **ACTR \_ DS \_ Read \_ prop** (16) che i **ACTRL \_ DS \_ Write \_ prop** (32).
-   Per le scritture convalidate, per richiedere che il sistema esegua il controllo del valore o la convalida, oltre a quanto richiesto dallo schema, prima di scrivere un valore in un attributo in un oggetto DS. In questo modo si garantisce che il valore immesso per l'attributo sia conforme alla semantica richiesta, sia all'interno di un intervallo di valori valido o sottoposto ad altre verifiche speciali che non vengono eseguite per una semplice scrittura di basso livello nell'attributo. Una scrittura convalidata è associata a un'autorizzazione speciale che è diversa dall'autorizzazione "Write <attribute> " che consentirebbe la scrittura di qualsiasi valore nell'attributo senza che venga eseguito il controllo dei valori. La scrittura convalidata è l'unico dei tre diritti di accesso di controllo che non possono essere creati come nuovo diritto di accesso di controllo per un'applicazione. Questo perché il sistema esistente non può essere modificato a livello di codice per applicare la convalida. Se un diritto di accesso al controllo è stato configurato nel sistema come una scrittura convalidata, l'attributo **validAccesses** sugli oggetti **controlAccessRight** conterrà il diritto di accesso **self- \_ \_ \_ Service DS** (8) right ads.

    Nello schema Active Directory di Windows 2000 sono definite solo tre scritture convalidate:

    -   Self-Membership autorizzazione per un oggetto gruppo, che consente l'aggiunta o la rimozione dell'account del chiamante, ma non di altri account, dall'appartenenza a un gruppo.
    -   Autorizzazione convalidata-DNS-host-name per un oggetto computer, che consente l'impostazione di un attributo del nome host DNS conforme al nome del computer e al nome di dominio.
    -   Autorizzazione Validated-SPN per un oggetto computer, che consente l'impostazione di un attributo SPN conforme al nome host DNS del computer.

Per praticità, ogni diritto di accesso di controllo è rappresentato da un oggetto **controlAccessRight** nel contenitore Extended-Rights della partizione di configurazione, anche se i set di proprietà e le scritture convalidate non vengono considerati diritti estesi. Poiché il contenitore di configurazione viene replicato nell'intera foresta, i diritti di controllo vengono propagati in tutti i domini di una foresta. Sono disponibili alcuni diritti di accesso di controllo predefiniti e, ovviamente, è possibile definire anche diritti di accesso personalizzati.

Tutti i diritti di accesso di controllo possono essere visualizzati come autorizzazioni nell'editor ACL.

Per ulteriori informazioni e un esempio di codice C++ e Visual Basic che imposta una voce ACE per controllare l'accesso in lettura/scrittura a un set di proprietà, vedere il [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

Per ulteriori informazioni sull'utilizzo dei diritti di accesso di controllo per controllare l'accesso a operazioni speciali, vedere:

-   [Creazione di un controllo di accesso a destra](creating-a-control-access-right.md)
-   [Impostazione di un controllo ACE destro per l'accesso a un controllo nell'ACL di un oggetto](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [Controllo del diritto di accesso a un controllo nell'elenco ACL di un oggetto](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [Lettura di un set di diritti di accesso di controllo nell'ACL di un oggetto](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 