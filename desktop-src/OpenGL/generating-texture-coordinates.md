---
title: Generazione di coordinate di trama
description: Anziché fornire in modo esplicito le coordinate di trama, è possibile fare in modo che OpenGL le generi come funzione di altri dati dei vertici usando glTexGen\ .
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- Pipeline di elaborazione OpenGL, coordinate di trama
- Coordinate della trama OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e7b6bc2d1263fac046f2d3078e2bab9bf8a789cacb335137ba27443b12b89d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082281"
---
# <a name="generating-texture-coordinates"></a>Generazione di coordinate di trama

Anziché fornire in modo esplicito le coordinate di trama, è possibile fare in modo che OpenGL le generi come funzione di altri dati dei vertici usando [glTexGen \* ](gltexgen-functions.md). Dopo che le coordinate della trama sono state specificate o generate, vengono trasformate dalla matrice di trama. Questa matrice è controllata con le stesse funzioni usate per le trasformazioni di matrice (vedere [Trasformazioni di matrice](matrix-transformations.md)).

 

 




