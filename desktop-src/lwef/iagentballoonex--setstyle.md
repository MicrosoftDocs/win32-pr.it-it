---
title: IAgentBalloonEx SetStyle
description: IAgentBalloonEx SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3961bf5f32aad10c662d9dc2943f32b60fad485621b5adce32e2036e6d2d4275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478541"
---
# <a name="iagentballoonexsetstyle"></a>IAgentBalloonEx::SetStyle

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

Recupera le impostazioni di stile del fumetto della parola del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*
</dt> <dd>

Impostazioni di stile per il fumetto della parola, che può essere una combinazione di uno dei valori seguenti:



| Valore                                                                            | Descrizione                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| **const unsigned short** **BALLOON STYLE \_ \_ BALLOONON = 0x00000001;**<br/>  | Il fumetto è supportato per l'output.                        |
| **const unsigned short** **BALLOON STYLE \_ \_ SIZETOTEXT = 0x0000002;**<br/> | L'altezza del fumetto viene ridimensionata in base all'output di testo. |
| **const unsigned short** **BALLOON STYLE \_ \_ AUTOHIDE = 0x00000004;**<br/>  | Il fumetto viene automaticamente nascosto.                        |
| **const unsigned short** **BALLOON STYLE \_ \_ AUTOPACE = 0x00000008;**<br/>  | L'output di testo viene paced in base alla frequenza di output.          |



 

</dd> </dl>

Quando il bit di stile **BalloonOn** è impostato, il fumetto viene visualizzato quando si usa il metodo [**Speak**](speak-method.md) o [**Think,**](think-method.md) a meno che l'utente non eserciti l'override della relativa visualizzazione nella finestra delle proprietà di Microsoft Agent. Se non è impostato, non viene visualizzato alcun fumetto.

Quando il bit di stile **SizeToText** è impostato, il fumetto della parola ridimensiona automaticamente l'altezza del fumetto in base alle dimensioni correnti del testo specificato nel [**metodo Speak**](speak-method.md) o [**Think.**](think-method.md) Se non è impostata, l'altezza del fumetto si basa sull'impostazione della proprietà number of lines del fumetto. Questo bit di stile è impostato su 1 e un tentativo di usare [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) restituirà un errore.

Quando il **bit di stile AutoHide** è impostato, il fumetto della parola si nasconde automaticamente dopo un breve timeout. Se non è impostato, il fumetto viene visualizzato fino a quando non viene visualizzata una nuova chiamata [**Speak**](speak-method.md) o [**Think,**](think-method.md) il carattere viene nascosto oppure l'utente fa clic o trascina il carattere.

Quando il bit di stile **AutoPace** è impostato, il fumetto della parola segue l'output in base alla frequenza di output corrente, ad esempio una parola alla volta. Quando l'output supera le dimensioni del fumetto, il testo precedente viene automaticamente scorrendo. Se non è impostato, tutto il testo incluso in [**un'istruzione Speak**](speak-method.md) [**o Think**](think-method.md) viene visualizzato contemporaneamente.

La proprietà di stile Balloon può essere impostata anche se l'utente ha disabilitato la visualizzazione del balloon usando la finestra delle proprietà di Microsoft Agent.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

Le impostazioni predefinite per questi bit di stile si basano sulle relative impostazioni quando il carattere viene compilato con l'editor di caratteri di Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md)


 

 





