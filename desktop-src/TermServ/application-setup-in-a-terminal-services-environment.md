---
title: Configurazione dell'applicazione
description: L'installazione di un'applicazione per un singolo utente può creare problemi in un ambiente multiutente Servizi Desktop remoto.
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3c53f2370f4123352489ac747546e3335c558
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338679"
---
# <a name="application-setup"></a>Configurazione dell'applicazione

La procedura di installazione automatica per molte applicazioni esistenti presuppone che l'applicazione sia installata per un singolo utente. In un ambiente di Servizi Desktop remoto multiutente, questo presupposto può creare i seguenti problemi:

-   Se la procedura di installazione aggiorna il registro di sistema e l'ambiente desktop per un solo utente, altri utenti dovranno reinstallare l'intero pacchetto o un amministratore deve copiare manualmente le informazioni dal registro di sistema e dal desktop di un utente agli altri utenti.
-   Con alcune procedure di installazione, è possibile personalizzare l'applicazione in fase di installazione escludendo le funzionalità di. Se il programma di installazione iniziale esclude parte dell'applicazione, altri utenti dovranno reinstallare l'applicazione per ottenere le funzionalità escluse.

Per evitare questi problemi, è necessario che le procedure di installazione usino le linee guida seguenti quando si installa un'applicazione in un server di host sessione Desktop remoto (host sessione Desktop remoto):

-   Installare le applicazioni nell'ambiente utente predefinito comune a tutti gli utenti. Prima di installare l'applicazione, eseguire il comando **Change user/install** console e, al termine dell'installazione, eseguire il comando **Change user/Execute Accoda** console. Usare uno script di compatibilità Servizi Desktop remoto per l'installazione.
-   Supporto della personalizzazione specifica dell'utente tramite l'utilizzo di profili utente. A tale scopo, creare un [formato di file modello amministrativo](/previous-versions/windows/desktop/Policy/administrative-template-file-format) per consentire a un amministratore di configurare il registro di sistema per indicare le funzionalità disponibili per ogni utente. Quindi, in fase di esecuzione, l'applicazione può abilitare o disabilitare le funzionalità in base alle impostazioni nelle impostazioni del registro di sistema dell'utente corrente. L'applicazione può archiviare la configurazione per utente nell'hive del registro di sistema **dell'utente corrente di HKEY** e consentire a ogni utente di configurare l'applicazione in base alle proprie preferenze.

 

 