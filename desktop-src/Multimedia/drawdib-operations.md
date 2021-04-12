---
title: Operazioni DrawDib
description: Operazioni DrawDib
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib, informazioni
- DrawDib, accesso
- DrawDib, apertura
- DrawDib, operazioni
- DrawDib, contesto di dispositivo (DC)
- CONTROLLER di dominio (contesto di dispositivo)
- DrawDibOpen (funzione)
- DrawDibClose (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471750"
---
# <a name="drawdib-operations"></a>Operazioni DrawDib

È possibile accedere all'intero gruppo di funzioni DrawDib usando la funzione [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) . Questa funzione carica la libreria di collegamento dinamico (DLL), alloca le risorse di memoria, crea un contesto di dispositivo DrawDib (DC) e mantiene un conteggio dei riferimenti del numero di controller di dominio inizializzati. **DrawDibOpen** restituisce anche un handle del nuovo controller di dominio usato con le altre funzioni DrawDib.

È possibile rilasciare un controller di dominio DrawDib al termine dell'uso usando la funzione [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) . **DrawDibClose** decrementa anche il conteggio dei riferimenti delle applicazioni che accedono alla dll. La chiamata a **DrawDibClose** deve essere l'ultima funzione DrawDib nell'applicazione.

È possibile creare tutti i controller di dominio DrawDib desiderati. È possibile usare più controller di dominio DrawDib per creare diverse bitmap simultaneamente. È anche possibile creare più controller di dominio DrawDib, ognuno con caratteristiche univoche, in modo che l'applicazione possa scegliere e quindi usare il controller di dominio con le impostazioni più appropriate. Ad esempio, è possibile creare due controller di dominio DrawDib in un'applicazione: uno che visualizza un'immagine con la risoluzione normale e l'altro che visualizza una parte ingrandita dell'immagine.

Per un'esecuzione efficiente, le funzioni DrawDib richiedono informazioni sulla scheda di visualizzazione e sul relativo driver. Il profilo di visualizzazione viene ottenuto eseguendo una serie di test sulla scheda di visualizzazione la prima volta che si accede alla DLL contenente le funzioni DrawDib. Le funzioni DrawDib utilizzano queste informazioni per tutte le applicazioni. È possibile ripetere questi test quando necessario tramite la funzione [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) .

> [!Note]  
> Il recupero e l'archiviazione del profilo di visualizzazione è in genere una singola occorrenza. Se, tuttavia, le informazioni sul profilo vengono eliminate o nel sistema è installato un altro driver di visualizzazione, DrawDib esegue nuovamente i test.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle funzioni DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




