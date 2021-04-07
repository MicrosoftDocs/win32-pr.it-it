---
title: Opzione/ZS
description: L'opzione/ZS indica che il compilatore controlla solo la sintassi e non genera file di output.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- /ZS switch MIDL
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469802434d54319aa55c1e409ccb8d64e942836f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718163"
---
# <a name="zs-switch"></a>Opzione/ZS

L'opzione **/ZS** indica che il compilatore controlla solo la sintassi e non genera file di output.

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Questa opzione esegue l'override di tutte le altre opzioni che specificano le informazioni sui file di output.

È anche possibile specificare la modalità di controllo della sintassi con il [**\_ controllo/Syntax**](-syntax-check.md)dell'opzione del compilatore MIDL.

## <a name="examples"></a>Esempio

**MIDL/ZS nomefile. idl**

**MIDL/Syntax \_ controllare filename. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**\_controllo/Syntax**](-syntax-check.md)
</dt> </dl>

 

 




