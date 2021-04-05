---
title: /syntax_check opzione
description: L' \_ opzione di controllo/Syntax indica che il compilatore controlla solo la sintassi e non genera file di output.
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check switch MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718478"
---
# <a name="syntax_check-switch"></a>\_opzione di controllo/Syntax

L'opzione di **\_ controllo/Syntax** indica che il compilatore controlla solo la sintassi e non genera file di output.

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Questa opzione esegue l'override di tutte le altre opzioni che specificano le informazioni sui file di output.

È anche possibile specificare la modalità di controllo della sintassi con l'opzione del compilatore MIDL [**/ZS**](-zs.md).

## <a name="examples"></a>Esempio

**MIDL/ZS nomefile. idl**

**MIDL/Syntax \_ controllare filename. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ZS**](-zs.md)
</dt> </dl>

 

 




