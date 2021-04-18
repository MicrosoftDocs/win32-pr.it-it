---
title: Servizi (Guida per sviluppatori di Windows 7)
description: Windows 7 offre una piattaforma potente, estremamente estendibile e gestibile per la creazione e l'integrazione dei servizi Web e delle applicazioni del futuro. Windows 7 offre API del codice gestito e API native per la compilazione e l'esecuzione di servizi Web.
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aab84cbb522f21b9a09a85d80ef25bf1c858baf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300750"
---
# <a name="services-windows-7-developer-guide"></a>Servizi (Guida per sviluppatori di Windows 7)

Windows 7 offre una piattaforma potente, estremamente estendibile e gestibile per la creazione e l'integrazione dei servizi Web e delle applicazioni del futuro.

Windows 7 offre API del codice gestito e API native per la compilazione e l'esecuzione di servizi Web. Una serie di nuove funzionalità si basa su un nuovo livello di estensibilità che consente agli sviluppatori di estendere tutte le API, nel codice nativo o all'interno del Framework Microsoft .NET.

Windows 7 consente inoltre agli sviluppatori di sfruttare al meglio le funzionalità di memorizzazione nella cache e di ricerca. Con questi miglioramenti, gli sviluppatori possono recuperare i dati più velocemente e ridurre l'utilizzo della larghezza di banda di rete.

## <a name="windows-web-services"></a>Servizi Web Windows

Con i [servizi Web Windows](/windows/desktop/wsw/portal), è possibile creare applicazioni che comunicano con facilità con un computer locale o un servizio Web remoto. Servizi Web Windows è un'implementazione di codice nativo di SOAP e fornisce la comunicazione di rete principale grazie al supporto di un'ampia gamma di protocolli (Web Services,*WS*). Servizi Web Windows è un peer to [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) (*WCF*, servizi Web di codice gestito) e fornisce un sottoinsieme a prestazioni elevate della funzionalità *WCF* . Servizi Web Windows offre i seguenti vantaggi:

-   Possibilità di compilare servizi Web di codice nativo in C/C++ nel client e nel server Windows.
-   Integrazione completa con [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) Services.
-   Possibilità di creare servizi Web con tempi di avvio minimi.
-   La possibilità di creare servizi basati sulla famiglia di protocolli *WS* di base e standard *W3C* .
-   Possibilità di utilizzare i servizi Web in ambienti con vincoli di risorse.

Per ulteriori informazioni, vedere l' [API dei servizi Web Windows](../wsw/portal.md) e [implementare i servizi Web con l'API dei servizi Web Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI).

## <a name="distributed-routing-table"></a>Tabella di routing distribuita

Windows 7 semplifica la creazione di applicazioni peer-to-peer sofisticate come file system distribuiti e reti di distribuzione del contenuto con la [tabella di routing distribuita](/windows/desktop/P2PSdk/distributed-routing-table-api-reference). La tabella di routing distribuita fornisce un meccanismo sicuro e scalabile per la pubblicazione e la ricerca di chiavi in un sistema peer-to-peer. Può essere utilizzato per compilare tabelle hash distribuite e creare topologie per le reti sovrapposte. Vedere [API tabella di routing distribuito](../p2psdk/distributed-routing-table-api.md).

## <a name="windows-branchcache"></a>**Windows BranchCache**

Windows 7 migliora la velocità di risposta dell'applicazione tra i server centrali e i computer delle succursali. Nelle reti attuali la comunicazione tra i server centrali e le succursali è spesso congestionata, il che comporta prestazioni più lente per le applicazioni nella succursale. Con Windows BranchCache, i client possono recuperare i dati da altri client nel proprio branch che hanno già scaricato i dati, anziché dover recuperare i dati su server remoti. Di conseguenza, il traffico di collegamento di Wide Area Network (WAN) diminuisce e migliora la velocità di risposta dell'applicazione. La cache mantiene una copia di tutto il contenuto richiesto dai client nel ramo e garantisce che solo i client autorizzati dal server di contenuti possano accedere ai dati richiesti, mantenendo al tempo stesso la crittografia end-to-end dei dati.

Windows BranchCache è già integrato con HTTP e Server Message Block (SMB). Se un'applicazione utilizza WindowsAPIs per uno di questi protocolli, Windows BranchCache può contribuire a migliorare le prestazioni dell'applicazione in Windows 7 senza apportare alcuna modifica.

Se l'applicazione recupera più volte gli stessi dati da un server su un collegamento WAN e non viene ottimizzata automaticamente con Windows 7, è facile utilizzare Windows BranchCacheAPIs per ottimizzare l'applicazione in modo che funzioni più velocemente in Windows 7 e soddisfi gli utenti del ramo.

Queste nuove funzionalità consentono di ridurre il traffico e la latenza WAN garantendo al contempo la conformità ai requisiti di sicurezza. Vedere [distribuzione peer](../p2psdk/peer-distribution.md).

 

 
