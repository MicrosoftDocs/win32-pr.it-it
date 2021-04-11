---
title: Contesti di rendering
description: Un contesto di rendering OpenGL è una porta attraverso la quale tutti i comandi di OpenGL passano. Ogni thread che effettua chiamate OpenGL deve avere un contesto di rendering corrente. I contesti di rendering collegano OpenGL ai sistemi Windows windowing.
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- OpenGL per Windows, contesti di rendering
- rendering di contesti OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac2ac6c5948da2b7372d600377666cd9e4e074
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330983"
---
# <a name="rendering-contexts"></a>Contesti di rendering

Un *contesto di rendering* OpenGL è una porta attraverso la quale tutti i comandi di OpenGL passano. Ogni thread che effettua chiamate OpenGL deve avere un contesto di rendering corrente. I contesti di rendering collegano OpenGL ai sistemi Windows windowing.

Un'applicazione specifica un contesto di dispositivo Windows quando crea un contesto di rendering. Questo contesto di rendering è adatto per il disegno sul dispositivo a cui fa riferimento il contesto di dispositivo specificato. In particolare, il contesto di rendering ha lo stesso formato pixel del contesto di dispositivo. Per altre informazioni, vedere [rendering delle funzioni di contesto](rendering-context-functions.md).

Nonostante questa relazione, un contesto di rendering non corrisponde a un contesto di dispositivo. Un contesto di dispositivo contiene informazioni pertinenti al componente grafico (GDI) di Windows. Un contesto di rendering contiene informazioni pertinenti per OpenGL. Un contesto di dispositivo deve essere specificato in modo esplicito in una chiamata GDI. Un contesto di rendering è implicito in una chiamata OpenGL. È necessario impostare il formato pixel di un contesto di dispositivo prima di creare un contesto di rendering.

Un thread che effettua chiamate OpenGL deve avere un contesto di rendering corrente. Se un'applicazione effettua chiamate OpenGL da un thread che non dispone di un contesto di rendering corrente, non viene eseguita alcuna operazione; la chiamata non ha alcun effetto. Un'applicazione crea in genere un contesto di rendering, la imposta come contesto di rendering corrente del thread e quindi chiama le funzioni OpenGL. Al termine della chiamata alle funzioni OpenGL, l'applicazione separa il contesto di rendering dal thread, quindi Elimina il contesto di rendering. Una finestra può includere più contesti di rendering contemporaneamente, ma un thread può avere un solo contesto di rendering attivo e corrente.

A un contesto di rendering corrente è associato un contesto di dispositivo. Il contesto di dispositivo non deve corrispondere allo stesso contesto di dispositivo usato durante la creazione del contesto di rendering, ma deve fare riferimento allo stesso dispositivo e avere lo stesso formato pixel.

Un thread può avere un solo contesto di rendering corrente. Un contesto di rendering può essere aggiornato a un solo thread.

 

 




