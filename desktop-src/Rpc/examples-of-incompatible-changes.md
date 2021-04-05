---
title: Esempi di modifiche incompatibili
description: 'Quando si gestiscono modifiche incompatibili, la regola empirica sfavorevole è la seguente: qualsiasi modifica può essere incompatibile con le versioni precedenti, a meno che non sia ben riconosciuta.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044869"
---
# <a name="examples-of-incompatible-changes"></a>Esempi di modifiche incompatibili

Quando si gestiscono modifiche incompatibili, la regola empirica sfavorevole è la seguente: qualsiasi modifica può essere incompatibile con le versioni precedenti, a meno che non sia ben riconosciuta. Questa regola richiede la conoscenza delle regole di mancato recapito. Se non si conosce il rapporto di mancato recapito, non apportare modifiche. Di seguito sono riportati alcuni esempi di modifiche che in genere comportano una violazione di accesso nell'applicazione o un' \_ \_ eccezione dei dati stub non valida \_ generata dal motore di marshalling:

-   Aggiunta di un nuovo metodo al centro dei metodi obsoleti.
-   Aggiunta o rimozione di parametri da un metodo.
-   Modifica di un attributo, ad esempio un attributo puntatore: \[ modifica \] di ref in \[ Unique \] o \[ ptr \] o viceversa. Ogni tipo di puntatore ha una rappresentazione Wire diversa.
-   Modifica della dimensione dei dati: da short a Long, da char a WCHAR \_ t (Unicode), aggiungendo un campo a una struttura, modificando la dimensione di una matrice a dimensione fissa.
-   Aggiunta di Union Arms a un'Unione con una clausola default.

Alcune modifiche insidiose o mancate corrispondenze indesiderate tra un client e un server possono verificarsi come segue:

-   Modifica di un membro di un tipo composto, ad esempio una struttura o una matrice. Se, ad esempio, un \_ ID client passa da un elemento integrale a un GUID, una \_ struttura di record client con il \_ campo ID client diventa incompatibile. Questo può essere difficile da rilevare se viene propagata attraverso diversi livelli di incorporamento in un tipo di parametro remoto effettivo.
-   Modifica di un tipo importato. Il tipo può provenire da un componente diverso che non è direttamente remoto, di conseguenza la modifica è stata considerata compatibile.
-   L'uso di \# ifdef in un file IDL non è una buona idea per le definizioni di tipo di ifdef in un file IDL. si tratta di un'emergenza in attesa di verificarsi. Inevitabilmente, a causa della compilazione o di altre anomalie, un client viene compilato con un set diverso di definizioni rispetto al server e non è più compatibile.

 

 




