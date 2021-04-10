---
title: Tipizzazione forte
description: C è un linguaggio debolmente tipizzato, ovvero il compilatore consente operazioni quali l'assegnazione e il confronto tra variabili di tipi diversi.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- RPC (Remote Procedure Call), descrizione, tipizzazione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955812"
---
# <a name="strong-typing"></a>Tipizzazione forte

C è un linguaggio debolmente tipizzato, ovvero il compilatore consente operazioni quali l'assegnazione e il confronto tra variabili di tipi diversi. Ad esempio, C consente il cast del valore di una variabile a un altro tipo. La possibilità di usare variabili di tipi diversi nella stessa espressione promuove la flessibilità e l'efficienza.

Un linguaggio fortemente tipizzato impone restrizioni sulle operazioni tra variabili di tipi diversi. In questi casi, il compilatore genera un errore che impedisce l'operazione. Queste rigide linee guida relative ai tipi di dati sono progettate per evitare potenziali errori.

La difficoltà nell'utilizzo di un linguaggio con tipizzazione debole, ad esempio C, per le chiamate a procedure remote è che le applicazioni distribuite possono essere eseguite in più computer diversi con compilatori C diversi e architetture diverse. Quando un'applicazione viene eseguita in un solo computer, non è necessario preoccuparsi del formato dati interno perché i dati vengono gestiti in modo coerente. Tuttavia, in un ambiente di elaborazione distribuita, computer diversi possono usare definizioni diverse per i tipi di dati di base. Alcuni computer, ad esempio, definiscono il tipo **int** , quindi la rappresentazione interna è 16 bit, mentre altri computer utilizzano 32 bit. Un'architettura di computer, nota come "little endian", assegna il byte di dati meno significativo all'indirizzo di memoria più basso e il byte più significativo all'indirizzo più elevato. Un'altra architettura, nota come "big endian", assegna il byte meno significativo all'indirizzo di memoria massimo associato a tali dati.

Le chiamate a procedure remote richiedono un controllo rigoroso sui tipi di parametro. Per gestire la trasmissione e la conversione dei dati in rete, MIDL impone rigorosamente restrizioni sui tipi per i dati trasferiti in rete. Per questo motivo, MIDL include un set di [tipi di base](base-types.md)ben definiti. MIDL impone la tipizzazione forte imponendo l'uso di parole chiave che definiscono in modo univoco le dimensioni e il tipo di dati. L'effetto più visibile della tipizzazione forte è che MIDL non consente le variabili del tipo **void \***.

Negli argomenti seguenti, in questa sezione vengono illustrate le funzionalità del linguaggio MIDL che applicano la tipizzazione dei dati avanzata:

-   [Tipi di base](base-types.md)
-   [Tipi firmati e non firmati](signed-and-unsigned-types.md)
-   [Tipi di caratteri wide](wide-character-types.md)
-   [Strutture](structures.md)
-   [Unioni](unions.md)
-   [Tipi enumerati](enumerated-types.md)
-   [Matrici](arrays.md)
-   [Attributi di funzione](function-attributes.md)
-   [Attributi di campo](field-attributes.md)
-   [Tre tipi di puntatore](three-pointer-types.md)
-   [Attributi di tipo](type-attributes.md)

 

 




