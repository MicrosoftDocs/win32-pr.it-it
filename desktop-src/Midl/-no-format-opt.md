---
title: Opzione /no_format_opt
description: L'opzione /no \_ format opt modifica il modo in cui \_ MIDL ottimizza i descrittori di tipo e routine.
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- Opzione /no_format_opt MIDL
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93753d1aa73d378ff093cf2d315e144461f466a42910e1778060be05defb911a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014139"
---
# <a name="no_format_opt-switch"></a>Opzione /no \_ format \_ opt

**L'opzione /no \_ format \_ opt** modifica il modo in cui MIDL ottimizza i descrittori di tipo e routine.

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, MIDL elimina i descrittori di tipo e routine duplicati per ridurre le dimensioni del codice stub generato. **L'uso dell'opzione /no \_ format \_ opt** disattiva questo comportamento di ottimizzazione.

## <a name="examples"></a>Esempio

**midl /no \_ format \_ opt mylean.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/oi**](-oi.md)
</dt> </dl>

 

 




