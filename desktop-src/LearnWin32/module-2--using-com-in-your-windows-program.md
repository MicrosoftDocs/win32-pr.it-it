---
title: Uso di COM nell'app di Windows
description: Il modulo 1 di questa serie ha illustrato come creare una finestra e rispondere ai messaggi della finestra, ad esempio WM \_ Paint e WM \_ Close. Nel modulo 2 è stata introdotta la Component Object Model (COM).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726951"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a>Modulo 2. Uso di COM nel programma Windows-Based

Il [modulo 1](your-first-windows-program.md) di questa serie ha illustrato come creare una finestra e rispondere ai messaggi della finestra, ad esempio [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e [**WM \_ Close**](/windows/desktop/winmsg/wm-close). Nel modulo 2 è stata introdotta la Component Object Model (COM).

COM è una specifica per la creazione di componenti software riutilizzabili. Molte delle funzionalità che si utilizzeranno in un programma moderno basato su Windows si basano su COM, come nel seguente esempio:

-   Grafica (Direct2D)
-   Testo (DirectWrite)
-   Shell di Windows
-   Controllo Ribbon
-   Animazione dell'interfaccia utente

Alcune tecnologie in questo elenco utilizzano un subset di COM e pertanto non sono "pure" COM.

COM ha una reputazione per essere difficile da apprendere. Ed è vero che scrivere un nuovo modulo software per supportare COM può essere difficile. Tuttavia, se il programma è esclusivamente un *consumatore* di com, è possibile che com sia più facile da comprendere del previsto.

Questo modulo illustra come chiamare le API basate su COM nel programma. Descrive anche alcuni dei ragionamenti dietro la progettazione di COM. Se si comprende il motivo per cui COM è progettato, è possibile programmare in modo più efficace. La seconda parte del modulo descrive alcune procedure di programmazione consigliate per COM.

COM è stato introdotto in 1993 per supportare il collegamento a oggetti e l'incorporamento (OLE) 2,0. A volte le persone pensano che COM e OLE siano uguali. Questo può essere un altro motivo della percezione che COM è difficile da apprendere. OLE 2,0 si basa su COM, ma non è necessario conoscere OLE per comprendere COM.

COM è uno *standard binario*, non uno standard del linguaggio: definisce l'interfaccia binaria tra un'applicazione e un componente software. Come standard binario, COM è indipendente dalla lingua, sebbene venga mappato naturalmente a determinati costrutti C++. Questo modulo si concentrerà su tre obiettivi principali di COM:

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

[Impara a programmare per Windows in C++](learn-to-program-for-windows.md)
</dt> </dl>

 

 