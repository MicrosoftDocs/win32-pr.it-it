---
title: Linee guida per più utenti
description: Linee guida per lo sviluppo di applicazioni per più utenti in un ambiente Servizi Desktop remoto.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298885"
---
# <a name="multiple-user-guidelines"></a>Linee guida per più utenti

Nelle sezioni seguenti vengono fornite le linee guida per lo sviluppo di applicazioni per più utenti in un ambiente Servizi Desktop remoto.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Configurazione dell'applicazione](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

L'installazione di un'applicazione per un singolo utente può creare problemi in un ambiente multiutente Servizi Desktop remoto.

</dd> <dt>

[Archiviazione di informazioni specifiche dell'utente](storing-user-specific-information.md)
</dt> <dd>

Le applicazioni devono archiviare le informazioni specifiche dell'utente in percorsi specifici dell'utente, separatamente da informazioni globali che si applicano a tutti gli utenti.

</dd> <dt>

[Spazi dei nomi dell'oggetto kernel](kernel-object-namespaces.md)
</dt> <dd>

Servizi Desktop remoto usa più spazi dei nomi per gli oggetti kernel; uno spazio dei nomi globale viene utilizzato principalmente dai servizi nelle applicazioni client/server.

</dd> <dt>

[Indirizzi IP e nomi di computer](ip-addresses-and-computer-names.md)
</dt> <dd>

Non è opportuno presupporre che il nome del computer o l' indirizzo IP assegnato al computer sia associato a un singolo utente poiché più utenti possono accedere contemporaneamente a un server Host sessione Desktop remoto.

</dd> </dl>

Come sempre, bloccare i file e i database durante le modifiche per evitare la perdita accidentale di dati.

L'applicazione non deve bloccare i file dell'applicazione in fase di esecuzione che non sono file per utente. I file di runtime bloccati possono impedire l'esecuzione di più istanze dell'applicazione o di processi nell'applicazione, ad esempio procedure guidate. Un modo efficace per verificare quali file sono i file dell'applicazione in fase di esecuzione consiste nel tenere traccia dei file installati dall'installazione dell'applicazione. I file per utente vengono raramente installati dal programma di installazione di; Pertanto, la maggior parte dei file installati dal programma di installazione sono file dell'applicazione in fase di esecuzione.

 

 




