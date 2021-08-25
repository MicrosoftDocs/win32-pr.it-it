---
title: Puntatori a interfaccia e interfacce
description: Puntatori a interfaccia e interfacce
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abeb6040c2e55168fee1aa2c73db0056de557d0ddafaed6499e7da048dfc56de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854371"
---
# <a name="interface-pointers-and-interfaces"></a>Puntatori a interfaccia e interfacce

Un'istanza di un'implementazione dell'interfaccia è in realtà un puntatore a una matrice di puntatori ai metodi, ad esempio una tabella di funzioni che fa riferimento a un'implementazione di tutti i metodi specificati nell'interfaccia. Gli oggetti con più interfacce possono fornire puntatori a più tabelle di funzioni. Qualsiasi codice con un puntatore tramite il quale può accedere alla matrice può chiamare i metodi in tale interfaccia.

Parlare precisamente di questo riferimento indiretto multiplo è poco pratico, quindi il puntatore alla tabella delle funzioni di interfaccia che un altro oggetto deve avere per chiamare i relativi metodi viene chiamato semplicemente puntatore a *interfaccia*. È possibile creare manualmente tabelle di funzioni in un'applicazione C o quasi automaticamente usando Visual C++ (o altri linguaggi orientati a oggetti che supportano COM).

Con il supporto appropriato del compilatore (intrinseco in C e C++), un client può chiamare un metodo di interfaccia tramite il relativo nome, non la relativa posizione nella matrice. Poiché un'interfaccia è un tipo, il compilatore, dati i nomi dei metodi, può controllare i tipi di parametri e i valori restituiti di ogni chiamata al metodo di interfaccia. Al contrario, se un client usa uno schema di chiamata basato sulla posizione, tale controllo dei tipi non è disponibile, anche in C o C++.

Ogni interfaccia è un contratto non modificabile di un gruppo funzionale di metodi. Si fa riferimento a un'interfaccia in fase di esecuzione con un IID (Globally Unique Interface Identifier). Questo IID, che è un'istanza specifica di un identificatore univoco globale (GUID) supportato da COM, consente a un client di chiedere a un oggetto con precisione se supporta la semantica dell'interfaccia, senza sovraccarico superfluo e senza la confusione che potrebbe verificarsi in un sistema dalla presenza di più versioni della stessa interfaccia con lo stesso nome.

Per riepilogare, è importante comprendere che cos'è un'interfaccia COM e non lo è:

-   Un'interfaccia COM non corrisponde a una classe C++. La definizione virtuale pura non comporta alcuna implementazione. Se si è programmatori C++, è possibile definire l'implementazione di un'interfaccia come classe, ma questo rientra nell'intestazione dei dettagli di implementazione, che COM non specifica. È necessario creare un'istanza di un oggetto che implementa un'interfaccia perché l'interfaccia esista effettivamente. Inoltre, diverse classi di oggetti possono implementare un'interfaccia in modo diverso, ma possono essere usate in modo intercambiabile in formato binario, purché il comportamento sia conforme alla definizione dell'interfaccia.
-   Un'interfaccia COM non è un oggetto . Si tratta semplicemente di un gruppo correlato di funzioni ed è lo standard binario tramite cui comunicano i client e gli oggetti. Purché possa fornire puntatori ai metodi di interfaccia, l'oggetto può essere implementato in qualsiasi linguaggio con qualsiasi rappresentazione interna dello stato.
-   Le interfacce COM sono fortemente tipizzato. Ogni interfaccia ha un proprio identificatore di interfaccia (GUID), che elimina la possibilità di duplicazione che potrebbe verificarsi con qualsiasi altro schema di denominazione.
-   Le interfacce COM non sono modificabili. Non è possibile definire una nuova versione di un'interfaccia precedente e assegnargli lo stesso identificatore. L'aggiunta o la rimozione di metodi di un'interfaccia o la modifica della semantica crea una nuova interfaccia, non una nuova versione di un'interfaccia precedente. Pertanto, una nuova interfaccia non può essere in conflitto con un'interfaccia precedente. Tuttavia, gli oggetti possono supportare più interfacce contemporaneamente ed esporre interfacce che sono revisioni successive di un'interfaccia, con identificatori diversi. Pertanto, ogni interfaccia è un contratto separato e gli oggetti a livello di sistema non devono preoccuparsi se la versione dell'interfaccia che chiamano è quella prevista. L'ID interfaccia (IID) definisce il contratto di interfaccia in modo esplicito e univoco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce e oggetti COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




