---
title: IAgentBalloonEx GetStyle
description: IAgentBalloonEx GetStyle
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e21ab22a9aa5a85fdbe1bc541f29df75313cdce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856526"
---
# <a name="iagentballoonexgetstyle"></a>IAgentBalloonEx:: GetStyle

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

Recupera le impostazioni di stile del fumetto Word del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*
</dt> <dd>

Impostazioni di stile per la parola Balloon, che può essere una combinazione dei valori seguenti:



| Valore                                                                           | Descrizione                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| **const unsigned short** **Balloon \_ Style \_ BALLOONON = 0x00000001;**<br/> | Il fumetto è supportato per l'output.                        |
| **const unsigned short** **Balloon \_ Style \_ SIZETOTEXT = 0x0000002;**           | L'altezza del fumetto è dimensionata in modo da contenere l'output di testo. |
| Nascondi automaticamente lo stile di un **breve fumetto const senza segno** **\_ \_ = 0x00000004;**            | Il fumetto viene nascosto automaticamente.                        |
| autopace **senza segno const unsigned short** **Balloon \_ \_ = 0x00000008;**            | L'output di testo viene gestito in base alla frequenza di output.          |



 

</dd> </dl>

Quando viene impostato il bit di stile **BalloonOn** , la parola Balloon viene visualizzata quando viene usato il metodo [**Speak**](speak-method.md) o [**think**](think-method.md) , a meno che l'utente non esegua l'override della relativa visualizzazione tramite la finestra delle proprietà di Microsoft Agent. Quando non è impostato, non viene visualizzato alcun fumetto.

Quando è impostato il bit di stile **SizeToText** , la parola Balloon ridimensiona automaticamente l'altezza del fumetto alla dimensione corrente del testo specificato nel metodo [**Speak**](speak-method.md) o [**think**](think-method.md) . Quando non è impostato, l'altezza del fumetto è basata sull'impostazione della proprietà Number of Lines del fumetto. Questo bit di stile è impostato su 1 e un tentativo di utilizzare [**IAgentBalloonEx:: SetNumLines**](iagentballoonex--setnumlines.md) comporterà un errore.

Quando è impostato il bit di stile **Nascondi** automaticamente, la parola fumetto viene nascosta automaticamente dopo un timeout breve. Quando non è impostato, il fumetto viene visualizzato fino a quando [](think-method.md) non viene visualizzata una nuova chiamata, il carattere è [**nascosto oppure l'**](speak-method.md) utente fa clic o trascina il carattere.

Quando è impostato il bit di stile **autopace** , la parola Balloon esegue il ritmo dell'output in base alla frequenza di output corrente, ad esempio una parola alla volta. Quando l'output supera le dimensioni del fumetto, viene automaticamente eseguito lo scorrimento del testo precedente. Quando non è impostato, tutto il testo incluso in un'istruzione [**Speak**](speak-method.md) o [**think**](think-method.md) viene visualizzato in una sola volta.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

Le impostazioni predefinite per questi bit di stile sono basate sulle impostazioni quando il carattere viene compilato tramite l'editor dei caratteri di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloonEx:: Sestyle**](iagentballoonex--setstyle.md)


 

 





