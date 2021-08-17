---
title: Porting delle chiamate al piano stencil
description: In OpenGL si allocano piani stencil richiedendo il formato pixel appropriato con OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Portabilità IRIS GL, piani stencil
- porting from IRIS GL,stencil planes
- porting to OpenGL from IRIS GL,stencil planes
- Porting OpenGL da IRIS GL, stencil planes
- piani stencil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d2c9ea8a9c025c06f179b51cab1301f8ff871740576a6c9e28cdfc1f15ad3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485391"
---
# <a name="porting-stencil-plane-calls"></a>Porting delle chiamate al piano stencil

In OpenGL si allocano piani stencil richiedendo il formato pixel appropriato con OpenGL **auxInitDisplayMode** o [**ChoosePixelFormat.**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) Funzioni. La tabella seguente elenca le funzioni IRIS GL che influiscono sui piani degli stencil e sulle funzioni OpenGL equivalenti.



| Funzione GL IRIS             | Funzione OpenGL                                         | Significato                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **stensize**                 | **ChoosePixelFormat**                                   |                                                        |
| **stencil**( **TRUE**, ... ) | [**glEnable**](glenable.md) ( GL \_ STENCIL \_ TEST )      | Abilita i test degli stencil.                                 |
| **Stencil**                  | [**glStencilOp**](glstencilop.md)                      | Imposta le azioni di test degli stencil.                             |
| **stencil**(... func, ... )  | [**glStencilFunc**](glstencilfunc.md)                  | Imposta la funzione e il valore di riferimento per il test degli stencil. |
| **swritemask**               | [**glStencilMask**](glstencilmask.md)                  | Specifica quali bit degli stencil possono essere scritti.           |
|                              | [**glClearStencil**](glclearstencil.md)                | Specifica il valore non crittografato per il buffer degli stencil.      |
| **sclear**                   | [**glClear**](glclear.md) ( GL \_ STENCIL BUFFER BIT \_ \_ ) |                                                        |



 

Le funzioni di confronto degli stencil e le operazioni di passaggio/errore degli stencil sono quasi equivalenti in OpenGL e IRIS GL. I flag della funzione di stencil IRIS GL sono preceduti da SF; i flag OpenGL con GL. I flag di operazione pass/fail IRIS GL sono preceduti da ST; i flag OpenGL con GL.

 

 




