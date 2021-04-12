---
title: Aggiunta di un riferimento a un progetto Visual Basic
description: Aggiunta di un riferimento a un progetto Visual Basic
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329383"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>Aggiunta di un riferimento a un progetto Visual Basic

Nella procedura riportata di seguito viene descritto come aggiungere un riferimento a un oggetto COM a un progetto Visual Basic. L'applicazione può quindi usare le classi di tale oggetto.

Quando si aggiunge un oggetto come riferimento, è possibile utilizzare solo la libreria dei tipi fornita dal controllo o la libreria dei tipi "Raw". Al contrario, l'aggiunta di un controllo come componente espone anche le proprietà e i metodi del Visual Basic Extender come se facessero parte del controllo.

**Per creare un riferimento Visual Basic a un componente**

1.  Nel menu **Progetto**, fare clic su **Riferimenti**.
2.  Fare clic per selezionare la casella di controllo accanto al componente che si desidera aggiungere. Se il componente non è elencato, individuare il file con estensione dll o ocx utilizzando **Sfoglia**.
3.  Fare clic su **OK**.

Il componente fa ora parte del progetto. L'applicazione può creare istanze di classe usando la parola chiave **New** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di un componente a un progetto Visual Basic](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Conversione in Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




