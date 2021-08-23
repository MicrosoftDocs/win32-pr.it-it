---
title: Uso di COM nell'app Windows app
description: Il modulo 1 di questa serie ha illustrato come creare una finestra e rispondere ai messaggi della finestra, ad esempio WM \_ PAINT e WM \_ CLOSE. Il modulo 2 introduce il Component Object Model (COM).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2180d47bd0dd12c0184a2f9241ec5656c7fe711150e1d5163ca2fec9e0b28fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068031"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a>Modulo 2. Uso di COM nel programma Windows-Based

[Il modulo 1](your-first-windows-program.md) di questa serie ha illustrato come creare una finestra e rispondere ai messaggi della finestra, ad esempio [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) e [**WM \_ CLOSE.**](/windows/desktop/winmsg/wm-close) Il modulo 2 introduce il Component Object Model (COM).

COM è una specifica per la creazione di componenti software riutilizzabili. Molte delle funzionalità che verranno usate in un programma moderno basato Windows si basano su COM, ad esempio:

-   Grafica (Direct2D)
-   Testo (DirectWrite)
-   Shell Windows
-   Controllo barra multifunzione
-   Animazione dell'interfaccia utente

Alcune tecnologie in questo elenco usano un subset di COM e quindi non sono COM "pure".

COM ha la reputazione di essere difficile da apprendere. Ed è vero che la scrittura di un nuovo modulo software per supportare COM può essere difficile. Tuttavia, se il programma è esclusivamente un *consumer* di COM, è possibile che COM sia più facile da comprendere del previsto.

Questo modulo illustra come chiamare LE API basate su COM nel programma. Descrive anche alcuni dei motivi alla base della progettazione di COM. Se si comprende perché COM è progettato così com'è, è possibile programmarlo in modo più efficace. La seconda parte del modulo descrive alcune procedure di programmazione consigliate per COM.

COM è stato introdotto nel 1993 per supportare il collegamento e l'incorporamento di oggetti (OLE) 2.0. A volte si pensa che COM e OLE siano la stessa cosa. Questo può essere un altro motivo della percezione che COM sia difficile da apprendere. OLE 2.0 è basato su COM, ma non è necessario conoscere OLE per comprendere COM.

COM è uno *standard binario,* non uno standard del linguaggio: definisce l'interfaccia binaria tra un'applicazione e un componente software. Come standard binario, COM è indipendente dal linguaggio, anche se viene mappato naturalmente a determinati costrutti C++. Questo modulo si concentrerà su tre obiettivi principali di COM:

-   Separazione dell'implementazione di un oggetto dalla relativa interfaccia.
-   Gestione della durata di un oggetto.
-   Individuazione delle funzionalità di un oggetto in fase di esecuzione.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Che cos'è un'interfaccia COM?](what-is-a-com-interface-.md)
-   [Inizializzazione della libreria COM](initializing-the-com-library.md)
-   [Codici di errore in COM](error-codes-in-com.md)
-   [Creazione di un oggetto in COM](creating-an-object-in-com.md)
-   [Esempio: finestra di dialogo Apri](example--the-open-dialog-box.md)
-   [Gestione della durata di un oggetto](managing-the-lifetime-of-an-object.md)
-   [Richiesta di un oggetto per un'interfaccia](asking-an-object-for-an-interface.md)
-   [Allocazione di memoria in COM](memory-allocation-in-com.md)
-   [Procedure di codifica COM](com-coding-practices.md)
-   [Gestione degli errori in COM](error-handling-in-com.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul programma per Windows in C++](learn-to-program-for-windows.md)
</dt> </dl>

 

 