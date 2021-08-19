---
title: LocalService
description: Installa un oggetto come applicazione di servizio.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Valore del Registro di sistema LocalService COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e454566ac505907f66fad585062bc67f41c865df45b30405b83e5faadef7f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736467"
---
# <a name="localservice"></a>LocalService

Installa un oggetto come applicazione di servizio.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a>Commenti

Oltre all'esecuzione come eseguibile del server locale (EXE), un oggetto COM può anche scegliere di creare un pacchetto per l'esecuzione come applicazione di servizio quando viene attivato da un client locale o remoto. I servizi supportano numerose funzionalità amministrative utili e integrate nell'interfaccia utente, tra cui avvio locale e remoto, arresto, sospensione e riavvio, nonché la possibilità di stabilire il server per l'esecuzione con un account utente e una stazione finestra specifici.

Un oggetto scritto come servizio viene installato per l'uso da parte di COM stabilendo un **valore LocalService** ed eseguendo un'installazione del servizio standard. Il **valore LocalService** deve essere impostato sul nome del servizio, come configurato in **HKEY LOCAL MACHINE System \_ \_ \\ \\ CurrentControlSet \\ Services,** come valore **REG \_ SZ** predefinito.

Quando **LocalService è** impostato, qualsiasi stringa assegnata a [**ServiceParameters**](serviceparameters.md) viene passata come argomento della riga di comando al servizio durante l'avvio.

La configurazione del servizio è preferibile in molte situazioni in cui le funzionalità delle API di gestione dei servizi locali e remoti e dell'interfaccia utente possono essere utili per i servizi forniti dall'oggetto. Ad esempio, l'uso del framework amministrativo esistente dell'architettura del servizio deve essere una scelta ovvia se l'oggetto è di lunga durata o supporta facilmente concetti come l'avvio, l'arresto, la reimpostazione o la sospensione.

I servizi possono essere configurati in modo dinamico e possono essere configurati per l'esecuzione automatica all'avvio del computer o per l'avvio quando richiesto da un'applicazione client.

Se si implementano classi come servizi, è necessario tenere presente quanto segue:

-   Questo valore viene usato in preferenza per la chiave [**LocalServer32**](localserver32.md) per le richieste di attivazione locale e remota" se **LocalService** esiste e fa riferimento a un servizio valido, la chiave **LocalServer32 viene ignorata.**
-   Attualmente, in un computer può essere in esecuzione una sola istanza di un'applicazione di servizio in un determinato momento. I servizi COM devono quindi registrare i relativi oggetti classe all'avvio usando REGCLS \_ MULTIPLEUSE per supportare più client.
-   Per avviare e inizializzare correttamente, i servizi COM configurati per l'esecuzione automatica all'avvio di un computer devono includere RPCSS nel relativo elenco di servizi dipendenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[**Parametri del servizio**](serviceparameters.md)
</dt> <dt>

[Services](/windows/desktop/Services/services)
</dt> </dl>

 

 