---
description: COMREPL è un'utilità che consente di replicare il catalogo COM+ da un computer di origine specifico a uno o più computer di destinazione.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: Utilità di replica COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966283"
---
# <a name="the-comrepl-replication-utility"></a>Utilità di replica COMREPL

COMREPL è un'utilità che consente di replicare il catalogo COM+ da un computer di origine specifico a uno o più computer di destinazione. Si pensi al computer di origine che rappresenta una "configurazione Master". COMREPL viene utilizzato per replicare questa configurazione Master per mantenere un set di computer configurati in modo identico.

L'unità di replica è l'intera configurazione COM+ nel computer master. Tutte le applicazioni COM+ nel database master vengono replicate nei computer di destinazione. tutto o niente. Inoltre, tutte le applicazioni COM+ installate in precedenza nei computer di destinazione, ad eccezione delle applicazioni COM+ preinstallate, verranno eliminate come parte del processo di replica.

COMREPL replica solo i dati di configurazione COM+. Sono incluse le applicazioni COM+ e le impostazioni specifiche del computer COM+. Microsoft Internet Information Services (IIS) ha un'utilità simile (IISSync) che usa COMREPL per replicare la configurazione di IIS e COM+.

Per informazioni dettagliate sull'avvio e sull'uso di COMREPL, vedere gli argomenti seguenti in questa sezione:

-   [Uso di COMREPL](using-comrepl.md)
-   [Cosa viene replicato](what-gets-replicated.md)
-   [Fasi di replica](replication-phases.md)
-   [Gestione dei file](file-management.md)
-   [Registrazione e segnalazione errori](logging-and-error-reporting.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di pacchetti di installazione per applicazioni COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Distribuzione di proxy di applicazione](deploying-application-proxies.md)
</dt> <dt>

[Catalogo COM+](the-com--catalog.md)
</dt> </dl>

 

 



