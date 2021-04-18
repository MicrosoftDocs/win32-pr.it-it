---
title: Novità (registro eventi di Windows)
description: In questa pagina vengono riepilogate le nuove funzionalità aggiunte all'API registro eventi di Windows per ogni versione.
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652d82f67292316dd7aec599955d69dd70ab39a3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300910"
---
# <a name="whats-new-windows-event-log"></a>Novità (registro eventi di Windows)

In questa pagina vengono riepilogate le nuove funzionalità aggiunte all'API registro eventi di Windows per ogni versione.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Di seguito sono riportate le modifiche apportate allo schema [EventManifest](eventmanifestschema-schema.md) :

-   Rimosso il tipo complesso [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) . Per fornire la stessa funzionalità, usare opcode specifici dell'attività (vedere l'elemento **OpCodes** del tipo complesso [**TaskType**](eventmanifestschema-tasktype-complextype.md) .
-   Sono stati aggiunti i tipi semplici [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md), [**filePath**](eventmanifestschema-filepath-simpletype.md)e [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) per limitare i valori assegnati agli attributi di questi tipi.
-   Aggiunta dell'attributo **Filters** al tipo complesso [**ProviderType**](eventmanifestschema-providertype-complextype.md) . I provider possono utilizzare i filtri nello stesso modo in cui i provider utilizzano il livello e le parole chiave per determinare se devono scrivere un evento.
-   Sono stati aggiunti i tipi di output seguenti che è possibile specificare per gli elementi di dati definiti in un modello di dati evento:
    -   Win: DateTimeCultureInsensitive
    -   Win: HResult
    -   Win: NTSTATUS
-   I tipi di output vengono ora rispettati, prima che vengano ignorati.

Sono state apportate le modifiche seguenti alla versione del [**compilatore di messaggi**](message-compiler--mc-exe-.md) fornita con la versione di Windows 7 del Windows SDK:

-   Sono stati aggiunti argomenti per fare in modo che il compilatore generi codice di registrazione basato sul manifesto. È inoltre possibile richiedere al compilatore di generare codice per registrare gli eventi nei sistemi operativi precedenti a Windows Vista. Per un elenco degli argomenti, vedere la sezione "argomenti specifici per la generazione di codice usato per registrare gli eventi" dell'argomento del [**compilatore del messaggio**](message-compiler--mc-exe-.md) .
-   Il compilatore ora impone una convalida sintattica e semantica più restrittiva nel manifesto. In questo modo alcuni manifesti compilati correttamente nelle versioni precedenti del compilatore di messaggi possono richiedere modifiche per poter essere compilati correttamente utilizzando la versione più recente.
