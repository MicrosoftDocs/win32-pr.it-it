---
title: Style (proprietà)
description: Style (proprietà)
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330071"
---
# <a name="style-property"></a>Style (proprietà)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta lo stile di output del fumetto Word del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. ***Caratteri ("*** CharacterID * * *"). Stile Balloon. Style* *  \[  =  \]



| Parte    | Descrizione                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Style* | Intero che rappresenta lo stile di output del fumetto. L'impostazione di stile è un bit con bit corrispondenti a: Balloon-on (bit 0), dimensioni-testo (bit 1), Nascondi automaticamente (bit 2), velocità automatica (bit 3), numero di caratteri per riga (bit 16-23) e numero di righe (bit 24-31). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando il bit di stile Balloon-on è impostato su 1, la parola Balloon viene visualizzata quando viene usato un metodo [**Speak**](https://www.bing.com/search?q=**Speak**) o [**think**](think-method.md) , a meno che l'utente non esegua l'override di questa impostazione nella finestra delle proprietà di Microsoft Agent. Se è impostato su 0, non viene visualizzato un fumetto.

Quando il bit di stile da dimensione a testo è impostato su 1, la parola Balloon ridimensiona automaticamente l'altezza del fumetto alla dimensione corrente del testo per l'istruzione [**Speak**](https://www.bing.com/search?q=**Speak**) o [**think**](think-method.md) . Quando è impostato su 0, l'altezza del fumetto è basata sull'impostazione della proprietà [**numberoflines**](numberoflines-property.md) . Se questo bit di stile è impostato su 1 e si tenta di impostare la proprietà **numberoflines** , Agent genera un errore.

Quando il bit di stile Nascondi automaticamente è impostato su 1, la parola fumetto viene nascosta automaticamente quando l'output parlato viene completato. Quando è impostato su 0, il fumetto rimane visualizzato fino alla [**chiamata successiva o**](https://www.bing.com/search?q=**Speak**) di [**interazione**](think-method.md) utente, il carattere è nascosto oppure l'utente fa clic o trascina il carattere.

Quando il bit di stile di regolazione automatica è impostato su 1, la parola Balloon esegue il ritmo dell'output in base alla frequenza di output corrente, ad esempio una parola alla volta. Quando l'output supera le dimensioni del fumetto, viene automaticamente eseguito lo scorrimento del testo precedente. Se impostato su 0, tutto il testo incluso in un'istruzione [**Speak**](https://www.bing.com/search?q=**Speak**) o [**think**](think-method.md) viene visualizzato in una sola volta.

Per recuperare solo il valore dei quattro bit inferiori **e** il valore restituito dallo **stile** con 255. Per impostare un valore di bit **oppure** il valore restituito con il valore dei bit che si desidera impostare. Per disattivare un bit **e** il valore restituito con un complemento del bit:


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



La proprietà **Style** restituisce anche il numero di caratteri per riga nel byte inferiore della parola superiore e il numero di righe nel byte massimo della parola superiore. Sebbene questa operazione possa essere letta più facilmente usando le proprietà [**CharsPerLine**](charsperline-property.md) e [**numberoflines**](numberoflines-property.md), la proprietà **Style** consente anche di impostare tali valori.

Per modificare, ad esempio, il numero di righe, deselezionare bits 24 to 31 con un'operazione **and** logica prima di impostare il nuovo valore come prodotto del nuovo valore Times 2 ^ 24, aggiunto al valore esistente della proprietà **Style** .


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



Per impostare il numero di caratteri per riga, deselezionare BITS da 16 a 23 con un'operazione **and** logica prima di impostare il nuovo valore come prodotto del nuovo valore Times 2 ^ 16, aggiunto al valore esistente della proprietà Style.


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



La proprietà **Style** può essere impostata anche se l'utente ha disabilitato la visualizzazione del fumetto usando la finestra delle proprietà di Microsoft Agent. Tuttavia, i valori per il numero di righe devono essere compresi tra 1 e 128 e il numero di caratteri per riga deve essere compreso tra 8 e 255. Se si fornisce un valore non valido per la proprietà **Style** , Agent genererà un errore.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

Le impostazioni predefinite per questi bit di stile sono basate sulle impostazioni quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.

 

 




