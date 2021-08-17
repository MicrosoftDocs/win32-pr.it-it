---
description: Per accedere a un'applicazione server COM+ in modalità remota da un altro computer (client), nel computer client deve essere installato un subset degli attributi dell'applicazione server, incluse le DLL proxy/stub e le librerie dei tipi per la comunicazione remota dell'interfaccia DCOM/QC.
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: Distribuzione di proxy di applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e651338e4bd89cb4fe5cb77789e5e10392f62e065da0f61ec4ea19f7cca312b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547990"
---
# <a name="deploying-application-proxies"></a>Distribuzione di proxy di applicazione

Per accedere a un'applicazione server COM+ in modalità remota da un altro computer (client), nel computer client deve essere installato un subset degli attributi dell'applicazione server, incluse le DLL proxy/stub e le librerie dei tipi per la comunicazione remota dell'interfaccia DCOM/QC. Questo subset è denominato *proxy dell'applicazione.*

Tramite lo strumento di amministrazione Servizi componenti è possibile esportare facilmente un'applicazione server COM+ come proxy di applicazione. Per fare in modo che COM+ generi un proxy di applicazione, è importante che tutti i componenti nell'applicazione server siano stati installati e non importati. Per altre informazioni su questa distinzione, vedere [Importazione di componenti.](importing-components.md) Ciò garantisce che l'applicazione includa tutte le informazioni di registrazione necessarie.

> [!Note]  
> È consigliabile separare le definizioni di interfaccia dalle implementazioni della classe. In caso contrario, il set di DLL o librerie dei tipi incluso nel proxy dell'applicazione COM+ includerà il codice server effettivo.

 

I proxy dell'applicazione generati da COM+ sono Windows pacchetti di installazione del programma di installazione. Dopo l'installazione, i proxy dell'applicazione vengono visualizzati nel pannello di controllo Installazione applicazioni del computer client (a meno che il file .msi non venga modificato usando uno strumento di creazione del programma di installazione di Windows).

## <a name="remote-access-via-application-proxies"></a>Accesso remoto tramite proxy di applicazione

Quando si genera un proxy di applicazione, COM+ fornisce automaticamente le informazioni seguenti, necessarie per l'accesso remoto a un'applicazione server COM+:

-   Informazioni sull'identità della classe (CLSID e ProgID). Un proxy di applicazione supporta fino a due ProgID.
-   Identità dell'applicazione e relazione delle classi con le applicazioni (AppID).
-   Informazioni sulla posizione per ogni applicazione (Nome server remoto).
-   Informazioni di marshalling per tutte le interfacce esposte dall'applicazione, ad esempio librerie dei tipi e proxy/stub.
-   Nomi e identificatori delle code MSMQ (se il servizio dei componenti in coda è abilitato per l'applicazione).
-   Attributi di classe, interfaccia e metodo, escluse le informazioni sui ruoli.
-   Attributi dell'applicazione.

## <a name="installing-application-proxies-on-other-operating-systems"></a>Installazione di proxy di applicazione in altri sistemi operativi

A differenza delle applicazioni server COM+, i proxy delle applicazioni possono essere installati in qualsiasi sistema operativo che supporta DCOM (e Windows programma di installazione). Nei computer che non eseguono COM+, viene installato solo il subset di informazioni necessarie per la comunicazione remota DCOM. Queste informazioni vengono installate nel Registro di Windows (usando le chiavi HKEY \_ CLASSES \_ ROOT, APPID/CLSID).

> [!Note]  
> Quando si installa un proxy di applicazione (file .msi) in computer che non eseguono COM+, è necessario che Windows Programma di installazione sia in esecuzione in tali computer. È consigliabile che gli sviluppatori spedino il file Windows Installer redistributable (instmsi.exe) insieme al file .msi dell'applicazione. Ciò garantisce che gli amministratori di sistema Windows programma di installazione di durante la distribuzione di proxy di applicazione nei client che non eseguono COM+.

 

Nei computer che eseguono COM+, le informazioni sul proxy dell'applicazione vengono installate nel catalogo COM+ ed è visibile nello strumento di amministrazione Servizi componenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di pacchetti di installazione per applicazioni COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Catalogo COM+](the-com--catalog.md)
</dt> <dt>

[Utilità di replica COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



