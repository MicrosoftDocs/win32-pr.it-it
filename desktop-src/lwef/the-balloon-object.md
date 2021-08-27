---
title: Oggetto balloon
description: Oggetto balloon
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc2ad1256b040588121dcb92fc8f66fea540b3051b92a6fe5273eb2f81107b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745973"
---
# <a name="the-balloon-object"></a>Oggetto balloon

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Microsoft Agent supporta la didascalia testuale del [**metodo Speak**](speak-method.md) usando un fumetto per cartoni animati. Il [**metodo Think**](think-method.md) consente di visualizzare il testo senza output audio in un fumetto di parole "pensato".

I valori predefiniti della finestra iniziale del fumetto di un carattere vengono definiti e compilati nell'editor di caratteri di Microsoft Agent. Dopo l'esecuzione, le proprietà [**Enabled**](enabled-property.md) e [**Font**](https://www.bing.com/search?q=**Font**) del fumetto possono essere sostituite dall'utente. Se un utente modifica le proprietà del fumetto, influisce su tutti i caratteri. Le aree [**commenti e**](speak-method.md) [**le**](think-method.md) aree commenti usano le stesse impostazioni delle proprietà per le dimensioni. È possibile accedere alle proprietà per il fumetto di parole di un carattere tramite l'oggetto [**Balloon,**](/windows/desktop/lwef/the-balloon-object) che è un elemento figlio [**dell'oggetto Character.**](/windows/desktop/lwef/the-characters-object)

[**L'oggetto Balloon**](/windows/desktop/lwef/the-balloon-object) supporta le proprietà seguenti:

-   [**Backcolor**](backcolor-property.md)
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

 

 