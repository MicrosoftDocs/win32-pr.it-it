---
title: Servizi (Windows 7 Developer Guide)
description: Windows 7 offre una piattaforma potente, altamente estendibile e gestibile per la creazione e l'integrazione dei servizi Web e delle applicazioni del futuro. Windows 7 offre API di codice gestito e API native per la compilazione e l'esecuzione di servizi Web.
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42fe2a59a69efe7fb34bb4a09c58b2ee03f00ac8b8129c36b1ef5f0f61971c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203864"
---
# <a name="services-windows-7-developer-guide"></a>Servizi (Windows 7 Developer Guide)

Windows 7 offre una piattaforma potente, altamente estendibile e gestibile per la creazione e l'integrazione dei servizi Web e delle applicazioni del futuro.

Windows 7 offre API di codice gestito e API native per la compilazione e l'esecuzione di servizi Web. Un'ampia gamma di nuove funzionalità si basa su un nuovo livello di estendibilità che consente agli sviluppatori di estendere tutte le API, in codice nativo o all'interno di Microsoft .NET Framework.

Windows 7 consente inoltre agli sviluppatori di sfruttare le migliori funzionalità di memorizzazione nella cache e ricerca. Con questi miglioramenti, gli sviluppatori possono recuperare i dati più velocemente e ridurre l'utilizzo della larghezza di banda di rete.

## <a name="windows-web-services"></a>Windows Servizi Web

Con [Windows servizi Web](/windows/desktop/wsw/portal), è possibile creare applicazioni che comunicano facilmente con un computer locale o un servizio Web remoto. Windows Servizi Web è un'implementazione in codice nativo di SOAP e fornisce la comunicazione di rete di base supportando un'ampia gamma di protocolli della famiglia di servizi Web *(WS).* Windows Servizi Web è un peer to [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) *(WCF,* servizi Web di codice gestito) e fornisce un subset di funzionalità WCF ad *alte* prestazioni. Windows Servizi Web offre i vantaggi seguenti:

-   Possibilità di compilare servizi Web di codice nativo in C/C++ in Windows client e server.
-   Ampia integrazione con [Windows Communication Foundation.](/previous-versions/windows/desktop/cc907054(v=vs.85))
-   Possibilità di compilare servizi Web con un tempo di avvio minimo.
-   Possibilità di creare servizi basati sulla famiglia *di protocolli WS* di base e sugli *standard W3C.*
-   Possibilità di usare i servizi Web in ambienti con risorse limitate.

Per altre informazioni, vedere [Windows WEB Services API](../wsw/portal.md) e Implement Web Services with the Windows Web Services [API](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI).

## <a name="distributed-routing-table"></a>Tabella di routing distribuito

Windows 7 semplifica la creazione di applicazioni peer-to-peer sofisticate come file system distribuiti e reti di distribuzione del contenuto con la [tabella di routing distribuito](/windows/desktop/P2PSdk/distributed-routing-table-api-reference). La tabella di routing distribuito offre un meccanismo sicuro e scalabile per la pubblicazione e la ricerca di chiavi in un sistema peer-to-peer. Può essere usato per compilare tabelle hash distribuite e costruire topologie per reti di sovrapposizione. Vedere [Routing distribuito API Tabella](../p2psdk/distributed-routing-table-api.md).

## <a name="windows-branchcache"></a>**Windows BranchCache**

Windows 7 migliora la velocità di risposta delle applicazioni tra i server centrali e i computer delle succursale. Nelle reti odierne la comunicazione tra server centrali e succursali è spesso congestionata, con conseguente rallentamento delle prestazioni per le applicazioni nella succursale. Con Windows BranchCache, i client possono recuperare dati da altri client nel proprio ramo che hanno già scaricato i dati, anziché dover recuperare i dati su server remoti. Di conseguenza, il traffico dei collegamenti WAN diminuisce e la velocità di risposta dell'applicazione migliora. La cache mantiene una copia di tutto il contenuto richiesto dai client nel ramo e garantisce che solo i client autorizzati dal server di contenuti possano accedere ai dati richiesti, mantenendo la crittografia end-to-end dei dati.

Windows BranchCache è già integrato con HTTP e Server Message Block (SMB). Se un'applicazione usa windowsAPIs per uno di questi protocolli, Windows BranchCache può contribuire ad aumentare le prestazioni dell'applicazione in Windows 7 senza apportare alcuna modifica.

Se l'applicazione recupera gli stessi dati più volte da un server tramite un collegamento WAN e non viene ottimizzata automaticamente con Windows 7, è facile usare le API branchCache di Windows per ottimizzare l'applicazione per lavorare più velocemente in Windows 7 e soddisfare gli utenti del ramo.

Queste nuove funzionalità consentono di ridurre il traffico WAN e la latenza garantendo al tempo stesso la conformità ai requisiti di sicurezza. Vedere [Distribuzione peer.](../p2psdk/peer-distribution.md)

 

 
