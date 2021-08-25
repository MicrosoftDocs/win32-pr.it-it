---
title: Tipi di carattere e testo (OpenGL)
description: L'implementazione microsoft di OpenGL in Windows supporta la grafica GDI in una finestra OpenGL a buffer singolo.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL in Windows,tipi di carattere
- OpenGL su Windows,text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966298b6a8d8e5584e761570205a5d3e7be58be3a8dfeb488db2a6f523fc9a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082431"
---
# <a name="fonts-and-text-opengl"></a>Tipi di carattere e testo (OpenGL)

L'implementazione microsoft di OpenGL in Windows supporta la grafica GDI in una finestra OpenGL a buffer singolo. Non supporta la grafica GDI in una finestra OpenGL con doppio buffer. Di conseguenza, è possibile chiamare solo le funzioni di tipo di carattere e testo GDI standard per disegnare testo in una finestra OpenGL a buffer singolo; non è possibile chiamare queste funzioni per disegnare testo in una finestra OpenGL con doppio buffer.

Esiste una soluzione alternativa per questa restrizione al testo nelle finestre con doppio buffer: creare elenchi di visualizzazione OpenGL per immagini bitmap di caratteri e quindi eseguire tali elenchi di visualizzazione per disegnare caratteri. In questo processo sono necessari tre passaggi principali:

1.  Selezionare un tipo di carattere per un contesto di dispositivo, impostando le proprietà del tipo di carattere come desiderato.
2.  Creare un set di elenchi di visualizzazione bitmap in base ai glifi nel tipo di carattere del contesto di dispositivo, un elenco di visualizzazione per ogni glifo che verrà di disegno dall'applicazione.
3.  Disegnare ogni glifo in una stringa usando gli elenchi di visualizzazione delle bitmap.

Per creare gli elenchi di visualizzazione, chiamare [**le funzioni wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) [**e wglUseFontOutlines.**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) Per disegnare caratteri in una stringa usando tali elenchi di visualizzazione, chiamare [**glCallLists**](glcalllists.md).

Per creare applicazioni facili da localizzare e che usano risorse con parsimonia, la creazione e l'archiviazione di questi elenchi di visualizzazione delle immagini degli glifi devono essere gestite con attenzione. Molte lingue, a differenza dell'inglese, hanno alfabeti i cui codici di carattere sono diversi da un set relativamente grande di valori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di tipo di carattere e testo](font-and-text-functions.md)
</dt> </dl>

 

 




