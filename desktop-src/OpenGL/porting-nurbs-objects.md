---
title: Porting di oggetti NURBS
description: OpenGL considera NURBS come oggetti, in modo analogo al modo in cui tratta quadriche si crea un oggetto NURBS e quindi si specifica come deve essere eseguito il rendering. La tabella seguente elenca le funzioni OpenGL GLU per la gestione degli oggetti NURBS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Porting di IRIS GL, oggetti NURBS
- porting da IRIS GL, oggetti NURBS
- porting in OpenGL da IRIS GL, oggetti NURBS
- Porting OpenGL da IRIS GL, oggetti NURBS
- Oggetti NURBS
- NURBS (B-spline razionale non uniforme)
- B-spline razionale non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396334"
---
# <a name="porting-nurbs-objects"></a>Porting di oggetti NURBS

OpenGL considera le NURBS come oggetti, in modo analogo al modo in cui tratta quadriche: si crea un oggetto NURBS e quindi si specifica come deve essere eseguito il rendering. La tabella seguente elenca le funzioni OpenGL GLU per la gestione degli oggetti NURBS.



| Funzione OpenGL GLU                                      | Significato                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)       | Crea un nuovo oggetto NURBS.                                    |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) | Elimina un oggetto NURBS.                                        |
| [*gluNurbsCallback*](glunurbs.md)                       | Associa un callback a un oggetto NURBS, per la gestione degli errori. |



 

Quando si esegue il porting del codice NURBS IRIS GL in OpenGL, tenere presente quanto segue:

-   I punti di controllo NURBS sono float, non doppi.
-   Il parametro stride viene conteggiato in float, non in byte.
-   Se si usa l'illuminazione e non si specificano i normali, chiamare [**glEnable**](glenable.md) con GL \_ auto \_ Normal come parametro per generare automaticamente le normali.

??

 

 




