---
description: Viene descritto come creare un oggetto PenInputPanel.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Creazione di un oggetto PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305346"
---
# <a name="creating-a-peninputpanel-object"></a>Creazione di un oggetto PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) è stato sostituito da [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) e [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)). Vedere la pagina relativa alla [programmazione del pannello input di testo](programming-the-text-input-panel.md).\]

I costruttori di codice gestito costituiscono un modo pratico per creare un oggetto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) e collegarlo a un controllo in un unico passaggio. In questo \# esempio C viene creato un oggetto PenInputPanel che viene collegato a un controllo [InkEdit](/previous-versions/ms835842(v=msdn.10)) esistente, `InkEdit1` , con una riga di codice.


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



Lo stesso esempio in Visual Basic .NET ha un aspetto simile al seguente:


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



Questa tecnica è utile nei casi in cui un oggetto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) verrà associato a un singolo controllo per tutta la sua durata. Nei casi in cui si desidera utilizzare un oggetto PenInputPanel e associarlo a più controlli, come illustrato nell' [esempio PenInputPanel](peninputpanel-sample.md), utilizzare la proprietà [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) per modificare il controllo a cui è associato l'oggetto PenInputPanel.

Per alleghi un oggetto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un controllo senza utilizzare un costruttore, utilizzare la proprietà [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) . Usare questa tecnica per i linguaggi che non supportano i costruttori gestiti, ad esempio C++.

 

 
