---
title: Informazioni sui gruppi da parte degli sviluppatori di applicazioni e servizi
description: Quando si sviluppa un'applicazione o un servizio, è possibile usare i gruppi per delegare l'amministrazione o controllare l'accesso all'applicazione o al servizio nel suo complesso o in parte.
ms.assetid: 19e189a5-2880-4b45-84c8-e7b542c4fbb6
ms.tgt_platform: multiple
keywords:
- Informazioni sui gruppi da parte degli sviluppatori di applicazioni e servizi
- groups AD , informazioni per sviluppatori di applicazioni e servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b59a8a1ce369d9b5fa1093297f219bf6a206178a950b9d0762fde3069846551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024394"
---
# <a name="what-application-and-service-developers-need-to-know-about-groups"></a>Informazioni sui gruppi da parte degli sviluppatori di applicazioni e servizi

Quando si sviluppa un'applicazione o un servizio, è possibile usare i gruppi per delegare l'amministrazione o controllare l'accesso all'applicazione o al servizio nel suo complesso o in parte. Ad esempio, un'applicazione può controllare chi può eseguire varie operazioni amministrative. A tale scopo, creare ACE che concedono diritti di accesso specificati ai gruppi appropriati. È buona norma di programmazione disporre di una ACE che concede l'accesso a un gruppo anziché di più voci ACE che concedono l'accesso a singoli utenti o computer.

È consigliabile che le applicazioni usino le linee guida seguenti quando si usano i gruppi:

-   Non creare dipendenze da gruppi hard coded, che possono creare complicazioni se il gruppo viene eliminato o spostato.
-   Evitare di usare gruppi predefiniti, a meno che la funzione del gruppo non specifici le esigenze specifiche dell'applicazione. Ad esempio, non è necessario che un utente sia membro del gruppo Administrators solo per fornire all'utente l'autorizzazione per creare un account computer. In questo modo l'utente dispone di autorizzazioni e privilegi che potrebbero non essere necessari e ciò può causare vulnerabilità della sicurezza. È invece necessario creare un nuovo gruppo di sicurezza con le autorizzazioni specifiche necessarie e aggiungere l'utente a questo nuovo gruppo.
-   Quando si creano nuovi gruppi, tenere presenti i consigli seguenti:
    -   Proteggere il gruppo impostando le voci ACE che controllano chi può aggiungere o rimuovere membri.
    -   Usare i gruppi globali se vengono usati per il controllo di accesso sugli oggetti Active Directory Domain Services.
    -   Usare i gruppi universali solo se necessario (i dati dei membri sono necessari a livello globale usando il catalogo globale; il gruppo può contenere qualsiasi utente/gruppo). Se si usano gruppi universali, inserire i gruppi globali nel gruppo universale e aggiungere/rimuovere utenti dal gruppo globale. Evitare modifiche eccessive ai gruppi universali per l'efficienza della replica.
-   Non usare l'appartenenza ai gruppi per il controllo di accesso. Usare invece una ACE e controllare l'accesso facendo in modo che il sistema esegua un controllo di accesso.

Per controllare l'accesso alle operazioni che non rientrano nei diritti di accesso predefiniti per gli oggetti nei servizi Dominio di Active Directory, usare la funzionalità di controllo dei diritti di accesso del controllo di accesso in Windows 2000. Per altre informazioni, vedere [**ADS \_ RIGHTS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum).

**Per usare un diritto di accesso di controllo per controllare il diritto di eseguire un'operazione**

1.  Creare un diritto di accesso di controllo che definisce il tipo di accesso all'applicazione o al servizio. Per altre informazioni, vedere [Controllare i diritti di accesso.](control-access-rights.md)
2.  Creare un oggetto in Active Directory Domain Services che rappresenta l'applicazione, il servizio o la risorsa.
3.  Aggiungere le voci ACE dell'oggetto all'elenco DACL nel descrittore di sicurezza degli oggetti per concedere o negare a utenti o gruppi il diritto di accesso di controllo su tale oggetto. Per altre informazioni, vedere [Impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).
4.  Quando un utente tenta di eseguire l'operazione protetta, l'applicazione o il servizio usa la [**funzione AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) per determinare se il diritto di accesso di controllo viene concesso all'utente. Per altre informazioni, vedere [Controllo di un diritto di accesso di controllo nell'ACL di un oggetto](checking-a-control-access-right-in-an-objectampaposs-acl.md).
5.  In base al risultato del controllo di accesso sull'oggetto, l'applicazione o il servizio può concedere o negare all'utente l'accesso all'applicazione o al servizio.

Un'applicazione di servizio può anche creare un gruppo i cui membri sarebbero le varie istanze del servizio. Ad esempio, un servizio con istanze installate in più computer in un'azienda potrebbe avere un file di log comune in cui vengono scrivite tutte le istanze del servizio. Il programma di installazione del servizio crea il file di log e usa un elenco DACL per concedere l'accesso solo ai membri di un gruppo. I membri del gruppo sono gli account utente con cui sono in esecuzione le varie istanze del servizio oppure, se i servizi vengono eseguiti con l'account LocalSystem, i membri saranno gli account computer dei server host.

 

 