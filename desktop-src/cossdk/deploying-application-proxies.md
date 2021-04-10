---
description: Per accedere a un'applicazione server COM+ in modalità remota da un altro computer (client), il computer client deve disporre di un subset degli attributi dell'applicazione server installata, incluse le DLL proxy/stub e le librerie dei tipi per la comunicazione remota dell'interfaccia DCOM/QC.
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: Distribuzione di proxy di applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5e6439574602005ca53917945fa9005f8959b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966379"
---
# <a name="deploying-application-proxies"></a>Distribuzione di proxy di applicazione

Per accedere a un'applicazione server COM+ in modalità remota da un altro computer (client), il computer client deve disporre di un subset degli attributi dell'applicazione server installata, incluse le DLL proxy/stub e le librerie dei tipi per la comunicazione remota dell'interfaccia DCOM/QC. Questo subset è denominato *proxy di applicazione*.

Tramite lo strumento di amministrazione Servizi componenti è possibile esportare facilmente un'applicazione server COM+ come proxy di applicazione. Affinché COM+ generi un proxy di applicazione, è importante che tutti i componenti dell'applicazione server siano stati installati e non importati. Per ulteriori informazioni su questa distinzione, vedere [importazione di componenti](importing-components.md). In questo modo si garantisce che l'applicazione includa tutte le informazioni di registrazione necessarie.

> [!Note]  
> È consigliabile separare le definizioni di interfaccia dalle implementazioni della classe. In caso contrario, il set di dll o librerie dei tipi incluso nel proxy di applicazione COM+ includerà il codice server effettivo.

 

I proxy di applicazione generati da COM+ sono Windows Installer pacchetti di installazione. Al termine dell'installazione, i proxy dell'applicazione vengono visualizzati nel pannello di controllo Installazione applicazioni del computer client, a meno che il file con estensione msi non venga modificato utilizzando uno strumento di creazione Windows Installer.

## <a name="remote-access-via-application-proxies"></a>Accesso remoto tramite proxy di applicazione

Quando si genera un proxy di applicazione, COM+ fornisce automaticamente le informazioni seguenti, necessarie per l'accesso remoto a un'applicazione server COM+ da parte del proxy dell'applicazione:

-   Informazioni sull'identità della classe (CLSID e ProgID). Un proxy di applicazione supporta fino a due ProgID.
-   Identità dell'applicazione e relazione delle classi con le applicazioni (AppID).
-   Informazioni sulla posizione per applicazione (nome server remoto).
-   Informazioni di marshalling per tutte le interfacce esposte dall'applicazione, ad esempio librerie dei tipi e proxy/stub.
-   Identificatori e nomi di coda MSMQ, se il servizio componenti in coda è abilitato per l'applicazione.
-   Attributi di classi, interfacce e metodi, escluse le informazioni sui ruoli.
-   Attributi dell'applicazione.

## <a name="installing-application-proxies-on-other-operating-systems"></a>Installazione di proxy di applicazione su altri sistemi operativi

Diversamente dalle applicazioni server COM+, i proxy di applicazione possono essere installati in qualsiasi sistema operativo che supporta DCOM (e Windows Installer). Nei computer che non eseguono COM+, viene installato solo il subset di informazioni necessarie per la comunicazione remota DCOM. Queste informazioni vengono installate nel registro di sistema di Windows (usando \_ le \_ chiavi radice delle classi hKey, AppID/CLSID).

> [!Note]  
> Quando si installa un proxy di applicazione (file con estensione msi) in computer in cui non è in esecuzione COM+, è necessario che Windows Installer sia in esecuzione in tali computer. Si consiglia agli sviluppatori di distribuire il file ridistribuibile Windows Installer (instmsi.exe) insieme al file con estensione msi dell'applicazione. In questo modo gli amministratori di sistema avranno Windows Installer disponibili quando distribuiscono proxy di applicazione su client che non eseguono COM+.

 

Nei computer che eseguono COM+, le informazioni sul proxy di applicazione vengono installate nel catalogo COM+ ed è visibile nello strumento di amministrazione Servizi componenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di pacchetti di installazione per applicazioni COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Catalogo COM+](the-com--catalog.md)
</dt> <dt>

[Utilità di replica COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



