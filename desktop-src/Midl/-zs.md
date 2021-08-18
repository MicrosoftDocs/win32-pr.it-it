---
title: Opzione /Zs
description: L'opzione /Zs indica che il compilatore controlla solo la sintassi e non genera file di output.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- Opzione /Zs MIDL
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92bd2321567bbc565d3198fe5ebf5c98a3d8df440ea967409830c8e73488609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014019"
---
# <a name="zs-switch"></a>Opzione /Zs

**L'opzione /Zs** indica che il compilatore controlla solo la sintassi e non genera file di output.

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Questa opzione sostituisce tutte le altre opzioni che specificano informazioni sui file di output.

È anche possibile specificare la modalità di controllo della sintassi con l'opzione del compilatore MIDL [**/syntax \_ check**](-syntax-check.md).

## <a name="examples"></a>Esempio

**midl /Zs filename.idl**

**midl /syntax \_ check filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/syntax \_ check**](-syntax-check.md)
</dt> </dl>

 

 




