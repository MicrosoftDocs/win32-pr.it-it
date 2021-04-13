---
title: Funzioni per il tipo di carattere e il testo (OpenGL)
description: Le funzioni seguenti possono essere utilizzate per gestire i tipi di carattere e il testo.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Funzioni WGL, testo
- Funzioni WGL, carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400128"
---
# <a name="font-and-text-functions-opengl"></a>Funzioni per il tipo di carattere e il testo (OpenGL)

Le funzioni seguenti possono essere utilizzate per gestire i tipi di carattere e il testo.



| Funzione Windows                                 | Descrizione                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | Crea un set di elenchi di visualizzazione bitmap di caratteri. I caratteri provengono dal tipo di carattere corrente del contesto di dispositivo specificato. I caratteri vengono specificati come esecuzione consecutiva all'interno del set di glifi del tipo di carattere.                                      |
| [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | Crea un set di elenchi di visualizzazione, in base ai glifi del tipo di carattere del contorno attualmente selezionato di un contesto di dispositivo, da utilizzare con il contesto di rendering corrente. Gli elenchi di visualizzazione vengono utilizzati per creare caratteri 3D di tipi di carattere TrueType. |



 

Le funzioni **wglUseFontBitmaps** e **wglUseFontOutlines** accettano un handle per un contesto di dispositivo e usano il tipo di carattere corrente del contesto di dispositivo come origine per le bitmap. È pertanto necessario impostare il tipo di carattere del contesto di dispositivo e le proprietà del tipo di carattere prima di chiamare **wglUseFontBitmaps** o **wglUseFontOutlines**.

Le funzioni [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) accettano anche un parametro che trasforma il primo glifo del tipo di carattere in un elenco di visualizzazione bitmap e un parametro che specifica il numero di glifi da trasformare negli elenchi di visualizzazione. La funzione crea quindi gli elenchi di visualizzazione per l'esecuzione consecutiva specificata di glifi. Ad esempio:

-   Per creare un set di elenchi di visualizzazione bitmap 224 per tutti i glifi del set di caratteri di Windows, impostare questi due parametri rispettivamente su 32 e 224.
-   Per creare un set di elenchi di visualizzazione bitmap 256 per tutte le icone del set di caratteri OEM, impostare questi due parametri rispettivamente su 0 e 256.
-   Per creare un elenco di visualizzazione bitmap singolo per qualsiasi glifo del set di caratteri singolo, impostare il secondo di questi parametri su 1.

Le funzioni **wglUseFontBitmaps** e **wglUseFontOutlines** rappresentano un glifo null in un tipo di carattere con un elenco di visualizzazione vuoto.

Gli elenchi di visualizzazione creati da una chiamata a **wglUseFontBitmaps** o **wglUseFontOutlines** vengono numerati automaticamente consecutivamente.

Dopo aver chiamato la funzione [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) o [**WglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) , chiamare [**glCallLists**](glcalllists.md) per creare una stringa di caratteri. Per il codice di esempio, vedere [disegno di testo in una finestra Double-Buffered OpenGL](drawing-text-in-a-double-buffered-opengl-window.md) . In questo contesto, **glCallLists** USA ogni carattere in una stringa come indice nella matrice di elenchi di visualizzazione numerati consecutivamente creati da **wglUseFontBitmaps** o **wglUseFontOutlines**.

Al termine della creazione del testo, chiamare la funzione [**glDeleteLists**](gldeletelists.md) per rilasciare il set contiguo di elenchi di visualizzazione creati da **wglUseFontBitmaps** e **wglUseFontOutlines**.

 

 




