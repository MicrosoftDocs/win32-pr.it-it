---
title: Traduzione di tevdef
description: L'esempio di codice seguente è una definizione dell'ambiente di trama IRIS GL che specifica il parametro \_ tv DECAL texture-environment
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- portabilità IRIS GL, trama
- porting from IRIS GL,texture
- porting to OpenGL from IRIS GL,texture
- Portabilità OpenGL da IRIS GL, trama
- trama
- Portabilità IRIS GL, tevdef
- porting from IRIS GL,tevdef
- porting to OpenGL from IRIS GL,tevdef
- Portabilità OpenGL da IRIS GL,tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7feef33c2aa725c6e5bb91782fe43fdc6a84d23db8aa412f02c07b6ec588f719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887881"
---
# <a name="translating-tevdef"></a>Traduzione di tevdef

L'esempio di codice seguente è una definizione dell'ambiente di trama IRIS GL che specifica il parametro \_ tv DECAL texture-environment:


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



e lo stesso codice convertito in OpenGL:


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



La tabella seguente elenca i parametri dell'ambiente di trama IRIS GL e i relativi parametri OpenGL equivalenti.



| Parametro IRIS GL     | Parametro OpenGL             |
|-----------------------|------------------------------|
| TV \_ MODULATE          | GL \_ MODULATE                 |
| TV \_ DECAL             | GL \_ DECAL                    |
| TV \_ BLEND             | GL \_ BLEND                    |
| COLORE \_ TV             | COLORE \_ DELL'AMBIENTE \_ TRAMA GL \_      |
| TV \_ ALPHA             | Nessun equivalente OpenGL diretto. |
| SELEZIONE \_ COMPONENTE \_ TV | Nessun equivalente OpenGL diretto. |



 

Per altre informazioni sui parametri dell'ambiente di trama, [**vedere glTexEnv.**](gltexenv-functions.md)

 

 




