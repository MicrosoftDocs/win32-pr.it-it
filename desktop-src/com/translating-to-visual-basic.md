---
title: Conversione in Visual Basic
description: Conversione in Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856401"
---
# <a name="translating-to-visual-basic"></a>Conversione in Visual Basic

È possibile aggiungere un oggetto COM al progetto Visual Basic come riferimento o come componente. Una volta che l'oggetto è stato aggiunto al progetto, l'applicazione può accedere alle classi e alle interfacce. È quindi possibile usare il Visualizzatore oggetti Visual Basic per visualizzare le informazioni sulla libreria dei tipi dell'oggetto nella sintassi Visual Basic.

I controlli vengono in genere aggiunti a un progetto in quanto i componenti e i non controlli vengono aggiunti come riferimenti. Quando un oggetto COM viene aggiunto come componente, viene visualizzato nella casella degli strumenti Visual Basic. Le nuove istanze di tale oggetto vengono create trascinando l'icona dell'oggetto dalla casella degli strumenti in un form Visual Basic o in un altro tipo di contenitore. Le nuove istanze di oggetti COM aggiunti come riferimenti vengono create utilizzando la parola chiave **New** .

La differenza tra l'uso di una classe come riferimento rispetto a un componente è sottile ma importante. Quando si aggiunge un oggetto come riferimento, è possibile utilizzare solo la libreria dei tipi fornita dal controllo o la libreria dei tipi "Raw".

Se si aggiunge un controllo come componente, Visual Basic unisce le proprietà e i metodi di estensione del form in cui il controllo è incorporato con la libreria dei tipi del controllo, fornendo in tal modo una versione estesa e con wrapper della libreria dei tipi. Con questa versione della libreria dei tipi, è possibile usare proprietà Extender come top e Left come se facessero parte del controllo anziché il contenitore del controllo.

Visual Basic attualmente non supporta più librerie dei tipi compilate in un unico file con estensione dll. Se si esegue una DLL che incorpora più librerie dei tipi, è necessario ottenere copie autonome delle librerie dei tipi dall'origine che ha fornito l'oggetto per poter utilizzare l'oggetto con Visual Basic.

Per altre informazioni, vedere i seguenti argomenti:

-   [Conversione in Visual Basic da C++](translating-to-visual-basic-from-c--.md)
-   [Conversione in Visual Basic da Java](translating-to-visual-basic-from-java.md)
-   [Aggiunta di un componente a un progetto Visual Basic](adding-a-component-to-a-visual-basic-project.md)
-   [Aggiunta di un riferimento a un progetto Visual Basic](adding-a-reference-to-a-visual-basic-project.md)
-   [Visual Basic Visualizzatore oggetti](visual-basic-object-browser.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in C++](translating-to-c--.md)
</dt> <dt>

[Conversione in Java](translating-to-java.md)
</dt> </dl>

 

 




