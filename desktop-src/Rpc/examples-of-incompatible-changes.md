---
title: Esempi di modifiche incompatibili
description: "Quando si gestiscono modifiche incompatibili, l'incompatibile regola generale è la seguente: qualsiasi modifica può essere incompatibile con le versioni precedenti, a meno che non sia ben compresa."
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a8736093e8189570026489bc1753145b941b7429b704e2c9c68783ddefef0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930040"
---
# <a name="examples-of-incompatible-changes"></a>Esempi di modifiche incompatibili

Quando si gestiscono modifiche incompatibili, la regola generale è la seguente: qualsiasi modifica può essere incompatibile con le versioni precedenti, a meno che non sia ben compresa. Questa regola richiede la conoscenza delle regole del rapporto di mancato recapito. Se non si conosce il rapporto di mancato recapito, non apportare modifiche. Di seguito sono riportati alcuni esempi di modifiche che in genere comportano una violazione di accesso nell'applicazione o un'eccezione BAD STUB DATA generata dal motore \_ \_ di \_ marshalling:

-   Aggiunta di un nuovo metodo nel mezzo di metodi vecchi.
-   Aggiunta o rimozione di parametri da un metodo.
-   Modifica di un attributo, ad esempio un attributo puntatore: modifica \[ di ref in unique o \] \[ \] \[ ptr o \] viceversa. Ogni tipo di puntatore ha una rappresentazione di collegamento diversa.
-   Modifica delle dimensioni dei dati: da short a long, da char a wchar t (unicode), aggiunta di un campo a una struttura, modifica delle dimensioni di \_ una matrice di dimensioni fisse.
-   Aggiunta di union bracci a un'unione con una clausola predefinita.

Alcune modifiche insidiose o mancate corrispondenze impreviste tra un client e un server possono verificarsi come segue:

-   Modifica di un membro di un tipo composto, ad esempio una struttura o una matrice. Ad esempio, se un ID CLIENT cambia da integrale a GUID, una struttura CLIENT RECORD con il \_ campo CLIENT ID diventa \_ \_ incompatibile. Questo può essere difficile da rilevare se viene propagato attraverso diversi livelli di incorporamento in un tipo di parametro remoto effettivo.
-   Modifica di un tipo importato. Il tipo può essere proveniente da un componente diverso che non è direttamente remoto, quindi la modifica è stata ritenuta compatibile.
-   L'uso di ifdef in un file IDL non è una buona idea per le definizioni di tipo ifdef in un file IDL. È un'emergenza \# in attesa di verificarsi. Inevitabilmente, a causa di errori di compilazione o di altro tipo, un client viene compilato con un set diverso di definizioni rispetto al server e finisce per essere incompatibile.

 

 




