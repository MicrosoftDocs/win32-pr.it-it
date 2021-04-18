---
title: Conversione di texgen
description: Il texgen della funzione IRIS GL viene convertito in glTexGen per OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Porting di IRIS GL, trama
- porting da IRIS GL, trama
- porting in OpenGL da IRIS GL, trama
- Porting OpenGL da IRIS GL, trama
- trama
- Porting di IRIS GL, texgen
- porting da IRIS GL, texgen
- porting in OpenGL da IRIS GL, texgen
- Porting OpenGL da IRIS GL, texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298813"
---
# <a name="translating-texgen"></a>Conversione di texgen

Il **texgen** della funzione IRIS GL viene convertito in [glTexGen](gltexgen-functions.md) per OpenGL.

Con IRIS GL, si chiama **texgen** due volte: una volta per impostare la modalità e l'equazione del piano contemporaneamente e una volta per abilitare la generazione della coordinata della trama. Ad esempio:


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



Con OpenGL si effettuano tre chiamate: due a **glTexGen** (una volta per impostare la modalità e una volta per impostare l'equazione del piano) e una a [**glEnable**](glenable.md). Ad esempio, l'equivalente OpenGL al codice IRIS GL precedente è:


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



La tabella seguente elenca i nomi delle coordinate di trama IRIS GL e i rispettivi equivalenti OpenGL.



| Coordinata di trama IRIS GL | Coordinata trama OpenGL | argomento glEnable   |
|----------------------------|---------------------------|---------------------|
| TX \_ S                      | GL \_ S                     | \_generazione trama \_ GL \_ |
| TX \_ T                      | GL \_ T                     | \_gen trama \_ GL \_ T |
| TX \_ R                      | GL \_ R                     | \_generazione trama \_ GL \_ R |
| TX \_ Q                      | GL \_ Q                     | \_generazione trama \_ GL \_ Q |



 

La tabella seguente elenca le modalità di generazione della trama di IRIS GL e le modalità di trama OpenGL equivalenti e i nomi dei piani.



| Modalità trama di IRIS GL | Modalità trama OpenGL | Nome del piano OpenGL |
|----------------------|---------------------|-------------------|
| TG \_ lineare           | \_oggetto GL \_ lineare  | \_piano oggetto \_ GL |
| \_profilo TG          | GL \_ occhio \_ lineare     | \_piano d'occhio GL \_    |
| \_SPHEREMAP TG        | \_mappa della sfera GL \_     |                   |



 

 

 




