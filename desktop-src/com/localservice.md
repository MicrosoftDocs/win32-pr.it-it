---
title: LocalService
description: Installa un oggetto come applicazione di servizio.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Valore LocalService del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873022"
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

Oltre a essere eseguito come file eseguibile del server locale (EXE), un oggetto COM può anche scegliere di creare un pacchetto per l'esecuzione come applicazione di servizio quando viene attivato da un client locale o remoto. I servizi supportano numerose funzionalità amministrative utili e integrate nell'interfaccia utente, tra cui l'avvio, l'arresto, la sospensione e il riavvio locali e remoti, nonché la possibilità di stabilire il server per l'esecuzione con un account utente e una stazione di finestra specifici.

Un oggetto scritto come servizio viene installato per l'uso da COM mediante la definizione di un valore **LocalService** e l'esecuzione di un'installazione del servizio standard. Il valore **LocalService** deve essere impostato sul nome del servizio, come configurato in **HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services**, come valore predefinito di **reg \_ SZ** .

Quando **LocalService** è impostato, qualsiasi stringa assegnata a [**ServiceParameters**](serviceparameters.md) viene passata come argomento della riga di comando al servizio mentre viene avviata.

La configurazione del servizio è preferibile in molte situazioni in cui le funzionalità delle API di gestione dei servizi locali e remote e dell'interfaccia utente possono essere utili per i servizi forniti dall'oggetto. Ad esempio, l'utilizzo del Framework di amministrazione esistente dell'architettura del servizio deve essere una scelta ovvia se l'oggetto è di lunga durata o supporta facilmente concetti quali l'avvio, l'arresto, la reimpostazione o la sospensione.

I servizi possono essere configurati dinamicamente e possono essere configurati per l'esecuzione automatica all'avvio del computer o per essere avviati quando richiesto da un'applicazione client.

Se si implementano classi come servizi, è necessario tenere presenti i punti seguenti:

-   Questo valore viene usato in preferenza con la chiave [**LocalServer32**](localserver32.md) per l'attivazione locale e remota requestsâ € "Se **LocalService** esiste e fa riferimento a un servizio valido, la chiave **LocalServer32** viene ignorata.
-   Attualmente, solo una singola istanza di un'applicazione di servizio potrebbe essere in esecuzione in un determinato momento in un computer. I servizi COM devono quindi registrare gli oggetti classe all'avvio usando REGCLS \_ MULTIPLEUSE per supportare più client.
-   Per avviare e inizializzare correttamente, i servizi COM configurati per l'esecuzione automatica quando un computer viene avviato devono includere RPCSS nell'elenco di servizi dipendenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[**ServiceParameters**](serviceparameters.md)
</dt> <dt>

[Services](/windows/desktop/Services/services)
</dt> </dl>

 

 