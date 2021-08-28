---
title: Contesti di rendering
description: Un contesto di rendering OpenGL è una porta attraverso la quale passano tutti i comandi OpenGL. Ogni thread che esegue chiamate OpenGL deve avere un contesto di rendering corrente. I contesti di rendering collegano OpenGL ai Windows windowing.
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- OpenGL in Windows,contesti di rendering
- contesti di rendering OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51167161662501f8aaaca6a392b2efc84217be139842c343056746abf0c35161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011949"
---
# <a name="rendering-contexts"></a>Contesti di rendering

Un contesto di *rendering* OpenGL è una porta attraverso la quale passano tutti i comandi OpenGL. Ogni thread che esegue chiamate OpenGL deve avere un contesto di rendering corrente. I contesti di rendering collegano OpenGL ai Windows windowing.

Un'applicazione specifica un contesto Windows di dispositivo quando crea un contesto di rendering. Questo contesto di rendering è adatto per disegnare sul dispositivo a cui fa riferimento il contesto di dispositivo specificato. In particolare, il contesto di rendering ha lo stesso formato pixel del contesto di dispositivo. Per altre informazioni, vedere Funzioni del [contesto di rendering](rendering-context-functions.md).

Nonostante questa relazione, un contesto di rendering non corrisponde a un contesto di dispositivo. Un contesto di dispositivo contiene informazioni pertinenti al componente grafico (GDI) di Windows. Un contesto di rendering contiene informazioni pertinenti a OpenGL. Un contesto di dispositivo deve essere specificato in modo esplicito in una chiamata GDI. Un contesto di rendering è implicito in una chiamata OpenGL. È necessario impostare il formato pixel di un contesto di dispositivo prima di creare un contesto di rendering.

Un thread che esegue chiamate OpenGL deve avere un contesto di rendering corrente. Se un'applicazione esegue chiamate OpenGL da un thread che non dispone di un contesto di rendering corrente, non accade nulla; la chiamata non ha alcun effetto. Un'applicazione crea in genere un contesto di rendering, lo imposta come contesto di rendering corrente di un thread e quindi chiama funzioni OpenGL. Al termine della chiamata alle funzioni OpenGL, l'applicazione scollega il contesto di rendering dal thread e quindi elimina il contesto di rendering. Una finestra può avere più contesti di rendering contemporaneamente, ma un thread può avere un solo contesto di rendering attivo corrente.

A un contesto di rendering corrente è associato un contesto di dispositivo. Tale contesto di dispositivo non deve essere lo stesso contesto di dispositivo usato al momento della creazione del contesto di rendering, ma deve fare riferimento allo stesso dispositivo e avere lo stesso formato pixel.

Un thread può avere un solo contesto di rendering corrente. Un contesto di rendering può essere corrente solo per un thread.

 

 




