---
description: Le raccolte di amministrazione COM+ consentono di conservare e organizzare i dati di configurazione archiviati nel catalogo COM+.
ms.assetid: eed8ca97-39ad-4188-afc6-8670b5073fad
title: Raccolte di amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb49ecd382e5a5a570e3e479714ad905a5eaf5f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104553416"
---
# <a name="com-administration-collections"></a>Raccolte di amministrazione COM+

Le raccolte di amministrazione COM+ consentono di conservare e organizzare i dati di configurazione archiviati nel catalogo COM+. Le raccolte corrispondono alle cartelle nell'albero della console dello strumento di amministrazione Servizi componenti. È possibile accedere a queste raccolte utilizzando gli oggetti e le interfacce COM+ Administration.

L'amministrazione a livello di codice viene avviata usando gli oggetti creati dalla classe [**COMAdminCatalog**](comadmincatalog.md) , si rappresenta qualsiasi raccolta nel catalogo usando oggetti creati dalla classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e si rappresentano gli elementi nelle raccolte usando oggetti creati dalla classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Gli elementi di una raccolta specifica espongono un set di proprietà coerente. Ogni elemento nella raccolta [**Components**](components.md) rappresenta ad esempio un componente e gli elementi nella raccolta **Components** espongono le stesse proprietà usate per configurare un componente. È possibile accedere a queste proprietà tramite la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

> [!Note]  
> Le proprietà con accesso WriteOnce sono ReadWrite quando si usa il metodo [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) e sono successivamente ReadOnly.

 

Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [automazione dell'amministrazione com+](automating-com--administration.md).

## <a name="collection-hierarchy"></a>Gerarchia della raccolta

Nella figura seguente vengono illustrate le relazioni tra le raccolte. Le raccolte all'estrema sinistra (nelle caselle bianco e grigio) sono raccolte di primo livello, accessibili chiamando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) di un oggetto creato dalla classe [**COMAdminCatalog**](comadmincatalog.md) . Le raccolte rimanenti (in caselle gialle) possono essere accessibili solo tramite la relativa raccolta padre, chiamando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) che rappresenta il relativo elemento padre. Le frecce puntano da una raccolta padre alle relative raccolte figlio.

![Diagramma che mostra le relazioni tra le raccolte.](images/ab61b0ab-2368-4bd8-9cfc-b7adc5beaca3.png)

Le quattro raccolte seguenti non sono illustrate nella figura: [**errorInfo**](errorinfo.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md)e [**root**](root.md). La raccolta **errorInfo** è un elemento figlio di ogni raccolta nella figura ad eccezione di [**InprocServers**](inprocservers.md) e [**WOWInprocServers**](wowinprocservers.md) (in caselle grigie). Le raccolte **PropertyInfo** e **RelatedCollectionInfo** sono elementi figlio di ogni raccolta. La raccolta **radice** è una raccolta di livello principale che è l'elemento padre di tutte le altre raccolte di primo livello. Tuttavia, non è necessario accedere alla raccolta **radice** prima di accedere ad altre raccolte di primo livello.

## <a name="comadmin-library"></a>Libreria COMAdmin

Le raccolte seguenti sono supportate dalla libreria COMAdmin.



| Raccolta                                                             | Descrizione                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationCluster**](applicationcluster.md)                       | Contiene un elenco dei server nel cluster di applicazioni.                                                                                            |
| [**ApplicationInstances**](applicationinstances.md)                   | Contiene un oggetto per ogni istanza di un'applicazione COM+ in esecuzione.                                                                                   |
| [**Applicazioni**](applications.md)                                   | Contiene un oggetto per ogni applicazione COM+ installata nel computer locale.                                                                         |
| [**Componenti**](components.md)                                       | Contiene un oggetto per ogni componente nell'applicazione a cui è correlato.                                                                      |
| [**Computer**](computerlist.md)                                   | Contiene un elenco dei computer disponibili nella cartella **computer** dello strumento di amministrazione Servizi componenti.                                     |
| [**DCOMProtocols**](dcomprotocols.md)                                 | Contiene un elenco dei protocolli che devono essere utilizzati da DCOM. Contiene un oggetto per ogni protocollo.                                                         |
| [**ErrorInfo**](errorinfo.md)                                         | Recupera informazioni dettagliate sugli errori relativi ai metodi che gestiscono più oggetti.                                                               |
| [**EventClassesForIID**](eventclassesforiid.md)                       | Recupera le informazioni relative alle classi di evento.                                                                                                        |
| [**FilesForImport**](filesforimport.md)                               | Recupera le informazioni dal file MSI relativo a un'applicazione che può essere importata.                                                                    |
| [**InprocServers**](inprocservers.md)                                 | Contiene un elenco dei server in-process registrati con il sistema. Contiene un oggetto per ogni componente.                                       |
| [**InterfacesForComponent**](interfacesforcomponent.md)               | Contiene un oggetto per ogni interfaccia esposta dal componente a cui è correlata la raccolta.                                                    |
| [**LegacyComponents**](legacycomponents.md)                           | Contiene un oggetto per ogni componente non configurato nell'applicazione a cui è correlato.                                                         |
| [**LegacyServers**](legacyservers.md)                                 | Identico alla raccolta [**InprocServers**](inprocservers.md) con la differenza che questa raccolta include anche server locali.                           |
| [**LocalComputer**](localcomputer.md)                                 | Contiene un singolo oggetto che contiene le informazioni sulle impostazioni a livello di computer per il computer di cui si desidera accedere al catalogo.                             |
| [**MethodsForInterface**](methodsforinterface.md)                     | Contiene un oggetto per ogni metodo sull'interfaccia a cui è correlata la raccolta.                                                               |
| [**Partizioni**](partitions.md)                                       | Utilizzato per specificare le applicazioni contenute in ogni partizione.                                                                                         |
| [**PartitionUsers**](partitionusers.md)                               | Utilizzato per specificare gli utenti contenuti in ogni partizione.                                                                                                |
| [**PropertyInfo**](propertyinfo.md)                                   | Recupera le informazioni sulle proprietà supportate da una raccolta specificata.                                                                      |
| [**PublisherProperties**](publisherproperties.md)                     | Contiene un oggetto per ogni proprietà del server di pubblicazione per la raccolta [**SubscriptionsForComponent**](subscriptionsforcomponent.md) padre.              |
| [**RelatedCollectionInfo**](relatedcollectioninfo.md)                 | Recupera informazioni su altre raccolte correlate alla raccolta dalla quale viene chiamato.                                                      |
| [**Ruoli**](roles.md)                                                 | Contiene un oggetto per ogni ruolo assegnato all'applicazione a cui è correlato.                                                                  |
| [**RolesForComponent**](rolesforcomponent.md)                         | Contiene un oggetto per ogni ruolo assegnato al componente a cui è correlata la raccolta.                                                        |
| [**RolesForInterface**](rolesforinterface.md)                         | Contiene un oggetto per ogni ruolo assegnato all'interfaccia a cui è correlata la raccolta.                                                        |
| [**RolesForMethod**](rolesformethod.md)                               | Contiene un oggetto per ogni ruolo assegnato al metodo al quale è correlata la raccolta.                                                           |
| [**RolesForPartition**](rolesforpartition.md)                         | Contiene un oggetto per ogni ruolo assegnato alla partizione a cui è correlata la raccolta.                                                        |
| [**Radice**](root.md)                                                   | Contiene le raccolte di primo livello nel catalogo.                                                                                                    |
| [**SubscriberProperties**](subscriberproperties.md)                   | Contiene un oggetto per ogni proprietà del Sottoscrittore per la raccolta [**SubscriptionsForComponent**](subscriptionsforcomponent.md) padre.             |
| [**SubscriptionsForComponent**](subscriptionsforcomponent.md)         | Contiene un oggetto per ogni sottoscrizione per la raccolta di [**componenti**](components.md) padre.                                                  |
| [**TransientPublisherProperties**](transientpublisherproperties.md)   | Contiene un oggetto per ogni proprietà del server di pubblicazione per la raccolta [**TransientSubscriptions**](transientsubscriptions.md) padre.                    |
| [**TransientSubscriberProperties**](transientsubscriberproperties.md) | Contiene un oggetto per ogni proprietà del Sottoscrittore per la raccolta [**TransientSubscriptions**](transientsubscriptions.md) padre.                   |
| [**TransientSubscriptions**](transientsubscriptions.md)               | Contiene un oggetto per ogni sottoscrizione temporanea.                                                                                                   |
| [**UsersInPartitionRole**](usersinpartitionrole.md)                   | Contiene un oggetto per ogni utente nel ruolo di partizione a cui è correlata la raccolta.                                                            |
| [**UsersInRole**](usersinrole.md)                                     | Contiene un oggetto per ogni utente nel ruolo a cui è correlata la raccolta.                                                                      |
| [**WOWInprocServers**](wowinprocservers.md)                           | Contiene un elenco dei server in-process registrati con il sistema per i componenti a 32 bit nei computer a 64 bit.                                       |
| [**WOWLegacyServers**](wowlegacyservers.md)                           | Identico alla raccolta [**LegacyServers**](legacyservers.md) con la differenza che questa raccolta viene disegnata dal registro di sistema a 32 bit nei computer a 64 bit. |



 

 

 



