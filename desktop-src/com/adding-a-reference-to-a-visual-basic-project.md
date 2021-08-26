---
title: Aggiunta di un riferimento a un Visual Basic Project
description: Aggiunta di un riferimento a un Visual Basic Project
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deba6030e57839e0f436239790aaa6f02e2fb29981ce021b0de2d09af2acdff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097071"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>Aggiunta di un riferimento a un Visual Basic Project

La procedura seguente descrive come aggiungere un riferimento a un oggetto COM a un Visual Basic progetto. L'applicazione può quindi usare le classi di tale oggetto.

Quando si aggiunge un oggetto come riferimento, è possibile usare solo la libreria dei tipi fornita dal controllo o la libreria dei tipi "non elaborata". Al contrario, l'aggiunta di un controllo come componente espone anche le proprietà e i metodi dell Visual Basic extender come se fossero parte del controllo.

**Per creare un Visual Basic riferimento a un componente**

1.  Nel menu **Progetto**, fare clic su **Riferimenti**.
2.  Fare clic per selezionare la casella di controllo accanto al componente da aggiungere. Se il componente non è elencato, individuare il file .dll o ocx usando **Sfoglia**.
3.  Fare clic su **OK**.

Il componente fa ora parte del progetto. L'applicazione può creare istanze di classe usando la **parola chiave New.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di un componente a un Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Traduzione in Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




