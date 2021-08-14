---
description: Le raccolte di amministrazione COM+ servono a contenere e organizzare i dati di configurazione archiviati nel catalogo COM+.
ms.assetid: eed8ca97-39ad-4188-afc6-8670b5073fad
title: Raccolte di amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc19ff14959c151dc5736fb4a52c5346d0f5a30b6565551aca2f0edb3cee61b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308443"
---
# <a name="com-administration-collections"></a>Raccolte di amministrazione COM+

Le raccolte di amministrazione COM+ servono a contenere e organizzare i dati di configurazione archiviati nel catalogo COM+. Le raccolte corrispondono alle cartelle nell'albero della console dello strumento di amministrazione Servizi componenti. È possibile accedere a queste raccolte usando le interfacce e gli oggetti di amministrazione COM+.

L'amministrazione a livello di codice viene avviata usando oggetti creati dalla classe [**COMAdminCatalog,**](comadmincatalog.md) si rappresentano le raccolte nel catalogo usando gli oggetti creati dalla classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e si rappresentano gli elementi nelle raccolte usando oggetti creati dalla [**classe COMAdminCatalogObject.**](comadmincatalogobject.md)

Gli elementi in una raccolta specificata espongono un set coerente di proprietà. Ad esempio, ogni elemento nella raccolta [**Components**](components.md) rappresenta un componente e gli elementi nella raccolta **Components** espongono le stesse proprietà usate per configurare un componente. È possibile accedere a queste proprietà usando la [**classe COMAdminCatalogObject.**](comadmincatalogobject.md)

> [!Note]  
> Le proprietà con accesso WriteOnce sono ReadWrite quando si usa il [**metodo Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) prima di [**usare SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) e sono readonly in un secondo momento.

 

Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [Automazione dell'amministrazione COM+.](automating-com--administration.md)

## <a name="collection-hierarchy"></a>Gerarchia di raccolte

La figura seguente illustra le relazioni tra le raccolte. Le raccolte all'estrema sinistra (in caselle vuote e grigie) sono raccolte di primo livello a cui si accede chiamando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) di un oggetto creato dalla [**classe COMAdminCatalog.**](comadmincatalog.md) Le raccolte rimanenti (in caselle gialle) sono accessibili solo tramite la relativa raccolta padre, chiamando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) che rappresenta il relativo elemento padre. Le frecce puntano da una raccolta padre alle raccolte figlio.

![Diagramma che mostra le relazioni tra le raccolte.](images/ab61b0ab-2368-4bd8-9cfc-b7adc5beaca3.png)

Le quattro raccolte seguenti non sono illustrate nella figura: [**ErrorInfo**](errorinfo.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md)e [**Root**](root.md). La **raccolta ErrorInfo** è un elemento figlio di ogni raccolta nella figura, ad eccezione di [**InprocServers**](inprocservers.md) e [**WOWInprocServers**](wowinprocservers.md) (in caselle grigie). Le **raccolte PropertyInfo** **e RelatedCollectionInfo** sono elementi figlio di ogni raccolta. La **raccolta Radice** è una raccolta di primo livello padre di tutte le altre raccolte di primo livello. Tuttavia, non è necessario accedere alla raccolta **Radice** prima di accedere ad altre raccolte di primo livello.

## <a name="comadmin-library"></a>Libreria COMAdmin

Le raccolte seguenti sono supportate dalla libreria COMAdmin.



| Raccolta                                                             | Descrizione                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationCluster**](applicationcluster.md)                       | Contiene un elenco dei server nel cluster di applicazioni.                                                                                            |
| [**ApplicationInstances**](applicationinstances.md)                   | Contiene un oggetto per ogni istanza di un'applicazione COM+ in esecuzione.                                                                                   |
| [**Applicazioni**](applications.md)                                   | Contiene un oggetto per ogni applicazione COM+ installata nel computer locale.                                                                         |
| [**Componenti**](components.md)                                       | Contiene un oggetto per ogni componente dell'applicazione a cui è correlato.                                                                      |
| [**Elenco computer**](computerlist.md)                                   | Contiene un elenco dei computer disponibili nella cartella **Computer** dello strumento di amministrazione Servizi componenti.                                     |
| [**DCOMProtocols**](dcomprotocols.md)                                 | Contiene un elenco dei protocolli che devono essere utilizzati da DCOM. Contiene un oggetto per ogni protocollo.                                                         |
| [**Errorinfo**](errorinfo.md)                                         | Recupera informazioni estese sugli errori relativi ai metodi che riguardano più oggetti.                                                               |
| [**EventClassesForIID**](eventclassesforiid.md)                       | Recupera informazioni relative alle classi di evento.                                                                                                        |
| [**FilesForImport**](filesforimport.md)                               | Recupera dal file MSI informazioni su un'applicazione che può essere importata.                                                                    |
| [**InprocServers**](inprocservers.md)                                 | Contiene un elenco dei server in-process registrati con il sistema. Contiene un oggetto per ogni componente.                                       |
| [**InterfacesForComponent**](interfacesforcomponent.md)               | Contiene un oggetto per ogni interfaccia esposta dal componente a cui è correlata la raccolta.                                                    |
| [**LegacyComponents**](legacycomponents.md)                           | Contiene un oggetto per ogni componente non configurato nell'applicazione a cui è correlato.                                                         |
| [**LegacyServers**](legacyservers.md)                                 | Identica alla raccolta [**InprocServers,**](inprocservers.md) ad eccezione del fatto che questa raccolta include anche server locali.                           |
| [**Computer locale**](localcomputer.md)                                 | Contiene un singolo oggetto che contiene informazioni sulle impostazioni a livello di computer per il computer a cui si accede al catalogo.                             |
| [**MethodsForInterface**](methodsforinterface.md)                     | Contiene un oggetto per ogni metodo nell'interfaccia a cui è correlata la raccolta.                                                               |
| [**Partizioni**](partitions.md)                                       | Consente di specificare le applicazioni contenute in ogni partizione.                                                                                         |
| [**PartitionUsers**](partitionusers.md)                               | Consente di specificare gli utenti contenuti in ogni partizione.                                                                                                |
| [**Propertyinfo**](propertyinfo.md)                                   | Recupera informazioni sulle proprietà supportate da una raccolta specificata.                                                                      |
| [**Proprietà server di pubblicazione**](publisherproperties.md)                     | Contiene un oggetto per ogni proprietà publisher per la [**raccolta SubscriptionsForComponent**](subscriptionsforcomponent.md) padre.              |
| [**RelatedCollectionInfo**](relatedcollectioninfo.md)                 | Recupera informazioni su altre raccolte correlate alla raccolta da cui viene chiamato.                                                      |
| [**Ruoli**](roles.md)                                                 | Contiene un oggetto per ogni ruolo assegnato all'applicazione a cui è correlato.                                                                  |
| [**RolesForComponent**](rolesforcomponent.md)                         | Contiene un oggetto per ogni ruolo assegnato al componente a cui è correlata la raccolta.                                                        |
| [**RolesForInterface**](rolesforinterface.md)                         | Contiene un oggetto per ogni ruolo assegnato all'interfaccia a cui è correlata la raccolta.                                                        |
| [**RolesForMethod**](rolesformethod.md)                               | Contiene un oggetto per ogni ruolo assegnato al metodo a cui è correlata la raccolta.                                                           |
| [**RolesForPartition**](rolesforpartition.md)                         | Contiene un oggetto per ogni ruolo assegnato alla partizione a cui è correlata la raccolta.                                                        |
| [**Radice**](root.md)                                                   | Contiene le raccolte di primo livello nel catalogo.                                                                                                    |
| [**Proprietà Sottoscrittore**](subscriberproperties.md)                   | Contiene un oggetto per ogni proprietà del sottoscrittore per la [**raccolta SubscriptionsForComponent**](subscriptionsforcomponent.md) padre.             |
| [**SubscriptionsForComponent**](subscriptionsforcomponent.md)         | Contiene un oggetto per ogni sottoscrizione per la raccolta [**components**](components.md) padre.                                                  |
| [**Proprietà del server di pubblicazione temporaneo**](transientpublisherproperties.md)   | Contiene un oggetto per ogni proprietà del server di pubblicazione per la [**raccolta TransientSubscriptions**](transientsubscriptions.md) padre.                    |
| [**TransientSubscriberProperties**](transientsubscriberproperties.md) | Contiene un oggetto per ogni proprietà del sottoscrittore per la [**raccolta TransientSubscriptions**](transientsubscriptions.md) padre.                   |
| [**TransientSubscriptions**](transientsubscriptions.md)               | Contiene un oggetto per ogni sottoscrizione temporanea.                                                                                                   |
| [**UsersInPartitionRole**](usersinpartitionrole.md)                   | Contiene un oggetto per ogni utente nel ruolo di partizione a cui è correlata la raccolta.                                                            |
| [**UsersInRole**](usersinrole.md)                                     | Contiene un oggetto per ogni utente nel ruolo a cui è correlata la raccolta.                                                                      |
| [**WOWInprocServers**](wowinprocservers.md)                           | Contiene un elenco dei server in-process registrati con il sistema per i componenti a 32 bit nei computer a 64 bit.                                       |
| [**WOWLegacyServers**](wowlegacyservers.md)                           | Identica alla [**raccolta LegacyServers,**](legacyservers.md) ad eccezione del fatto che questa raccolta viene disegnata dal Registro di sistema a 32 bit nei computer a 64 bit. |



 

 

 



