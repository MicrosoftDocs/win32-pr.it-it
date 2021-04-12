---
title: Generazione di coordinate di trama
description: Anziché specificare in modo esplicito le coordinate di trama, è possibile fare in modo che OpenGL le generi come funzione di altri dati del vertice usando glTexGen \.
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- Pipeline di elaborazione OpenGL, coordinate di trama
- Coordinate di trama OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d3f5b807f25aee2783ff8dab3a4930a9c797ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221653"
---
# <a name="generating-texture-coordinates"></a>Generazione di coordinate di trama

Anziché specificare in modo esplicito le coordinate di trama, è possibile fare in modo che OpenGL le generi come funzione di altri dati del vertice usando [glTexGen \* ](gltexgen-functions.md). Una volta specificate o generate le coordinate di trama, vengono trasformate dalla matrice di trame. Questa matrice viene controllata con le stesse funzioni usate per le trasformazioni di matrici (vedere [trasformazioni matrici](matrix-transformations.md)).

 

 




