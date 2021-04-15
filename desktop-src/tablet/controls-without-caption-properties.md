---
description: Introduzione all'utilizzo di controlli senza proprietà didascalia per Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Controlli senza proprietà didascalia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524378"
---
# <a name="controls-without-caption-properties"></a>Controlli senza proprietà didascalia

Quando un controllo non ha una propria proprietà Caption, attenersi alla procedura seguente per assicurarsi che gli strumenti di accessibilità possano identificare i controlli:

-   Creare un controllo testo statico con un nome significativo e descrittivo.
-   Posizionare l'etichetta statica in modo che preceda immediatamente il controllo a cui si fa riferimento, in ordine di tabulazione.
-   Verificare che il testo dell'etichetta termini con i due punti, ad esempio "Settings:".
-   Posizionare il testo dell'etichetta immediatamente a sinistra o prima del controllo a cui si fa riferimento.
-   Rendere invisibile il testo statico se non è appropriato visualizzarlo visivamente. A tale scopo, assegnare l'attributo appropriato nello script della risorsa. Questo può essere appropriato quando il nome o la funzione di un controllo viene fornito visivamente tramite un metodo diverso dal controllo testo statico, ad esempio un elemento grafico o un pulsante di opzione correlato.

L'uso corretto dei controlli statici è l'unico modo per implementare correttamente le chiavi di accesso sottolineate per i controlli che non dispongono di etichette intrinseche. Per ulteriori informazioni sull'utilizzo di controlli che non dispongono di proprietà didascalia, vedere la sezione relativa all' [accessibilità](/windows/desktop/accessibility) .

 

 
