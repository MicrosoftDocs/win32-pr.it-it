---
title: Funzioni carattere e testo (OpenGL)
description: Le funzioni seguenti possono essere usate per gestire tipi di carattere e testo.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Funzioni WGL, testo
- Funzioni WGL, tipo di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1341dab969178a08e43c1af0a32c4cac817072ad2d5315cd051df2c87ac3c3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082441"
---
# <a name="font-and-text-functions-opengl"></a>Funzioni carattere e testo (OpenGL)

Le funzioni seguenti possono essere usate per gestire tipi di carattere e testo.



| Windows Funzione                                 | Descrizione                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | Crea un set di elenchi di visualizzazione bitmap di caratteri. I caratteri provengono dal tipo di carattere corrente di un contesto di dispositivo specificato. I caratteri vengono specificati come esecuzione consecutiva all'interno del set di glifi del tipo di carattere.                                      |
| [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | Crea un set di elenchi di visualizzazione, in base ai glifi del tipo di carattere di struttura attualmente selezionato di un contesto di dispositivo, da usare con il contesto di rendering corrente. Gli elenchi di visualizzazione vengono usati per disegnare caratteri 3D di tipi di carattere TrueType. |



 

Le **funzioni wglUseFontBitmaps** e **wglUseFontOutlines** accettano un handle per un contesto di dispositivo e usano il tipo di carattere corrente del contesto di dispositivo come origine per le bitmap. È quindi necessario impostare il tipo di carattere del contesto di dispositivo e le proprietà del tipo di carattere prima di chiamare **wglUseFontBitmaps** o **wglUseFontOutlines**.

Le funzioni [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) accettano anche un parametro che trasforma il primo glifo nel tipo di carattere in un elenco di visualizzazione bitmap e un parametro che specifica il numero di glifi da trasformare in elenchi di visualizzazione. La funzione crea quindi elenchi di visualizzazione per l'esecuzione consecutiva di glifi specificata. Esempio:

-   Per creare un set di 224 elenchi di visualizzazione bitmap per tutti i glifi del set di caratteri Windows, impostare questi due parametri rispettivamente su 32 e 224.
-   Per creare un set di 256 elenchi di visualizzazione bitmap per tutti i glifi del set di caratteri OEM, impostare questi due parametri rispettivamente su 0 e 256.
-   Per creare un singolo elenco di visualizzazione bitmap per qualsiasi singolo glifo del set di caratteri, impostare il secondo di questi parametri su 1.

Le **funzioni wglUseFontBitmaps** e **wglUseFontOutlines** rappresentano un glifo Null in un tipo di carattere con un elenco di visualizzazione vuoto.

Gli elenchi di visualizzazione creati da una chiamata a **wglUseFontBitmaps** o **wglUseFontOutlines** vengono numerati automaticamente consecutivamente.

Dopo aver chiamato [**la funzione wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) o [**wglUseFontOutlines,**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) chiamare [**glCallLists**](glcalllists.md) per disegnare una stringa di caratteri. Vedere [Disegno di testo in una finestra Double-Buffered OpenGL per](drawing-text-in-a-double-buffered-opengl-window.md) il codice di esempio. In questo contesto, **glCallLists** usa ogni carattere in una stringa come indice nella matrice di elenchi di visualizzazione numerati consecutivamente creati da **wglUseFontBitmaps** o **wglUseFontOutlines**.

Al termine del disegno del testo, chiamare la funzione [**glDeleteLists**](gldeletelists.md) per rilasciare il set contiguo di elenchi di visualizzazione creati da **wglUseFontBitmaps** e **wglUseFontOutlines**.

 

 




