---
title: Porting di contesti di dispositivo e formati pixel
description: Porting di contesti di dispositivo e formati pixel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- portabilità in OpenGL, pixel
- Portabilità OpenGL, pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b292fb3f27eb2ed888a4db94198944f41a8571114b38c5c90b994cdd1cb6367f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144084"
---
# <a name="porting-device-contexts-and-pixel-formats"></a>Porting di contesti di dispositivo e formati pixel

Ogni finestra nell'implementazione Microsoft di OpenGL per Windows ha il proprio formato pixel corrente. Un formato pixel è definito da una struttura di [**dati PIXELFORMATDESCRIPTOR.**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) Poiché ogni finestra ha un proprio formato pixel, si ottiene un contesto di dispositivo, si imposta il formato pixel del contesto di dispositivo e quindi si crea un contesto di rendering OpenGL per il contesto di dispositivo. Il contesto di rendering usa automaticamente il formato pixel del contesto di dispositivo.

X Window System usa anche una struttura di dati, **XVisualInfo,** per specificare le proprietà dei pixel in una finestra. **Le strutture XVisualInfo** contengono una **struttura di dati visivi** che descrive come vengono usate le risorse di colore in una schermata specifica.

Nel sistema di finestre X, **XVisualInfo viene** usato per creare una finestra impostando la finestra sul formato pixel desiderato. La struttura restituita viene usata per creare la finestra e un contesto di rendering. In Windows prima di tutto si crea una finestra e si ottiene un handle per un contesto di dispositivo (HDC) della finestra. L'HDC viene quindi usato per impostare il formato pixel per la finestra. Il contesto di rendering usa il formato pixel della finestra.

La tabella seguente confronta le funzioni visive X Window System e GLX con le funzioni equivalenti Windows formato pixel.



| Finestra X/funzione visiva GLX                                                                                     | Windows di formato pixel                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| XVisualInfo \* **glXChooseVisual**( Display *\* dpy*,int *screen*,int *\* attribList*)                               | int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\* ppfd*)                                      |
| int **glXGetConfig**( Display *\* dpy*,XVisualInfo *\* vis*,int *\* attribList*,int *\* value*)                      | int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*,int *iPixelFormat*,UINT *nBytes*,LPPIXELFORMATDESCRIPTOR *ppfd*) |
| XVisualInfo \* **XGetVisualInfo**( Display *\* dpy*,long *vinfo \_ mask*,XVisualInfo *\* vinfo \_ templ*,int *\* nitems*) | int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)                                                                           |
| *L'oggetto* visivo **restituito da glxChooseVisual** viene usato quando viene creata una finestra.                                   | BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*,int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\* ppfd*)                        |



 

Le sezioni seguenti forniscono esempi di frammenti di codice in formato pixel per un programma X Window System e lo stesso codice dopo che è stato Windows.

-   [Esempio di codice per il formato pixel GLX](glx-pixel-format-code-sample.md)
-   [Windows Esempio di codice per il formato pixel](win32-pixel-format-code-sample.md)

Per altre informazioni sui formati pixel, vedere [Formati di pixel.](pixel-formats.md)

 

 




