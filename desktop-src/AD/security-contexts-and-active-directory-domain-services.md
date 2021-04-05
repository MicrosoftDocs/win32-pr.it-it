---
title: Contesti di sicurezza e Active Directory Domain Services
description: Quando un'applicazione viene associata a un controller di Dominio di Active Directory (DC), viene eseguita nel contesto di sicurezza di un'entità di sicurezza, che può essere un utente o un'entità, ad esempio un computer o un servizio di sistema.
ms.assetid: 7ad0acbe-f81b-46d6-be87-3526b0bfbd1b
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, contesti di sicurezza
- contesti di sicurezza Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c337cb05f8158dbb90f231652c42fb10a486aef4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046486"
---
# <a name="security-contexts-and-active-directory-domain-services"></a>Contesti di sicurezza e Active Directory Domain Services

Quando un'applicazione viene associata a un controller di Dominio di Active Directory (DC), viene eseguita nel contesto di sicurezza di un'entità di sicurezza, che può essere un utente o un'entità, ad esempio un computer o un servizio di sistema. Il contesto di sicurezza è l'account utente utilizzato dal sistema per applicare la sicurezza quando un thread tenta di accedere a un oggetto a protezione diretta. Questi dati includono l'ID di sicurezza (SID) dell'utente, le appartenenze ai gruppi e i privilegi.

Un utente stabilisce un contesto di sicurezza presentando le credenziali per l'autenticazione. Se le credenziali vengono autenticate, il sistema produce un token di accesso che identifica le appartenenze ai gruppi e i privilegi associati all'account utente. Il sistema verifica il token di accesso quando si tenta di accedere a un oggetto directory. Confronta i dati nel token di accesso con gli account e i gruppi a cui è stato concesso o negato l'accesso da parte del descrittore di sicurezza dell'oggetto.

Usare i metodi seguenti per controllare il contesto di sicurezza con cui si esegue l'associazione a un Active Directory DC:

-   Eseguire l'associazione con l'opzione **Ads \_ Secure \_ Authentication** con la funzione [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) o il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) e specificare in modo esplicito un nome utente e una password. Il sistema autentica queste credenziali e genera un token di accesso usato per la verifica dell'accesso per la durata di tale associazione. Per altre informazioni, vedere [Autenticazione](authentication.md).
-   Eseguire l'associazione con l'opzione **Ads \_ Secure \_ Authentication** , ma senza specificare le credenziali. Se non si esegue la rappresentazione di un utente, il sistema utilizza il contesto di sicurezza primario dell'applicazione, ovvero il contesto di sicurezza dell'utente che ha avviato l'applicazione. Nel caso di un servizio di sistema, si tratta del contesto di sicurezza dell'account del servizio o dell'account LocalSystem.
-   Rappresentare un utente e quindi eseguire l'associazione con **\_ \_ l'autenticazione protetta ADS**, ma senza specificare le credenziali. In questo caso, il sistema utilizza il contesto di sicurezza del client rappresentato. Per ulteriori informazioni, vedere [rappresentazione client](/windows/desktop/SecAuthZ/client-impersonation).
-   Eseguire l'associazione tramite [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) con l'opzione **Ads \_ No \_ Authentication** . Questo metodo viene associato senza autenticazione e restituisce "Everyone" come contesto di sicurezza. Questa opzione è supportata solo dal provider LDAP.

Se possibile, eseguire il binding senza specificare le credenziali. Ovvero utilizzare il contesto di sicurezza dell'utente connesso o il client rappresentato. Questo consente di evitare la memorizzazione delle credenziali nella cache. Se è necessario utilizzare credenziali utente alternative, richiedere le credenziali, associarle, ma non memorizzarle nella cache. Per usare lo stesso contesto di sicurezza in più operazioni di binding, è possibile specificare il nome utente e la password per la prima operazione di binding e quindi specificare solo il nome utente per eseguire le associazioni successive. Per ulteriori informazioni sull'utilizzo di questa tecnica, vedere [Authentication](authentication.md).

Alcuni contesti di sicurezza sono più potenti di altri. Ad esempio, l'account LocalSystem in un controller di dominio ha accesso completo ai Active Directory Domain Services, mentre un utente tipico ha solo accesso limitato a alcuni degli oggetti nella directory. In generale, l'applicazione non deve essere eseguita in un contesto di sicurezza avanzato, ad esempio LocalSystem, quando un contesto di sicurezza meno potente è sufficiente per eseguire le operazioni. Ciò significa che è possibile suddividere l'applicazione in componenti distinti, ognuno dei quali viene eseguito in un contesto di sicurezza appropriato per le operazioni da eseguire. Ad esempio, il programma di installazione dell'applicazione può essere suddiviso nel modo seguente:

-   Eseguire modifiche allo schema ed estensioni nel contesto di un utente membro del gruppo Schema Administrators.
-   Eseguire modifiche al contenitore di configurazione nel contesto di un utente membro del gruppo Enterprise Administrators.
-   Eseguire le modifiche del contenitore di dominio nel contesto di un utente membro del gruppo Domain Administrators.

 

 