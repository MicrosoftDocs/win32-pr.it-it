---
title: Oggetto Balloon
description: Oggetto Balloon
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223560"
---
# <a name="the-balloon-object"></a>Oggetto Balloon

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Microsoft Agent supporta la didascalia testuale del metodo [**Speak**](speak-method.md) usando un fumetto di parole. Il metodo [**think**](think-method.md) consente di visualizzare testo senza output audio in un fumetto di parola "pensiero".

Le impostazioni predefinite della finestra fumetto di Word iniziale di un carattere sono definite e compilate nell'editor dei caratteri di Microsoft Agent. Al termine dell'esecuzione, l'utente può eseguire l'override delle proprietà del [**tipo di carattere**](https://www.bing.com/search?q=**Font**) e [**abilitate**](enabled-property.md) per il fumetto. Se un utente modifica le proprietà di Word Balloon, avrà effetto su tutti i caratteri. Sia i [**fumetti di parole che quelli**](speak-method.md) [**di Word usano**](think-method.md) le stesse impostazioni delle proprietà per le dimensioni. È possibile accedere alle proprietà per la parola Balloon di un carattere tramite l'oggetto [**Balloon**](/windows/desktop/lwef/the-balloon-object) , che è un elemento figlio dell'oggetto [**character**](/windows/desktop/lwef/the-characters-object) .

L'oggetto [**Balloon**](/windows/desktop/lwef/the-balloon-object) supporta le proprietà seguenti:

-   [**BackColor**](backcolor-property.md)
-   [**ColoreBordo**](bordercolor-property.md)
-   [**CharsPerLine**](charsperline-property.md)
-   [**Abilitato**](enabled-property.md)
-   [**FontCharSet**](fontcharset-property.md)
-   [**FontName**](fontname-property-bal.md)
-   [**FontBold**](fontbold-property.md)
-   [**CarattereCorsivo**](fontitalic-property.md)
-   [**FontSize**](fontsize-property-bal.md)
-   [**FontStrikeThru**](fontstrikethru-property.md)
-   [**CarattereSottolineato**](fontunderline-property.md)
-   [**ColorePrimoPiano**](forecolor-property.md)
-   [**NumberOfLines**](numberoflines-property.md)
-   [**Stile**](style-property.md)
-   [**Visible**](visible-property-bal.md)

 

 