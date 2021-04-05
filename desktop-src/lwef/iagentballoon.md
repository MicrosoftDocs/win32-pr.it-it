---
title: IAgentBalloon
description: IAgentBalloon
ms.assetid: 94a48cd9-bea5-4993-8991-50c6c86a646b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b811956e368abbaf2d2782c68017084f5e17a09f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725570"
---
# <a name="iagentballoon"></a>IAgentBalloon

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

**IAgentBalloon** definisce un'interfaccia che consente alle applicazioni di eseguire query sulle proprietà per l'aerostato di Word di Microsoft Agent. Queste funzioni sono disponibili anche da [**IAgentBalloonEx**](https://www.bing.com/search?q=**IAgentBalloonEx**).

Le impostazioni predefinite iniziali per il fumetto di Word di un carattere sono impostate nell'editor dei caratteri di Microsoft Agent, ma una volta che l'applicazione è in esecuzione, è possibile che l'utente esegua l'override delle proprietà [**Enabled**](enabled-property.md) e [font](fontname-property.md) . Se un utente modifica le proprietà del fumetto, la modifica avrà effetto su tutti i caratteri. Le proprietà dell'oggetto [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) si applicano anche all'output di testo tramite il metodo [**think**](think-method.md) .

**Metodi nell'ordine Vtable**



| Metodi IAgentBalloon                                       | Descrizione                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [GetEnabled](iagentballoon--getenabled.md)                 | Restituisce un valore che indica se la parola Balloon è abilitata.                                          |
| [GetNumLines](iagentballoon--getnumlines.md)               | Restituisce il numero di righe visualizzate nella parola Balloon.                            |
| [GetNumCharsPerLine](iagentballoon--getnumcharsperline.md) | Restituisce il numero medio di caratteri per riga visualizzato nell'oggetto Balloon di Word.      |
| [GetFontName](iagentballoon--getfontname.md)               | Restituisce il nome del tipo di carattere visualizzato nella parola Balloon.                           |
| [GetFontSize](iagentballoon--getfontsize.md)               | Restituisce la dimensione del tipo di carattere visualizzato nella parola Balloon.                           |
| [GetFontBold](iagentballoon--getfontbold.md)               | Restituisce un valore che indica se il tipo di carattere visualizzato nella parola Balloon è in grassetto.                       |
| [GetFontItalic](iagentballoon--getfontitalic.md)           | Restituisce un valore che indica se il tipo di carattere visualizzato nella parola Balloon è in corsivo.                     |
| [GetFontStrikethru](iagentballoon--getfontstrikethru.md)   | Restituisce un valore che indica se il tipo di carattere visualizzato nella parola Balloon viene visualizzato come barrato. |
| [GetFontUnderline](iagentballoon--getfontunderline.md)     | Restituisce un valore che indica se il tipo di carattere visualizzato nella parola Balloon è sottolineato.                 |
| [GetForeColor](iagentballoon--getforecolor.md)             | Restituisce il colore di primo piano visualizzato nell'aerostato di parole.                           |
| [GetBackColor](iagentballoon--getbackcolor.md)             | Restituisce il colore di sfondo visualizzato nella parola Balloon.                           |
| [GetBorderColor](iagentballoon--getbordercolor.md)         | Restituisce il colore del bordo visualizzato nell'aerostato di Word.                               |
| [SetVisible](iagentballoon--setvisible.md)                 | Imposta la parola Balloon come visibile.                                                  |
| [GetVisible](iagentballoon--getvisible.md)                 | Restituisce l'impostazione di visibilità per la parola Balloon.                                  |
| [Sefontname](iagentballoon--setfontname.md)               | Imposta il tipo di carattere utilizzato nella parola Balloon.                                               |
| [SetFontSize](iagentballoon--setfontsize.md)               | Imposta la dimensione del carattere utilizzata nell'aerostato di Word.                                          |
| [SetFontCharSet](iagentballoon--setfontcharset.md)         | Imposta il set di caratteri utilizzato nella parola Balloon.                                      |
| [GetFontCharSet](iagentballoon--getfontcharset.md)         | Restituisce il set di caratteri utilizzato nella parola Balloon.                                   |



 

 

 