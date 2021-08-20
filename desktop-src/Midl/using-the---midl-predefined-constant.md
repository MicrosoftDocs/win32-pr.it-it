---
title: Uso della __midl costante predefinita
description: Quando il compilatore MIDL elabora i file IDL e ACF di input, midl viene definito per impostazione predefinita e viene usato per la compilazione condizionale per ottenere coerenza in tutta \_ \_ la compilazione.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL del compilatore MIDL, usando _midl costante predefinita
- _midl costante predefinita MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fbc111ad07839d891f7bdffaf7ecaae83fbf277a0fc2c93fc483f526f9dda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382822"
---
# <a name="using-the-__midl-predefined-constant"></a>Uso della \_ \_ costante predefinita midl

Quando il compilatore MIDL elabora i file IDL e ACF di input, midl viene definito per impostazione predefinita e viene usato per la compilazione condizionale per ottenere coerenza in tutta \_ \_ la compilazione. In questo modo viene gradualmente definito l'uso di istruzioni define nei file di intestazione, ad esempio **MIDL \_ PASS,** e vengono sostituite con un flag coerente. Il valore della costante midl indica la versione del compilatore \_ \_ *major.minor* in base alla formula *major* \* 100 + *minor,* ad esempio MIDL ver. 6.0.x ha \_ \_ il valore midl definito come 600.

Se si sceglie , è possibile eseguire l'override di questa impostazione predefinita specificando quanto segue nella riga di comando: **/U \_ \_ midl**. Per altre informazioni, vedere [**/U**](-u.md).

 

 




