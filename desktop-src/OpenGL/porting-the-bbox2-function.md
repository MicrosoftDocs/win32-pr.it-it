---
title: Porting della funzione bbox2
description: Non esiste un equivalente OpenGL per la funzione bbox2 di IRIS GL.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- Porting di IRIS GL, funzione bbox2
- porting da IRIS GL, funzione bbox2
- porting in OpenGL da IRIS GL, funzione bbox2
- Porting OpenGL da IRIS GL, funzione bbox2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21060b8a11ccd6c44297c8b533bca98d79cc00f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712499"
---
# <a name="porting-the-bbox2-function"></a>Porting della funzione bbox2

Non esiste un equivalente OpenGL per la funzione **bbox2** di Iris GL.

**Per trasferire il codice che contiene funzioni bbox2**

1.  Creare un nuovo elenco di visualizzazione (OpenGL) contenente tutti gli elementi dell'elenco di visualizzazione di IRIS GL equivalenti, ad eccezione della chiamata a **bbox2**.
2.  Usare il codice di Windows appropriato per creare un rettangolo con le stesse dimensioni del **Bbox** IRIS GL.

 

 




