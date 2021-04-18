---
title: Macro predefinite
description: RC non supporta le macro predefinite ANSI C ( \_ \_ date \_ \_ , \_ \_ file \_ \_ , \_ \_ line \_ \_ , \_ \_ STDC \_ \_ , \_ \_ time \_ \_ , \_ \_ timestamp \_ \_ ). Di conseguenza, non è possibile includere queste macro nei file di intestazione da includere nello script della risorsa.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116800"
---
# <a name="predefined-macros"></a>Macro predefinite

RC non supporta le macro predefinite ANSI C (**\_ \_ date \_ \_**, **\_ \_ file \_ \_**, **\_ \_ line \_ \_**, **\_ \_ STDC \_ , Time \_** **\_ \_ , timestamp \_ ). \_** **\_ \_ \_ \_** Di conseguenza, non è possibile includere queste macro nei file di intestazione da includere nello script della risorsa.

RC definisce RC \_ richiamato, che consente di compilare in modo condizionale parti dei file di intestazione, a seconda che il compilatore sia il compilatore C o il compilatore RC. Questo è importante perché il compilatore RC supporta solo un subset delle istruzioni supportate da un compilatore C.

Per compilare in modo condizionale il codice con il compilatore RC, racchiudere il codice che RC non può compilare con \# ifndef RC \_ richiamato e **\# endif**.

L'esempio seguente è tratto dagli esempi di SDK. Viene illustrato come creare un file di intestazione che può essere compilato in modo condizionale.

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




