---
title: Interfacce e implementazioni di interfacce
description: COM fa una distinzione fondamentale tra le definizioni di interfaccia e le relative implementazioni.
ms.assetid: f50b3e8f-bf87-4525-b47b-96e75b3a05b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee00521b847acbd063f1cd7ad84a0eb231f78d7bd274b7a4658996dbdd61150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992701"
---
# <a name="interfaces-and-interface-implementations"></a>Interfacce e implementazioni di interfacce

COM fa una distinzione fondamentale tra le definizioni di interfaccia e le relative implementazioni.

*Un'interfaccia* è in realtà un contratto costituito da un gruppo di prototipi di funzione correlati il cui utilizzo è definito ma la cui implementazione non lo è. Questi prototipi di funzione sono equivalenti alle classi di base virtuali pure nella programmazione C++. Una definizione di interfaccia specifica le funzioni membro dell'interfaccia, denominate metodi *,* i relativi tipi restituiti, il numero e i tipi dei relativi parametri e le relative attività. A un'interfaccia non è associata alcuna implementazione.

*Un'implementazione dell'interfaccia* è il codice fornito da un programmatore per eseguire le azioni specificate in una definizione di interfaccia. Le implementazioni di molte delle interfacce che un programmatore può usare in un'applicazione basata su oggetti sono incluse nelle librerie COM. Tuttavia, i programmatori possono ignorare queste implementazioni e scriverne di proprie. Un'implementazione dell'interfaccia deve essere associata a un oggetto quando viene creata un'istanza di tale oggetto e l'implementazione fornisce i servizi offerte dall'oggetto.

Ad esempio, un'ipotetica interfaccia denominata IStack potrebbe definire due metodi, denominati Push e Pop, specificando che le chiamate successive al metodo Pop restituiscono, in ordine inverso, i valori passati in precedenza al metodo Push. Questa definizione di interfaccia non specifica come devono essere implementate le funzioni nel codice. Nell'implementazione dell'interfaccia, un programmatore potrebbe implementare lo stack come matrice e implementare i metodi Push e Pop in modo da accedere a tale matrice, mentre un altro programmatore potrebbe usare un elenco collegato e implementare i metodi di conseguenza. Indipendentemente da una particolare implementazione dei metodi Push e Pop, la rappresentazione in memoria di un puntatore a un'interfaccia IStack e quindi il relativo utilizzo da parte di un client è completamente determinata dalla definizione dell'interfaccia.

Gli oggetti semplici supportano una sola interfaccia. Gli oggetti più complessi, ad esempio gli oggetti incorporabili, supportano in genere diverse interfacce. I client hanno accesso a un oggetto COM solo tramite un puntatore a una delle relative interfacce, che a sua volta consente al client di chiamare uno dei metodi che costituiscono tale interfaccia. Questi metodi determinano come un client può usare i dati dell'oggetto.

Le interfacce definiscono un contratto tra un oggetto e i relativi client. Il contratto specifica i metodi che devono essere associati a ogni interfaccia e il comportamento di ognuno dei metodi in termini di input e output. Il contratto in genere non definisce come implementare i metodi in un'interfaccia. Un altro aspetto importante del contratto è che se un oggetto supporta un'interfaccia, deve supportare tutti i metodi di tale interfaccia in qualche modo. Non tutti i metodi in un'implementazione devono eseguire un'operazione. Se un oggetto non supporta la funzione implicita da un metodo, la relativa implementazione può essere un semplice ritorno o forse la restituzione di un messaggio di errore significativo, ma i metodi devono esistere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce e oggetti COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




