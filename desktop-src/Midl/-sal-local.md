---
title: Opzione /sal_local
description: L'opzione locale /sal indica a MIDL di generare anche annotazioni SAL per i parametri \_ dei metodi di interfaccia contrassegnati come \ local\ . Deve essere presente anche l'opzione /sal.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- Opzione /sal_local MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666401cca482846fc2e6a9d5851a4da9d2d362279c9bc1496ab672a94ac9b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014089"
---
# <a name="sal_local-switch"></a>Opzione \_ locale /sal

**L'opzione \_ locale /sal** indica a MIDL di generare anche annotazioni SAL per i parametri dei metodi di interfaccia contrassegnati come [**\[ local. \]**](local.md) Deve essere presente anche l'opzione [**/sal.**](-sal.md)

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Modifica il comportamento dell'opzione [**/sal**](-sal.md) per fornire anche annotazioni sui parametri dei metodi di interfaccia contrassegnati con [**\[ l'attributo \]**](local.md) locale. Usare [**\[ l'attributo annotate \]**](annotate.md)per eseguire l'override dell'annotazione generata da MIDL con una stringa di annotazione diversa.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[Annotare\]**](annotate.md)
</dt> </dl>

 

 




