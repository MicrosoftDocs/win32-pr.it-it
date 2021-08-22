---
title: Nomi delle funzioni OpenGL
description: Molte funzioni OpenGL sono varianti l'una dell'altra, che differiscono principalmente per i tipi di dati dei relativi argomenti.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, nomi di funzione
- nomi di funzione OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7729ca1f8a092c261a2ae87a835b51ea253ff2d09de710a830458c0825642bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936881"
---
# <a name="opengl-function-names"></a>Nomi delle funzioni OpenGL

Molte funzioni OpenGL sono varianti l'una dell'altra, che differiscono principalmente per i tipi di dati dei relativi argomenti. Alcune funzioni differiscono per il numero di argomenti correlati e se tali argomenti possono essere specificati come vettore o devono essere specificati separatamente in un elenco. Ad esempio, se si usa la **funzione glVertex2f,** è necessario fornire le coordinate x e y come numeri a virgola mobile a 32 bit; con **glVertex3sv**, è necessario fornire una matrice di tre valori interi brevi (a 16 bit) per x, y e z. Negli argomenti seguenti viene usato solo il nome di base della funzione. Un asterisco indica che il nome effettivo della funzione potrebbe essere maggiore di quello visualizzato. [ \* GlVertex,](glvertex-functions.md) ad esempio, è l'acronimo di tutte le varianti della funzione che si usa per specificare i vertici: **glVertex2d**, **glVertex2f**, **glVertex2i** e così via.

L'effetto di una funzione OpenGL può variare a seconda che siano abilitate determinate modalità. Ad esempio, è necessario abilitare l'illuminazione se le funzioni correlate all'illuminazione devono produrre un oggetto correttamente acceso. Per abilitare una particolare modalità, usare la funzione [**glEnable**](glenable.md) e specificare la costante appropriata per identificare la modalità (ad esempio, GL \_ LIGHTING). Per disabilitare una modalità, [**usare glDisable.**](gldisable.md) Vedere **glEnable per** un elenco completo delle modalità che possono essere abilitate.

 

 




