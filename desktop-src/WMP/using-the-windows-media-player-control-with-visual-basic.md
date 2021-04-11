---
title: Uso del controllo Media Player di Windows con Visual Basic
description: Uso del controllo Media Player di Windows con Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, Visual Basic
- Modello a oggetti di Windows Media Player, Visual Basic
- modello a oggetti, Visual Basic
- Windows Media Player Mobile Visual Basic
- Controllo ActiveX di Windows Media Player, Visual Basic
- Controllo ActiveX Windows Media Player Mobile Visual Basic
- Controllo ActiveX, Visual Basic
- Incorporamento di programmi basati su Visual Basic
- incorporamento, programmi basati su Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330836"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a>Uso del controllo Media Player di Windows con Visual Basic

In questa sezione viene descritto come utilizzare il controllo ActiveX Windows Media Player 9 o versioni successive nelle applicazioni create con Microsoft Visual Basic 6,0.

## <a name="getting-started"></a>Introduzione

Per aggiungere il controllo Media Player Windows alla casella degli strumenti, selezionare innanzitutto **componenti** dal menu **progetto** . Nella finestra di dialogo componenti selezionare la casella di controllo accanto a "Windows Media Player". Nella parte inferiore della finestra di dialogo verificare che il file selezionato sia wmp.dll. Dopo aver chiuso la finestra di dialogo, è possibile inserire un'istanza del controllo Media Player Windows sul form nel modo consueto.

È possibile impostare molte proprietà del controllo usando il Finestra Proprietà. Per impostare alcune proprietà, è necessario utilizzare la finestra di dialogo Proprietà Media Player di Windows, che è possibile aprire utilizzando l'elemento "(personalizzato)" nel Finestra Proprietà.

## <a name="object-references"></a>Riferimenti a oggetti

È possibile utilizzare determinate proprietà del controllo lettore per ottenere riferimenti a oggetti specifici. Ad esempio, la proprietà **cdromcollection** restituisce un riferimento a un oggetto **cdromcollection** . È necessario assegnare tale riferimento a una variabile dichiarata come interfaccia corrispondente. Nel caso della proprietà **cdromcollection** , ad esempio, si assegna il relativo valore restituito a una variabile di tipo **IWMPCdromCollection**.

Leggere l'argomento [interfacce](interfaces.md) nel [riferimento del modello a oggetti per C++](object-model-reference-for-c.md) per identificare gli oggetti che implementano più interfacce. In questi casi, è necessario dichiarare una variabile oggetto come l'interfaccia con il numero più elevato documentato in questo SDK per avere accesso a tutte le proprietà e i metodi di tale oggetto. Ad esempio, è necessario assegnare il valore della proprietà **currentMedia** del controllo Windows Media Player a una variabile dichiarata come **IWMPMedia3** per assicurarsi di avere accesso ai metodi **getAttributeCountByType** e **getItemInfoByType** .

> [!Note]  
> L'oggetto **windowsmediaplayer** implementa tutte le proprietà e i metodi delle interfacce **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3** e **IWMPPlayer4** . Non è necessario dichiarare variabili separate per nessuna di queste interfacce. È possibile accedere a tutti i relativi membri usando il nome assegnato all'istanza di **windowsmediaplayer** .

 

Nella Visual Basic Visualizzatore oggetti verranno visualizzate numerose interfacce destinate all'uso privato da parte del controllo Windows Media Player, incluse alcune che supportano gli sviluppatori di skin. È consigliabile utilizzare solo gli oggetti, le proprietà, i metodi e gli eventi documentati in questo SDK.

## <a name="additional-tips"></a>Suggerimenti aggiuntivi

-   Nella documentazione di riferimento viene illustrata la sintassi di JScript. In JScript gli argomenti passati ai metodi sono sempre racchiusi tra parentesi. In Visual Basic 6,0 gli argomenti passati ai metodi che non restituiscono un valore non devono essere racchiusi tra parentesi.
-   Alcune proprietà o metodi potrebbero non essere visualizzati nella funzionalità di completamento automatico del codice nell'editor di codice Visual Basic. È comunque possibile usare tali membri digitando i relativi nomi esattamente come appaiono in questa documentazione.
-   Gestire l'aspetto visivo del controllo utilizzando la proprietà **uiMode** . Questa operazione può essere eseguita in due modi. È possibile utilizzare l'elenco a discesa **Seleziona modalità** nella finestra di dialogo Proprietà Media Player di Windows oppure è possibile digitare il valore corretto nel finestra Proprietà.

    In particolare, non utilizzare la proprietà **Visible** per nascondere il controllo; Assegnare invece il valore "invisibile" alla proprietà **uiMode** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida al controllo del lettore**](player-control-guide.md)
</dt> </dl>

 

 




