---
title: Traduzione in Visual Basic
description: Traduzione in Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9aa8a163141c6361df464a22ce873770c8385607bdf8f84d333d204c55a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550615"
---
# <a name="translating-to-visual-basic"></a>Traduzione in Visual Basic

È possibile aggiungere un oggetto COM al Visual Basic progetto come riferimento o come componente. Dopo aver aggiunto l'oggetto al progetto, l'applicazione può accedere alle relative classi e interfacce. È quindi possibile usare il visualizzatore Visual Basic oggetti per visualizzare le informazioni sulla libreria dei tipi dell'oggetto Visual Basic sintassi.

In genere, i controlli vengono aggiunti a un progetto come componenti e i controlli non vengono aggiunti come riferimenti. Quando un oggetto COM viene aggiunto come componente, viene visualizzato nella casella Visual Basic strumenti. Le nuove istanze dell'oggetto vengono create trascinando l'icona dell'oggetto dalla casella degli strumenti Visual Basic form o un altro tipo di contenitore. Le nuove istanze di oggetti COM aggiunti come riferimenti vengono create usando la **parola chiave new.**

La distinzione tra l'uso di una classe come riferimento rispetto a un componente è sottile ma importante. Quando si aggiunge un oggetto come riferimento, è possibile usare solo la libreria dei tipi fornita dal controllo o la libreria dei tipi "non elaborata".

Se si aggiunge un controllo come componente, Visual Basic unisce le proprietà e i metodi di estensione del form in cui il controllo è incorporato nella libreria dei tipi del controllo, fornendo in tal modo una versione estesa e incapsulata della libreria dei tipi. Con questa versione della libreria dei tipi, è possibile usare le proprietà di estensione, ad esempio Top e Left, come se fossero parte del controllo, anziché il contenitore del controllo.

Visual Basic attualmente non supporta più librerie dei tipi incorporate in un singolo .dll file. Se si esegue una DLL che incorpora più librerie dei tipi, è necessario ottenere copie autonome delle librerie dei tipi dall'origine che ha fornito l'oggetto per usare l'oggetto con Visual Basic.

Per altre informazioni, vedere i seguenti argomenti:

-   [Conversione in Visual Basic da C++](translating-to-visual-basic-from-c--.md)
-   [Conversione in Visual Basic da Java](translating-to-visual-basic-from-java.md)
-   [Aggiunta di un componente a un Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
-   [Aggiunta di un riferimento a un Visual Basic Project](adding-a-reference-to-a-visual-basic-project.md)
-   [Visual Basic Visualizzatore oggetti](visual-basic-object-browser.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in C++](translating-to-c--.md)
</dt> <dt>

[Traduzione in Java](translating-to-java.md)
</dt> </dl>

 

 




