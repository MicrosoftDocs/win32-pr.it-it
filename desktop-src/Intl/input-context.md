---
description: Un &\# 0034;contesto di input&0034; è una struttura interna gestita \# da IMM.
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: Contesto di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2927d3f573704aadb1ef72bdb26a35d37d90c1f90ab58d3a947ee84f8f38f7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145900"
---
# <a name="input-context"></a>Contesto di input

Un "contesto di input" è una struttura interna gestita da IMM. Contiene informazioni sullo stato dell'IME e viene usato dalle finestre IME. Per impostazione predefinita, il sistema operativo crea e assegna un contesto di input a ogni thread. All'interno del thread, questo contesto di input predefinito è una risorsa condivisa ed è associato a ogni finestra appena creata.

Per recuperare o impostare informazioni nell'IME, un'applicazione in grado di riconoscere IME deve prima recuperare un handle per il contesto di input associato a una finestra specificata. L'applicazione recupera l'handle usando la [**funzione ImmGetContext.**](/windows/desktop/api/Imm/nf-imm-immgetcontext) Può usare l'handle recuperato nelle chiamate successive alle funzioni IMM per recuperare e impostare i valori IME, ad esempio lo stile della finestra di composizione, lo stile di composizione e la posizione della finestra di stato. Al termine dell'uso del contesto, l'applicazione deve rilasciare il contesto usando la [**funzione ImmReleaseContext.**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)

Poiché il contesto di input predefinito è una risorsa condivisa, tutte le modifiche apportate dall'applicazione si applicano a tutte le finestre nel thread. Tuttavia, l'applicazione può eseguire l'override di questo comportamento predefinito creando il proprio contesto di input e associandolo a una o più finestre del thread. Le modifiche apportate a un contesto di input specifico dell'applicazione si applicano solo alle finestre associate al contesto.

L'applicazione può creare un contesto di input usando la [**funzione ImmCreateContext.**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) Per assegnare il contesto a una finestra, l'applicazione chiama la [**funzione ImmAssociateContext.**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) Questa funzione restituisce un handle al contesto di input associato in precedenza. Se l'applicazione non ha già associato un contesto di input alla finestra, l'handle restituito è per il contesto di input predefinito. In genere, l'applicazione salva questo handle e successivamente lo riassocia alla finestra quando il contesto di input personalizzato non è più necessario.

Quando un contesto di input è associato a una finestra, il sistema operativo seleziona automaticamente tale contesto quando la finestra viene attivata e riceve lo stato attivo per l'input. Lo stile e altre informazioni nel contesto di input influiscono sull'input successivo della tastiera per tale finestra, determinando il funzionamento dell'IME.

L'applicazione deve eliminare qualsiasi contesto di input personalizzato prima che termini. In primo luogo, l'applicazione rimuove il contesto di input da qualsiasi associazione effettuata con le finestre nel thread usando la [**funzione ImmAssociateContext.**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) Chiama quindi la [**funzione ImmDestroyContext.**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 



