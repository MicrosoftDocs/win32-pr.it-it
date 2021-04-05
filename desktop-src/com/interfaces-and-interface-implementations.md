---
title: Interfacce e implementazioni di interfaccia
description: COM apporta una distinzione fondamentale tra le definizioni di interfaccia e le relative implementazioni.
ms.assetid: f50b3e8f-bf87-4525-b47b-96e75b3a05b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db8df92ac8b851925d82a4b03505fa4c5ab3dc39
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2020
ms.locfileid: "104046413"
---
# <a name="interfaces-and-interface-implementations"></a>Interfacce e implementazioni di interfaccia

COM apporta una distinzione fondamentale tra le definizioni di interfaccia e le relative implementazioni.

Un' *interfaccia* è in realtà un contratto costituito da un gruppo di prototipi di funzione correlati il cui utilizzo è definito ma la cui implementazione non lo è. Questi prototipi di funzione sono equivalenti alle classi base virtuali pure nella programmazione C++. Una definizione di interfaccia specifica le funzioni membro dell'interfaccia, i *Metodi* denominati, i relativi tipi restituiti, il numero e i tipi di parametri e le operazioni che devono eseguire. Non esiste alcuna implementazione associata a un'interfaccia.

Un' *implementazione dell'interfaccia* è il codice fornito da un programmatore per eseguire le azioni specificate in una definizione di interfaccia. Le implementazioni di molte delle interfacce che possono essere utilizzate da un programmatore in un'applicazione basata su oggetti sono incluse nelle librerie COM. Tuttavia, i programmatori sono liberi di ignorare queste implementazioni e di scriverne di proprie. Un'implementazione dell'interfaccia deve essere associata a un oggetto quando viene creata un'istanza di tale oggetto e l'implementazione fornisce i servizi offerti dall'oggetto.

Ad esempio, un'ipotetica interfaccia denominata l'interfaccia può definire due metodi, denominati push e pop, che specificano che le chiamate successive al metodo pop restituiscono, in ordine inverso, i valori passati in precedenza al metodo push. Questa definizione di interfaccia non specifica il modo in cui le funzioni devono essere implementate nel codice. Quando si implementa l'interfaccia, un programmatore può implementare lo stack come matrice e implementare i metodi push e pop in modo tale da poter accedere a tale matrice, mentre un altro programmatore può utilizzare un elenco collegato e implementare i metodi di conseguenza. Indipendentemente da una particolare implementazione dei metodi push e pop, la rappresentazione in memoria di un puntatore a un'interfaccia e pertanto il suo utilizzo da parte di un client è completamente determinata dalla definizione dell'interfaccia.

Gli oggetti semplici supportano una sola interfaccia. Gli oggetti più complessi, ad esempio gli oggetti incorporabili, supportano in genere più interfacce. I client hanno accesso a un oggetto COM solo tramite un puntatore a una delle sue interfacce, che, a sua volta, consente al client di chiamare qualsiasi metodo che costituisce tale interfaccia. Questi metodi determinano il modo in cui un client può utilizzare i dati dell'oggetto.

Le interfacce definiscono un contratto tra un oggetto e i relativi client. Il contratto specifica i metodi che devono essere associati a ogni interfaccia e il comportamento di ognuno dei metodi deve essere in termini di input e output. Il contratto non definisce in genere come implementare i metodi in un'interfaccia. Un altro aspetto importante del contratto è che se un oggetto supporta un'interfaccia, deve supportare tutti i metodi di tale interfaccia in qualche modo. Non tutti i metodi di un'implementazione devono eseguire un'operazione. Se un oggetto non supporta la funzione implicita da un metodo, la relativa implementazione può essere un valore restituito semplice o forse il ritorno di un messaggio di errore significativo, ma i metodi devono esistere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti e interfacce COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




