---
title: Porting di contesti di dispositivo e formati pixel
description: Porting di contesti di dispositivo e formati pixel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- porting in OpenGL, pixel
- Porting OpenGL, pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297857"
---
# <a name="porting-device-contexts-and-pixel-formats"></a>Porting di contesti di dispositivo e formati pixel

Ogni finestra nell'implementazione Microsoft di OpenGL per Windows ha il proprio formato pixel corrente. Un formato pixel è definito da una struttura di dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) . Poiché ogni finestra ha il proprio formato pixel, si ottiene un contesto di dispositivo, si imposta il formato pixel del contesto di dispositivo e quindi si crea un contesto di rendering OpenGL per il contesto di dispositivo. Il contesto di rendering usa automaticamente il formato pixel del relativo contesto di dispositivo.

Il sistema X Window usa anche una struttura di dati, **XVisualInfo**, per specificare le proprietà dei pixel in una finestra. Le strutture **XVisualInfo** contengono una struttura di dati **visiva** che descrive il modo in cui vengono usate le risorse di colore in una schermata specifica.

Nel sistema X Window, **XVisualInfo** viene usato per creare una finestra impostando la finestra sul formato pixel desiderato. La struttura restituita viene utilizzata per creare la finestra e un contesto di rendering. In Windows si crea prima una finestra e si ottiene un handle per un contesto di dispositivo (HDC) della finestra. HDC viene quindi usato per impostare il formato pixel per la finestra. Il contesto di rendering usa il formato pixel della finestra.

Nella tabella seguente vengono confrontate le funzioni visive di sistema X e GLX con le funzioni di formato pixel Windows equivalenti.



| Funzione visiva X/GLX                                                                                     | Funzione formato pixel Windows                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| XVisualInfo \* **glXChooseVisual**(display *\* DPY*, int *Screen*, int *\* attrib*)                               | int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *HDC*, PIXELFORMATDESCRIPTOR *\* PPFD*)                                      |
| int **glXGetConfig**(display *\* DPY*, XVisualInfo *\* Vis*, int *\* attrib*, int *\* value*)                      | int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *HDC*, int *iPixelFormat*, uint *nBytes*, LPPIXELFORMATDESCRIPTOR *PPFD*) |
| XVisualInfo \* **XGetVisualInfo**(display *\* DPY*, Long *vinfo \_ mask*, XVisualInfo *\* vinfo \_ Templ*, int *\* nItems*) | int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *HDC*)                                                                           |
| Quando viene creata una finestra, viene usato l'oggetto *visivo* restituito da **glxChooseVisual** .                                   | BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *HDC*, int *iPixelFormat*, PIXELFORMATDESCRIPTOR *\* PPFD*)                        |



 

Nelle sezioni seguenti vengono illustrati esempi di frammenti di codice in formato pixel per un programma di sistema Windows X e lo stesso codice dopo che è stato trasferito a Windows.

-   [Esempio di codice in formato pixel GLX](glx-pixel-format-code-sample.md)
-   [Esempio di codice in formato pixel Windows](win32-pixel-format-code-sample.md)

Per ulteriori informazioni sui formati pixel, vedere [formati pixel](pixel-formats.md).

 

 




