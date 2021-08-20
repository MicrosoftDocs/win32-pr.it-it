---
title: Porting di oggetti NURBS
description: OpenGL considera NURBS come oggetti, in modo analogo al modo in cui considera i quadric quando si crea un oggetto NURBS e quindi si specifica come deve essere eseguito il rendering. Nella tabella seguente sono elencate le funzioni GLU OpenGL per la gestione degli oggetti NURBS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Porting IRIS GL, oggetti NURBS
- porting da oggetti IRIS GL,NURBS
- porting in OpenGL da oggetti IRIS GL,NURBS
- Porting OpenGL da oggetti IRIS GL,NURBS
- Oggetti NURBS
- NURBS (B-Spline razionale non uniforme)
- B-Spline razionale non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6990d2292399cb1ccaf00ba6ec42d680c5ace887b2495daf8640db2da30ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132410"
---
# <a name="porting-nurbs-objects"></a>Porting di oggetti NURBS

OpenGL considera NURBS come oggetti, in modo analogo al modo in cui tratta i quadrics: si crea un oggetto NURBS e quindi si specifica come deve essere eseguito il rendering. Nella tabella seguente sono elencate le funzioni GLU OpenGL per la gestione degli oggetti NURBS.



| Funzione GLU OpenGL                                      | Significato                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)       | Crea un nuovo oggetto NURBS.                                    |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) | Elimina un oggetto NURBS.                                        |
| [*gluNurbsCallback*](glunurbs.md)                       | Associa un callback a un oggetto NURBS per la gestione degli errori. |



 

Quando si esegue il porting del codice NURBS IRIS GL in OpenGL, tenere presenti i punti seguenti:

-   I punti di controllo NURBS sono float, non double.
-   Il parametro stride viene conteggiato in float, non in byte.
-   Se si usa l'illuminazione e non si specificano le normali, chiamare [**glEnable**](glenable.md) con GL AUTO NORMAL come parametro per generare \_ \_ automaticamente le normali.

??

 

 




