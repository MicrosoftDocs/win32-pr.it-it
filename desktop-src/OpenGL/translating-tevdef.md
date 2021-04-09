---
title: Conversione di tevdef
description: L'esempio di codice seguente è una definizione dell'ambiente di trama di IRIS GL che specifica il \_ parametro di trama-ambiente delle decalcomanie TV
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Porting di IRIS GL, trama
- porting da IRIS GL, trama
- porting in OpenGL da IRIS GL, trama
- Porting OpenGL da IRIS GL, trama
- trama
- Porting di IRIS GL, tevdef
- porting da IRIS GL, tevdef
- porting in OpenGL da IRIS GL, tevdef
- Porting OpenGL da IRIS GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955786"
---
# <a name="translating-tevdef"></a>Conversione di tevdef

L'esempio di codice seguente è una definizione dell'ambiente di trama di IRIS GL che specifica il \_ parametro di trama-ambiente delle decalcomanie TV:


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



e lo stesso codice è stato convertito in OpenGL:


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



La tabella seguente elenca i parametri dell'ambiente di trama di IRIS GL e i parametri OpenGL equivalenti.



| Parametro di IRIS GL     | Parametro OpenGL             |
|-----------------------|------------------------------|
| \_modulazione TV          | \_modulazione GL                 |
| \_decalcomania TV             | \_decalcomania GL                    |
| \_Blend TV             | \_Blend GL                    |
| \_colore TV             | \_ \_ colore ENV trama \_ GL      |
| TV \_ Alpha             | Nessun equivalente OpenGL diretto. |
| \_selezione componente \_ TV | Nessun equivalente OpenGL diretto. |



 

Per ulteriori informazioni sui parametri dell'ambiente di trama, vedere [**glTexEnv**](gltexenv-functions.md).

 

 




