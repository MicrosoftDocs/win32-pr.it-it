---
title: Nomi di funzioni OpenGL
description: Molte funzioni OpenGL sono varianti tra loro, in particolare per quanto riguarda i tipi di dati degli argomenti.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, nomi di funzione
- nomi di funzione OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710606"
---
# <a name="opengl-function-names"></a>Nomi di funzioni OpenGL

Molte funzioni OpenGL sono varianti tra loro, in particolare per quanto riguarda i tipi di dati degli argomenti. Alcune funzioni differiscono per il numero di argomenti correlati e se tali argomenti possono essere specificati come vettore o devono essere specificati separatamente in un elenco. Se ad esempio si usa la funzione **glVertex2f** , è necessario fornire le coordinate x e y come numeri a virgola mobile a 32 bit; con **glVertex3sv**, è necessario fornire una matrice di tre valori integer brevi (a 16 bit) per x, y e z. Negli argomenti seguenti viene utilizzato solo il nome di base della funzione. Un asterisco indica che il nome effettivo della funzione può essere maggiore di quello visualizzato. Ad esempio, [glVertex \*](glvertex-functions.md) sta per tutte le varianti della funzione usata per specificare i vertici: **glVertex2d**, **glVertex2f**, **glVertex2i** e così via.

L'effetto di una funzione OpenGL può variare a seconda che determinate modalità siano abilitate. Ad esempio, è necessario abilitare l'illuminazione se le funzioni correlate all'illuminazione devono produrre un oggetto illuminato correttamente. Per abilitare una particolare modalità, usare la funzione [**glEnable**](glenable.md) e fornire la costante appropriata per identificare la modalità (ad esempio, l' \_ illuminazione GL). Per disabilitare una modalità, usare [**glDisable**](gldisable.md). Vedere **glEnable** per un elenco completo delle modalità che è possibile abilitare.

 

 




