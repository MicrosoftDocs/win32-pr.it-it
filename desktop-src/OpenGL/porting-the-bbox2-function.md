---
title: Porting della funzione bbox2
description: Non esiste un equivalente OpenGL per la funzione Bbox2 IRIS GL.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- Porting IRIS GL,funzione bbox2
- porting da IRIS GL,funzione bbox2
- porting a OpenGL da IRIS GL,funzione bbox2
- Porting OpenGL da IRIS GL,funzione bbox2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f34bc9035e9aa9fac884a14946a0593cb70702cf19f22d5d4c82011b58077e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012009"
---
# <a name="porting-the-bbox2-function"></a>Porting della funzione bbox2

Non esiste un equivalente OpenGL per la funzione **Bbox2** IRIS GL.

**Per eseguire la porta del codice che contiene le funzioni bbox2**

1.  Creare un nuovo elenco di visualizzazione (OpenGL) contenente tutti gli elementi nell'elenco di visualizzazione IRIS GL equivalente, ad eccezione della chiamata a **bbox2**.
2.  Usare il Windows codice appropriato per disegnare un rettangolo delle stesse dimensioni della **bbox** IRIS GL.

 

 




