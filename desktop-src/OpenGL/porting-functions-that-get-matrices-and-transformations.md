---
title: Funzioni di portabilità che ottengono matrici e trasformazioni
description: La tabella seguente elenca le funzioni IRIS GL che ottengono lo stato delle matrici e delle trasformazioni e i relativi equivalenti OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- portabilità IRIS GL, matrici
- porting from IRIS GL,matrici
- porting to OpenGL from IRIS GL,matrici
- Portabilità OpenGL da IRIS GL, matrici
- matrici
- portabilità IRIS GL, trasformazioni
- porting from IRIS GL,transformations
- porting to OpenGL from IRIS GL,transformations
- Porting OpenGL da IRIS GL, trasformazioni
- trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68eed8722d982d8d93f47f4d2dc02b8f0f97d9c58512400353ab068015455e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776971"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a>Funzioni di portabilità che ottengono matrici e trasformazioni

La tabella seguente elenca le funzioni IRIS GL che ottengono lo stato delle matrici e delle trasformazioni e i relativi equivalenti OpenGL.



| Query matrice IRIS GL                  | Query matrice GlGet OpenGL         | Significato                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| **getmmode**                          | MODALITÀ MATRICE GL \_ \_                  | Restituisce la modalità matrice corrente.                                |
| **getmatrix** in **modalità MVIEWING**    | MATRICE \_ DI MODELVIEW \_ GL             | Restituisce una copia della matrice di visualizzazione del modello corrente.                |
| **getmatrix** in **modalità MPROJECTION** | MATRICE DI \_ \_ PROIEZIONE GL            | Restituisce una copia della matrice di proiezione corrente.                |
| **getmatrix** in **modalità MTEXTURE**    | MATRICE DI TRAMA GL \_ \_               | Restituisce una copia della matrice di trama corrente.                   |
| Non applicabile.                       | GL \_ MAX \_ MODELVIEW \_ STACK \_ DEPTH  | Restituisce la profondità massima supportata dello stack della matrice di visualizzazione del modello. |
| Non applicabile.                       | GL \_ MAX \_ PROJECTION \_ STACK \_ DEPTH | Restituisce la profondità massima supportata dello stack della matrice di proiezione. |
| Non applicabile.                       | GL \_ MAX \_ TEXTURE \_ STACK \_ DEPTH    | Restituisce la profondità massima supportata dello stack della matrice di trame.    |
| Non applicabile.                       | GL \_ MODELVIEW \_ STACK \_ DEPTH       | Restituisce il numero di matrici nello stack di visualizzazione del modello.             |
| Non applicabile.                       | GL \_ PROJECTION \_ STACK \_ DEPTH      | Restituisce il numero di matrici nello stack di proiezione.             |
| Non applicabile.                       | GL \_ TEXTURE \_ STACK \_ DEPTH         | Restituisce il numero di matrici nello stack di trame.                |



 

??

 

 




