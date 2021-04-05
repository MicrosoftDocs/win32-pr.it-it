---
title: Funzioni di porting che ottengono matrici e trasformazioni
description: La tabella seguente elenca le funzioni di IRIS GL che ottengono lo stato delle matrici e delle trasformazioni e dei rispettivi equivalenti OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Porting di IRIS GL, matrici
- porting da IRIS GL, matrici
- porting in OpenGL da IRIS GL, matrici
- Porting OpenGL da IRIS GL, matrici
- matrici
- Porting, trasformazioni di IRIS GL
- porting da IRIS GL, trasformazioni
- porting in OpenGL da IRIS GL, trasformazioni
- Porting OpenGL da IRIS GL, trasformazioni
- trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955576"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a>Funzioni di porting che ottengono matrici e trasformazioni

La tabella seguente elenca le funzioni di IRIS GL che ottengono lo stato delle matrici e delle trasformazioni e dei rispettivi equivalenti OpenGL.



| Query matrice GL IRIS                  | Query della matrice glGet OpenGL         | Significato                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| **getmmode**                          | \_modalità matrice \_ GL                  | Restituisce la modalità della matrice corrente.                                |
| **getMatrix** in modalità **MVIEWING**    | \_matrice GL MODELVIEW \_             | Restituisce una copia della matrice di visualizzazione modello corrente.                |
| **getMatrix** in modalità **MPROJECTION** | \_matrice di proiezione GL \_            | Restituisce una copia della matrice di proiezione corrente.                |
| **getMatrix** in modalità **MTEXTURE**    | \_matrice di trama GL \_               | Restituisce una copia della matrice di trama corrente.                   |
| Non applicabile.                       | \_ \_ \_ profondità dello stack MODELVIEW max per GL \_  | Restituisce la profondità massima supportata dello stack della matrice di visualizzazione del modello. |
| Non applicabile.                       | \_ \_ \_ profondità dello stack di proiezione max GL \_ | Restituisce la profondità massima supportata dello stack della matrice di proiezione. |
| Non applicabile.                       | \_ \_ \_ profondità stack trama massimo \_ GL    | Restituisce la profondità massima supportata dello stack della matrice di trame.    |
| Non applicabile.                       | \_ \_ profondità dello stack MODELVIEW GL \_       | Restituisce il numero di matrici nello stack della visualizzazione del modello.             |
| Non applicabile.                       | \_ \_ profondità dello stack di proiezione GL \_      | Restituisce il numero di matrici nello stack di proiezione.             |
| Non applicabile.                       | \_ \_ profondità dello stack di trama GL \_         | Restituisce il numero di matrici nello stack di trame.                |



 

??

 

 




