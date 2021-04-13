---
title: Tipi di carattere e testo (OpenGL)
description: L'implementazione Microsoft di OpenGL in Windows supporta la grafica GDI in una finestra OpenGL con singolo buffer.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL per Windows, tipi di carattere
- OpenGL per Windows, testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400127"
---
# <a name="fonts-and-text-opengl"></a>Tipi di carattere e testo (OpenGL)

L'implementazione Microsoft di OpenGL in Windows supporta la grafica GDI in una finestra OpenGL con singolo buffer. Non supporta la grafica GDI in una finestra OpenGL con doppio buffer. Pertanto, è possibile chiamare solo le funzioni standard GDI font e Text per creare testo in una finestra OpenGL con buffer singolo; non è possibile chiamare queste funzioni per creare testo in una finestra OpenGL con doppio buffer.

Esiste una soluzione alternativa per questa restrizione sul testo nelle finestre con doppio buffer: compila gli elenchi di visualizzazione OpenGL per le immagini bitmap di caratteri, quindi Esegui gli elenchi di visualizzazione per creare caratteri. Questo processo prevede tre passaggi principali:

1.  Selezionare un tipo di carattere per un contesto di dispositivo, impostando le proprietà del tipo di carattere come desiderato.
2.  Creare un set di elenchi di visualizzazione bitmap basati sui glifi nel tipo di carattere del contesto di dispositivo, un elenco di visualizzazione per ogni glifo che l'applicazione trarrà.
3.  Creare ogni glifo in una stringa usando gli elenchi di visualizzazione bitmap.

Per creare gli elenchi di visualizzazione, chiamare le funzioni [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) . Per creare caratteri in una stringa usando gli elenchi di visualizzazione, chiamare [**glCallLists**](glcalllists.md).

Per creare applicazioni facili da localizzare e che usano le risorse in modo sporadico, è necessario gestire con attenzione la creazione e l'archiviazione degli elenchi di visualizzazione delle immagini del glifo. Molti linguaggi, a differenza della lingua inglese, presentano alfabeti i cui codici di caratteri sono compresi in un set di valori relativamente grande.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di tipo carattere e testo](font-and-text-functions.md)
</dt> </dl>

 

 




