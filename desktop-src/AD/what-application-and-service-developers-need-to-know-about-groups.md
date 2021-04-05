---
title: Quali sviluppatori di applicazioni e servizi devono conoscere sui gruppi
description: Quando si sviluppa un'applicazione o un servizio, è possibile utilizzare i gruppi per delegare l'amministrazione o controllare l'accesso all'applicazione o al servizio nel suo complesso o in parte.
ms.assetid: 19e189a5-2880-4b45-84c8-e7b542c4fbb6
ms.tgt_platform: multiple
keywords:
- Quali sviluppatori di applicazioni e servizi devono conoscere sui gruppi
- gruppi AD, informazioni per sviluppatori di applicazioni e servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd23f598925c959502e1013ff43ad18bbb42ed7b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724383"
---
# <a name="what-application-and-service-developers-need-to-know-about-groups"></a>Quali sviluppatori di applicazioni e servizi devono conoscere sui gruppi

Quando si sviluppa un'applicazione o un servizio, è possibile utilizzare i gruppi per delegare l'amministrazione o controllare l'accesso all'applicazione o al servizio nel suo complesso o in parte. Ad esempio, un'applicazione può controllare gli utenti che possono eseguire varie operazioni amministrative. A tale scopo, creare voci ACE che concedono i diritti di accesso specificati ai gruppi appropriati. È consigliabile avere una voce ACE che consenta l'accesso a un gruppo anziché avere più ACE che concedono l'accesso a singoli utenti o computer.

Quando si usano i gruppi, è consigliabile che le applicazioni usino le linee guida seguenti:

-   Non creare dipendenze da gruppi hardcoded, che possono creare complicazioni se il gruppo viene eliminato o spostato.
-   Evitare di usare i gruppi predefiniti a meno che la funzione del gruppo non fornisca le esigenze specifiche per l'applicazione. Non è ad esempio necessario che un utente sia membro del gruppo Administrators solo per fornire all'utente l'autorizzazione per la creazione di un account computer. In questo modo l'utente dispone di autorizzazioni e privilegi che potrebbero non essere necessari, che possono causare una vulnerabilità della sicurezza. Al contrario, è necessario creare un nuovo gruppo di sicurezza con le autorizzazioni specifiche necessarie e aggiungere l'utente a questo nuovo gruppo.
-   Quando si creano nuovi gruppi, tenere presenti le raccomandazioni seguenti:
    -   Proteggere il gruppo impostando le voci ACE che controllano gli utenti che possono aggiungere o rimuovere membri.
    -   Usare i gruppi globali se vengono usati per il controllo di accesso sugli oggetti in Active Directory Domain Services.
    -   Usare i gruppi universali solo se necessario (i dati dei membri sono necessari a livello globale usando il catalogo globale; il gruppo può contenere qualsiasi utente o gruppo). Se si usano i gruppi universali, inserire i gruppi globali nel gruppo universale e aggiungere/rimuovere gli utenti dal gruppo globale. Evitare modifiche superflue ai gruppi universali per l'efficienza della replica.
-   Non usare l'appartenenza al gruppo per il controllo di accesso. Usare invece una voce ACE e controllare l'accesso facendo in modo che il sistema esegua un controllo di accesso.

Per controllare l'accesso a operazioni che non rientrano nei diritti di accesso predefiniti per gli oggetti in Dominio di Active Directory Services, usare la funzionalità controlla diritti di accesso di controllo di accesso in Windows 2000. Per altre informazioni, vedere [**Ads \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum).

**Per usare un diritto di accesso al controllo per controllare il diritto di eseguire un'operazione**

1.  Creare un diritto di accesso di controllo che definisce il tipo di accesso all'applicazione o al servizio. Per altre informazioni, vedere [controllare i diritti di accesso](control-access-rights.md).
2.  Creare un oggetto in Active Directory Domain Services che rappresenti l'applicazione, il servizio o la risorsa.
3.  Aggiungere le voci ACE degli oggetti all'elenco DACL nel descrittore di sicurezza dell'oggetto per concedere o negare agli utenti o ai gruppi il diritto di accesso di controllo su tale oggetto. Per ulteriori informazioni, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).
4.  Quando un utente tenta di eseguire l'operazione protetta, l'applicazione o il servizio utilizza la funzione [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) per determinare se all'utente è concesso il diritto di accesso del controllo. Per ulteriori informazioni, vedere controllo dell' [accesso a un controllo direttamente nell'elenco ACL di un oggetto](checking-a-control-access-right-in-an-objectampaposs-acl.md).
5.  In base al risultato del controllo di accesso sull'oggetto, l'applicazione o il servizio può concedere o negare l'accesso dell'utente all'applicazione o al servizio.

Un'applicazione di servizio può inoltre creare un gruppo i cui membri sono le varie istanze del servizio. Ad esempio, un servizio con istanze installate in più computer in un'azienda potrebbe avere un file di log comune in cui tutte le istanze del servizio scrivono. Il programma di installazione del servizio crea il file di log e utilizza un DACL per concedere l'accesso solo ai membri di un gruppo. I membri del gruppo sarebbero gli account utente con cui vengono eseguite le varie istanze del servizio o se i servizi vengono eseguiti con l'account LocalSystem, i membri sarebbero gli account computer dei server host.

 

 