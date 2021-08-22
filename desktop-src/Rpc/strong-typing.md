---
title: Tipizzazione forte
description: C è un linguaggio tipizzazione debole, in altre modo il compilatore consente operazioni quali l'assegnazione e il confronto tra variabili di tipi diversi.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- Chiamata di procedura remota RPC, descritta, digitazione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae47746119f4c1b22bc066075ed484ef836fa6a68ee103e06975018a6ae49012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924847"
---
# <a name="strong-typing"></a>Tipizzazione forte

C è un linguaggio tipizzazione debole, in altre modo il compilatore consente operazioni quali l'assegnazione e il confronto tra variabili di tipi diversi. Ad esempio, C consente il cast del valore di una variabile a un altro tipo. La possibilità di usare variabili di tipi diversi nella stessa espressione favorisce la flessibilità e l'efficienza.

Un linguaggio fortemente tipizzato impone restrizioni sulle operazioni tra variabili di tipi diversi. In questi casi, il compilatore genera un errore che impedisce l'operazione. Queste linee guida rigorose relative ai tipi di dati sono progettate per evitare potenziali errori.

La difficoltà di usare un linguaggio debolmente tipidato, ad esempio C per le chiamate di procedura remota, è che le applicazioni distribuite possono essere eseguite in diversi computer con compilatori C diversi e architetture diverse. Quando un'applicazione viene eseguita in un solo computer, non è necessario preoccuparsi del formato dati interno perché i dati vengono gestiti in modo coerente. Tuttavia, in un ambiente di elaborazione distribuito, computer diversi possono usare definizioni diverse per i tipi di dati di base. Ad esempio, alcuni computer definiscono il **tipo int,** quindi la relativa rappresentazione interna è di 16 bit, mentre altri computer usano 32 bit. Un'architettura di computer, nota come "little endian", assegna il byte di dati meno significativo all'indirizzo di memoria più basso e il byte più significativo all'indirizzo più alto. Un'altra architettura, nota come "big endian", assegna il byte meno significativo all'indirizzo di memoria più alto associato a tale dati.

Le chiamate di procedura remota richiedono un controllo rigoroso sui tipi di parametro. Per gestire la trasmissione e la conversione dei dati in rete, MIDL applica rigorosamente restrizioni di tipo per i dati trasferiti in rete. Per questo motivo, MIDL include un set di tipi [di base ben definiti.](base-types.md) MIDL impone la tipizzazione forte imponendo l'uso di parole chiave che definiscono in modo non ambiguo le dimensioni e il tipo di dati. L'effetto più visibile della tipizzazione forte è che MIDL non consente variabili di tipo **void \***.

Negli argomenti seguenti questa sezione illustra le funzionalità del linguaggio MIDL che imponino la digitazione di dati avanzati:

-   [Tipi di base](base-types.md)
-   [Tipi firmati e senza segno](signed-and-unsigned-types.md)
-   [Tipi di caratteri wide](wide-character-types.md)
-   [Strutture](structures.md)
-   [Unioni](unions.md)
-   [Tipi enumerati](enumerated-types.md)
-   [Matrici](arrays.md)
-   [Attributi delle funzioni](function-attributes.md)
-   [Attributi di campo](field-attributes.md)
-   [Tre tipi di puntatore](three-pointer-types.md)
-   [Attributi di tipo](type-attributes.md)

 

 




