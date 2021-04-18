---
title: Puntatori a interfaccia e interfacce
description: Puntatori a interfaccia e interfacce
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa23d53f529c43fa7529d657108cc75cb6a23b15
ms.sourcegitcommit: d482e4276cc06515e9fade2f253a257ffc418ce5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2019
ms.locfileid: "106297593"
---
# <a name="interface-pointers-and-interfaces"></a>Puntatori a interfaccia e interfacce

Un'istanza di un'implementazione di interfaccia è in realtà un puntatore a una matrice di puntatori ai metodi, ovvero una tabella di funzioni che fa riferimento a un'implementazione di tutti i metodi specificati nell'interfaccia. Gli oggetti con più interfacce possono fornire puntatori a più di una tabella di funzioni. Il codice con un puntatore tramite il quale può accedere alla matrice può chiamare i metodi di tale interfaccia.

La precisazione di questo riferimento indiretto multiplo è scomoda, quindi il puntatore alla tabella di funzioni di interfaccia che un altro oggetto deve chiamare i relativi metodi viene chiamato semplicemente un *puntatore di interfaccia*. È possibile creare manualmente tabelle di funzioni in un'applicazione C o quasi automaticamente utilizzando Visual C++ (o altri linguaggi orientati a oggetti che supportano COM).

Con il supporto del compilatore appropriato, che è intrinseco in C e C++, un client può chiamare un metodo di interfaccia tramite il nome, non la posizione nella matrice. Poiché un'interfaccia è un tipo, il compilatore, dato i nomi dei metodi, può controllare i tipi di parametri e i valori restituiti di ogni chiamata al metodo di interfaccia. Al contrario, se un client usa uno schema di chiamata basato sulla posizione, questo controllo dei tipi non è disponibile, anche in C o C++.

Ogni interfaccia è un contratto non modificabile di un gruppo funzionale di metodi. Si fa riferimento a un'interfaccia in fase di esecuzione con un identificatore di interfaccia univoco globale (IID). Questo IID, che è un'istanza specifica di un identificatore univoco globale (GUID) supportato da COM, consente a un client di richiedere un oggetto con precisione se supporta la semantica dell'interfaccia, senza un sovraccarico superfluo e senza confusione che potrebbe verificarsi in un sistema di avere più versioni della stessa interfaccia con lo stesso nome.

Per riepilogare, è importante comprendere che cos'è un'interfaccia COM e non è:

-   Un'interfaccia COM non corrisponde a una classe C++. La definizione virtuale pura non contiene alcuna implementazione. Se si è un programmatore C++, è possibile definire l'implementazione di un'interfaccia come una classe, ma ciò rientra nell'intestazione dei dettagli di implementazione, che non è specificato da COM. È necessario creare un'istanza di un oggetto che implementa un'interfaccia per l'interfaccia effettivamente esistente. Inoltre, le classi di oggetti diverse possono implementare un'interfaccia in modo diverso, ma devono essere usate in modo intercambiabile in forma binaria, purché il comportamento sia conforme alla definizione dell'interfaccia.
-   Un'interfaccia COM non è un oggetto. Si tratta semplicemente di un gruppo correlato di funzioni ed è lo standard binario attraverso cui comunicano client e oggetti. Fino a quando può fornire puntatori ai metodi di interfaccia, l'oggetto può essere implementato in qualsiasi linguaggio con qualsiasi rappresentazione di stato interna.
-   Le interfacce COM sono fortemente tipizzate. Ogni interfaccia ha un proprio identificatore di interfaccia (GUID), che elimina la possibilità di duplicazione che può verificarsi con qualsiasi altro schema di denominazione.
-   Le interfacce COM non sono modificabili. Non è possibile definire una nuova versione di un'interfaccia precedente e assegnargli lo stesso identificatore. L'aggiunta o la rimozione di metodi di un'interfaccia o la modifica della semantica crea una nuova interfaccia, non una nuova versione di un'interfaccia obsoleta. Pertanto, una nuova interfaccia non può essere in conflitto con un'interfaccia obsoleta. Tuttavia, gli oggetti possono supportare più interfacce simultaneamente e possono esporre interfacce che sono revisioni successive di un'interfaccia, con identificatori diversi. Pertanto, ogni interfaccia è un contratto separato e gli oggetti a livello non devono preoccuparsi se la versione dell'interfaccia che sta chiamando è quella che si aspettano. L'ID di interfaccia (IID) definisce il contratto di interfaccia in modo esplicito e univoco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti e interfacce COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




