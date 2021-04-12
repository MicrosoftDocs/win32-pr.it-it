---
title: Linee guida dell'interfaccia utente per le estensioni della classe helper NDF
description: Quando si compila la classe helper, è necessario creare il testo per aiutare l'utente a comprendere la ragione di un evento imprevisto e le possibili operazioni di ripristino che possono essere eseguite.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104335407"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a>Linee guida dell'interfaccia utente per le estensioni della classe helper NDF

Quando si compila la classe helper, è necessario creare il testo per aiutare l'utente a comprendere la ragione di un evento imprevisto e le possibili operazioni di ripristino che possono essere eseguite.

## <a name="root-cause-and-repair"></a>Causa radice e ripristino

Quando si verifica un evento imprevisto, viene visualizzata una finestra di dialogo che informa l'utente di cosa è accaduto. Il testo creato verrà visualizzato in due aree separate.

-   **Causa radice**: breve descrizione della causa del problema. Contiene informazioni che consentono a un amministratore o a un utente avanzato di risolvere il problema.
-   **Correzione**: espande la causa radice per fornire altri dettagli sui passaggi che possono essere eseguiti da un utente senza troppo tempo.

Ogni causa radice o correzione deve avere un titolo e una descrizione. Tutto il testo prima del primo \\ carattere "n" verrà usato per il titolo. Per la descrizione verrà usato tutto il testo che segue il primo \\ carattere "n", comprese le interruzioni di riga successive.

## <a name="title-guidelines"></a>Linee guida sul titolo

Il titolo di una causa radice o di un ripristino deve attenersi alle linee guida seguenti:

-   Deve avere una lunghezza inferiore a 128 caratteri. (è consigliato 40 caratteri o meno).
-   Non deve terminare con un punto.

## <a name="description-guidelines"></a>Linee guida per la descrizione

La descrizione di una causa radice o di un ripristino deve attenersi alle linee guida seguenti:

-   Deve avere una lunghezza inferiore a 512 caratteri.
-   Ogni frase deve terminare con un punto.
-   Il \\ carattere "n" può essere utilizzato per creare un'interruzioni di riga nella descrizione.

 

 




