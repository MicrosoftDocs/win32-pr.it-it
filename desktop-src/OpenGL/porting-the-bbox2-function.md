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
# <a name="porting-the-bbox2-function"></a><span data-ttu-id="92259-107">Porting della funzione bbox2</span><span class="sxs-lookup"><span data-stu-id="92259-107">Porting the bbox2 Function</span></span>

<span data-ttu-id="92259-108">Non esiste un equivalente OpenGL per la funzione **bbox2** di Iris GL.</span><span class="sxs-lookup"><span data-stu-id="92259-108">There is no OpenGL equivalent for the IRIS GL **bbox2** function.</span></span>

<span data-ttu-id="92259-109">**Per trasferire il codice che contiene funzioni bbox2**</span><span class="sxs-lookup"><span data-stu-id="92259-109">**To port code that contains bbox2 functions**</span></span>

1.  <span data-ttu-id="92259-110">Creare un nuovo elenco di visualizzazione (OpenGL) contenente tutti gli elementi dell'elenco di visualizzazione di IRIS GL equivalenti, ad eccezione della chiamata a **bbox2**.</span><span class="sxs-lookup"><span data-stu-id="92259-110">Create a new (OpenGL) display list that contains everything in the equivalent IRIS GL display list except the call to **bbox2**.</span></span>
2.  <span data-ttu-id="92259-111">Usare il codice di Windows appropriato per creare un rettangolo con le stesse dimensioni del **Bbox** IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="92259-111">Use appropriate Windows code to draw a rectangle the same size as the IRIS GL **bbox**.</span></span>

 

 




