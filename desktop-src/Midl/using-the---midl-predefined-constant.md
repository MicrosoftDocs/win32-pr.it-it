---
title: Uso della costante __midl predefinita
description: Quando il compilatore MIDL elabora i file di input IDL e ACF, \_ \_ MIDL viene definito per impostazione predefinita e viene usato per la compilazione condizionale per ottenere la coerenza durante la compilazione.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL Compiler MIDL, uso della _midl costante predefinita
- _midl MIDL costante predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044791"
---
# <a name="using-the-__midl-predefined-constant"></a>Uso della \_ \_ costante predefinita MIDL

Quando il compilatore MIDL elabora i file di input IDL e ACF, \_ \_ MIDL viene definito per impostazione predefinita e viene usato per la compilazione condizionale per ottenere la coerenza durante la compilazione. In questo modo si elimina l'uso di istruzioni define nei file di intestazione, ad esempio il **\_ passaggio MIDL**, e li sostituisce con un flag coerente. Il valore della \_ \_ costante MIDL indica la versione del compilatore *Major. minor* in base alla formula *principale* \* 100 + *minor*, ad esempio MIDL ver. la versione 6.0. x ha il \_ \_ MIDL definito come 600.

Se si sceglie, è possibile eseguire l'override di questa impostazione predefinita specificando quanto segue nella riga di comando: **/u \_ \_ MIDL**. Per ulteriori informazioni, vedere [**/u**](-u.md).

 

 




