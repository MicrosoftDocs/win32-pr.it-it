---
title: Macro predefinite
description: RC non supporta le macro predefinite C ANSI ( \_ \_ DATE , FILE \_ \_ , LINE \_ \_ \_ \_ , \_ \_ \_ \_ \_ \_ STDC \_ \_ , TIME , \_ \_ \_ \_ \_ \_ TIMESTAMP \_ \_ ). Pertanto, non è possibile includere queste macro nei file di intestazione che verranno inclusi nello script della risorsa.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9e48b915fae430bf776b9eebab7ac795e7b69a3d79e06a7ce6422b6d6eab6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971950"
---
# <a name="predefined-macros"></a>Macro predefinite

RC non supporta le macro predefinite C ANSI (**\_ \_ DATE \_ \_**, **\_ \_ \_ \_ FILE**, **\_ \_ LINE \_ \_**, **\_ \_ STDC \_ \_**, **\_ \_ TIME \_ \_**, **\_ \_ TIMESTAMP \_ \_**). Pertanto, non è possibile includere queste macro nei file di intestazione che verranno inclusi nello script della risorsa.

RC definisce RC INVOKED, che consente di compilare in modo condizionale parti dei file di intestazione, a seconda che il compilatore sia il compilatore C o \_ il compilatore RC. Questo è importante perché il compilatore RC supporta solo un subset delle istruzioni supportate da un compilatore C.

Per compilare in modo condizionale il codice con il compilatore RC, racchiudere il codice che RC non può compilare con \# ifndef RC \_ INVOKED **\# ed endif**.

L'esempio seguente è tratto dagli esempi sdk. Illustra come creare un file di intestazione che può essere compilato in modo condizionale.

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




