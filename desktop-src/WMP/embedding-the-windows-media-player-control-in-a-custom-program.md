---
title: Incorporamento del controllo Media Player Windows in un programma personalizzato
description: Incorporamento del controllo Media Player Windows in un programma personalizzato
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- incorporamento, programmi personalizzati
- incorporamento di programmi personalizzati
- incorporamento, programmi basati su Visual Basic
- Incorporamento di programmi basati su Visual Basic
- incorporamento, utilizzo manuale di metodi COM
- incorporamento manuale mediante i metodi COM
- incorporamento, programmi C++
- Incorporamento del programma C++
- incorporamento, programmi di Visual Studio
- Visual Studio, incorporamento del programma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044490"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a>Incorporamento del controllo Media Player Windows in un programma personalizzato

Poiché il controllo ActiveX di Windows Media Player è basato sulla tecnologia Microsoft Component Object Model (COM), è possibile incorporarlo nei programmi scritti con molti linguaggi di programmazione diversi. Il controllo Windows Media Player rappresenta un modo semplice per aggiungere sofisticate funzionalità multimediali digitali a qualsiasi programma.

In Microsoft Visual Basic è possibile aggiungere il controllo alla casella degli strumenti del controllo, inserirlo in un form e modificare le proprietà del controllo nella finestra Proprietà. Se si vuole un'interfaccia utente personalizzata, è possibile inserire i pulsanti di comando nel form e aggiungere il codice che gestisce il controllo Media Player di Windows. Incorporare il controllo in un programma basato su Visual Basic è molto simile all'incorporamento in un documento di Office e alla programmazione con VBA.

In alternativa, è possibile incorporare il controllo manualmente usando i metodi COM per creare un'istanza del controllo e accedere alle interfacce COM documentate in [riferimento al modello a oggetti per C++](object-model-reference-for-c.md).

Quando si incorpora il controllo Windows Media Player in un programma C++, è possibile implementare interfacce COM che consentono di eseguire il controllo in modalità remota. Ciò significa che il controllo incorporato condivide lo stesso motore di riproduzione della modalità completa del lettore e gli utenti possono spostarsi tra la modalità completa e lo stato ancorato senza interrompere la riproduzione di file multimediali digitali. È anche possibile controllare ciò che viene visualizzato nei vari riquadri del lettore in modalità completa quando gli utenti passano allo stato non ancorato.

Con l'incorporamento C++, è anche possibile applicare un file di definizione dell'interfaccia per il controllo Player incorporato. Si tratta di un modo semplice per creare codice di interfaccia utente leggero che è possibile gestire separatamente dal codice del programma principale.

Microsoft Visual Studio supporta l'incorporamento di controlli ActiveX, incluso il controllo Media Player di Windows. Quando si sceglie di eseguire questa operazione, Visual Studio crea un nuovo assembly di interoperabilità alternativo per gestire l'interoperabilità tra il .NET Framework e il controllo Media Player di Windows. Visual Studio usa lo strumento tlbimp.exe .NET Framework per creare l'assembly di interoperabilità. Ciò significa che le firme visualizzate quando si usa la funzionalità IntelliSense in Visual Studio usano la semantica determinata dalla versione corrente di Tlbimp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Incorporamento del controllo Media Player Windows**](embedding-the-windows-media-player-control.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows in un programma C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows in una soluzione .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows con Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




