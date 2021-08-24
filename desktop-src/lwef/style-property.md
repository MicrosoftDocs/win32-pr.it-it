---
title: Proprietà Style
description: Proprietà Style
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37196aead474c5364c7a94780686707b74bab0f4c4831381cf4c40e47e350e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715881"
---
# <a name="style-property"></a>Proprietà Style

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta lo stile di output del fumetto del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Stile_ *  \[  =  *Balloon.Style*\]



| Parte    | Descrizione                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Style* | Intero che rappresenta lo stile di output del balloon. L'impostazione di stile è un campo di bit con bit corrispondenti a: balloon-on (bit 0), dimensione-testo (bit 1), nascondi automaticamente (bit 2), velocità automatica (bit 3), numero di caratteri per riga (bit 16-23) e numero di righe (bit 24-31). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando il bit di stile balloon-on è impostato su 1, il fumetto viene visualizzato quando si usa un metodo [**Speak**](https://www.bing.com/search?q=**Speak**) o [**Think,**](think-method.md) a meno che l'utente non eserciti l'override di questa impostazione nella finestra delle proprietà di Microsoft Agent. Se impostato su 0, non viene visualizzato un balloon.

Quando il bit di stile da dimensione a testo è impostato su 1, l'altezza del fumetto viene automaticamente ridimensionata in base alle dimensioni correnti del testo per l'istruzione [**Speak**](https://www.bing.com/search?q=**Speak**) o [**Think.**](think-method.md) Se impostato su 0, l'altezza del balloon si basa sull'impostazione della proprietà [**NumberOfLines.**](numberoflines-property.md) Se questo bit di stile è impostato su 1 e si tenta di impostare la **proprietà NumberOfLines,** Agent genera un errore.

Quando il bit di stile nascondi automaticamente è impostato su 1, il fumetto viene nascosto automaticamente al termine dell'output parlato. Se impostato su 0, il fumetto rimane visualizzato fino alla successiva chiamata [**Speak**](https://www.bing.com/search?q=**Speak**) o [**Think,**](think-method.md) il carattere non viene nascosto o l'utente fa clic o trascina il carattere.

Quando il bit di stile della velocità automatica è impostato su 1, il fumetto della parola pace l'output in base alla frequenza di output corrente, ad esempio, una parola alla volta. Quando l'output supera le dimensioni del balloon, viene automaticamente visualizzato il testo precedente. Se impostato su 0, tutto il testo incluso in un'istruzione [**Speak**](https://www.bing.com/search?q=**Speak**) o [**Think**](think-method.md) viene visualizzato contemporaneamente.

Per recuperare solo il valore dei quattro bit inferiore e **il** valore restituito da **Style** con 255. Per impostare un valore di bit **oppure** il valore restituito con il valore dei bit da impostare. Per disattivare un bit e **il** valore restituito con il complemento del bit:


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



La **proprietà Style** restituisce anche il numero di caratteri per riga nel byte inferiore della parola superiore e il numero di righe nel byte superiore della parola superiore. Anche se questa operazione può essere letta più facilmente usando le [**proprietà CharsPerLine**](charsperline-property.md) e [**NumberOfLines,**](numberoflines-property.md)la **proprietà Style** consente anche di impostare tali valori.

Ad esempio, per modificare il numero di righe, cancellare i bit da 24 a 31 con un'operazione **AND** logica prima di impostare il nuovo valore come prodotto del nuovo valore per 2^24, aggiunto al valore esistente della proprietà **Style.**


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



Per impostare il numero di caratteri per riga, cancellare i bit da 16 a 23 con un'operazione **AND** logica prima di impostare il nuovo valore come prodotto del nuovo valore per 2^16, aggiunto al valore esistente della proprietà Style.


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



La **proprietà Style** può essere impostata anche se l'utente ha disabilitato la visualizzazione del balloon tramite la finestra delle proprietà di Microsoft Agent. Tuttavia, i valori per il numero di righe devono essere compresi tra 1 e 128 e i caratteri numerici per riga devono essere compresi tra 8 e 255. Se si specifica un valore non valido per la **proprietà Style,** Agent genererà un errore.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

Le impostazioni predefinite per questi bit di stile si basano sulle relative impostazioni quando il carattere viene compilato con l'editor di caratteri di Microsoft Agent.

 

 




