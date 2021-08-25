---
description: Introduzione all'uso di controlli senza proprietà della didascalia per il Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Controlli senza proprietà didascalia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5cd8eb0c87f946d8540fb63d75408dcf98a880cefcd1ba295ba2ba113e6828f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774111"
---
# <a name="controls-without-caption-properties"></a>Controlli senza proprietà didascalia

Quando un controllo non dispone di una proprietà didascalia, seguire questa procedura per assicurarsi che gli strumenti di accessibilità possano identificare i controlli:

-   Creare un controllo di testo statico con un nome significativo e descrittivo.
-   Posizionare l'etichetta statica in modo che preceda immediatamente il controllo a cui si fa riferimento, nell'ordine di tabulazione.
-   Assicurarsi che il testo dell'etichetta termini con i due punti, ad esempio "Impostazioni:"
-   Posizionare il testo dell'etichetta immediatamente a sinistra o prima del controllo a cui si fa riferimento.
-   Rendere il testo statico invisibile se non è appropriato visualizzarlo visivamente. A tale scopo, assegnare l'attributo appropriato nello script della risorsa. Questo può essere appropriato quando il nome o la funzione di un controllo viene fornito visivamente con mezzi diversi dal controllo di testo statico, ad esempio un elemento grafico o un pulsante di opzione correlato.

L'uso corretto dei controlli statici è l'unico modo per implementare correttamente le chiavi di accesso sottolineate per i controlli che non dispongono di etichette intrinseche. Per altre informazioni sull'uso di controlli che non dispongono di proprietà della didascalia, vedere la [sezione Accessibilità.](/windows/desktop/accessibility)

 

 
