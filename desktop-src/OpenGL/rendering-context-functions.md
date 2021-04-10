---
title: Funzioni del contesto di rendering
description: Cinque funzioni WGL gestiscono i contesti di rendering, come descritto nella tabella seguente.
ms.assetid: e03ec03d-2a85-49de-a2be-fe81a5ec5f7f
keywords:
- Funzioni WGL, contesti di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8d3a8ea0333154d3145711829ab23e262fa485
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963416"
---
# <a name="rendering-context-functions"></a>Funzioni del contesto di rendering

Cinque funzioni WGL gestiscono i contesti di rendering, come descritto nella tabella seguente.



| WGL (funzione)                                         | Descrizione                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)         | Crea un nuovo contesto di rendering.                                                             |
| [**WglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)             | Imposta il contesto di rendering corrente di un thread.                                                   |
| [**WglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) | Ottiene un handle per il contesto di rendering corrente di un thread.                                    |
| [**WglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)           | Ottiene un handle per il contesto di dispositivo associato al contesto di rendering corrente di un thread. |
| [**WglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)         | Elimina un contesto di rendering.                                                                 |



 

La funzione [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) accetta un handle del contesto di dispositivo come parametro e restituisce un handle del contesto di rendering. Il contesto di rendering creato è adatto per il disegno sul dispositivo a cui fa riferimento l'handle del contesto di dispositivo. In particolare, il formato pixel corrisponde al formato pixel del contesto di dispositivo. Dopo aver creato un contesto di rendering, è possibile rilasciare o eliminare il contesto di dispositivo. Vedere [contesti di dispositivo](/windows/desktop/gdi/device-contexts) per altri dettagli sulla creazione, il recupero, il rilascio e l'eliminazione di un contesto di dispositivo.

> [!Note]  
> Il contesto di dispositivo inviato a [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) deve essere un contesto di dispositivo di visualizzazione, un contesto di dispositivo di memoria o un contesto di dispositivo stampante a colori che usa quattro o più bit per pixel. Il contesto di dispositivo non può essere un contesto di dispositivo stampante monocromatico.

 

La funzione [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) accetta un handle del contesto di rendering e un handle del contesto di dispositivo come parametri. Tutte le chiamate OpenGL successive eseguite dal thread vengono eseguite tramite tale contesto di rendering e vengono disegnate sul dispositivo a cui fa riferimento il contesto di dispositivo. Non è necessario che il contesto di dispositivo sia uguale a quello passato a **wglCreateContext** quando è stato creato il contesto di rendering, ma deve trovarsi nello stesso dispositivo e avere lo stesso formato pixel. La chiamata a **wglMakeCurrent** crea un'associazione tra il contesto di rendering fornito e il contesto di dispositivo. Non è possibile rilasciare o eliminare il contesto di dispositivo associato a un contesto di rendering corrente fino a quando non si rende il contesto di rendering non aggiornato.

Una volta che un thread ha un contesto di rendering corrente, può effettuare chiamate grafiche OpenGL. Tutte le chiamate devono passare attraverso un contesto di rendering. Non accade nulla se si effettuano chiamate grafiche OpenGL da un thread che non dispone di un contesto di rendering corrente.

La funzione [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) non accetta parametri e restituisce un handle al contesto di rendering corrente del thread chiamante. Se il thread non dispone di un contesto di rendering corrente, il valore restituito è **null**.

Quando si ottiene un handle per il contesto di dispositivo associato al contesto di rendering corrente di un thread chiamando [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc), l'associazione viene creata quando un contesto di rendering viene reso corrente.

È possibile suddividere l'associazione tra un contesto di rendering corrente e un thread chiamando [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) con uno dei due handle seguenti:

-   Handle di contesto per il rendering **null**
-   Handle diverso da quello originariamente chiamato

Dopo la chiamata di [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) con il parametro handle del contesto di rendering impostato su **null**, il thread chiamante non dispone di un contesto di rendering corrente. Il contesto di rendering viene rilasciato dalla connessione al thread e l'associazione del contesto di rendering a un contesto di dispositivo termina. OpenGL Scarica tutti i comandi di disegno e può rilasciare alcune risorse. Non verrà eseguito alcun disegno OpenGL fino alla successiva chiamata a **wglMakeCurrent**, perché il thread non può eseguire chiamate grafiche OpenGL fino a ottenere un contesto di rendering corrente.

Il secondo modo per interrompere l'associazione tra un contesto di rendering e un thread consiste nel chiamare **wglMakeCurrent** con un contesto di rendering diverso. Dopo una chiamata di questo tipo, il thread chiamante ha un nuovo contesto di rendering corrente, il precedente contesto di rendering corrente viene rilasciato dalla connessione al thread e l'associazione del contesto di rendering corrente precedente a un contesto di dispositivo termina.

La funzione [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext) accetta un solo parametro, ovvero l'handle per il contesto di rendering da eliminare. Prima di chiamare **wglDeleteContext**, rendere il contesto di rendering non corrente chiamando [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)ed eliminare o rilasciare il contesto di dispositivo associato chiamando [DeleteDC](/windows/desktop/api/wingdi/nf-wingdi-deletedc) o [ReleaseDC](/windows/desktop/api/winuser/nf-winuser-releasedc) nel modo appropriato.

È un errore per un thread eliminare un contesto di rendering che è il contesto di rendering corrente di un altro thread. Tuttavia, se un contesto di rendering è il contesto di rendering corrente del thread chiamante, **wglDeleteContext** Scarica tutti i comandi di disegno OpenGL e rende il contesto di rendering non aggiornato prima di eliminarlo. In questo caso, l'uso di **wglDeleteContext** per creare un contesto di rendering non aggiornato richiede che il programmatore elimini o rilasci il contesto di dispositivo associato.

 

 