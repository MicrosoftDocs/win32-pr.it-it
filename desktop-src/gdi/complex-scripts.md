---
description: Sebbene le funzioni descritte nella precedente funzionino correttamente per molti linguaggi, potrebbero non occuparsi delle esigenze di alfabeti non latini.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Script complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880326"
---
# <a name="complex-scripts"></a>Script complessi

Sebbene le funzioni descritte nella precedente funzionino correttamente per molti linguaggi, potrebbero non occuparsi delle esigenze di alfabeti non latini. Gli *alfabeti non latini* sono linguaggi il cui modulo stampato non viene sottoposto a rendering in modo semplice. Uno script complesso, ad esempio, può consentire il rendering bidirezionale, il Shaping contestuale dei glifi o la combinazione di caratteri. A causa di questi requisiti speciali, il controllo dell'output di testo deve essere molto flessibile.

Le funzioni che visualizzano [**testo text**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)out, [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)e [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) sono state estese per supportare script complessi. In generale, questo supporto è trasparente per l'applicazione. Tuttavia, le applicazioni devono salvare i caratteri in un buffer e visualizzare un'intera riga di testo in una sola volta, in modo che i moduli di definizione degli script complessi possano usare il contesto per riordinare e generare correttamente i glifi. Inoltre, poiché la larghezza di un glifo può variare in base al contesto, le applicazioni devono usare [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) per determinare la lunghezza della riga invece di usare la larghezza dei caratteri memorizzata nella cache.

Inoltre, le applicazioni complesse compatibili con gli script devono considerare l'aggiunta del supporto per l'ordine di lettura da destra a sinistra e l'allineamento a destra per le applicazioni. È possibile alternare l'ordine di lettura o l'allineamento tra Left e Right con il codice seguente:


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



Per impostare entrambi gli attributi contemporaneamente, eseguire l'istruzione seguente e quindi chiamare [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) e [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), come illustrato in precedenza:


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



È anche possibile elaborare script complessi con Uniscribe. Uniscribe è un set di funzioni che consentono un elevato livello di controllo per gli script complessi. Per altre informazioni, vedere [Uniscribe](../intl/uniscribe.md) ed [elaborazione di script complessi](../intl/processing-complex-scripts.md).

 

 
