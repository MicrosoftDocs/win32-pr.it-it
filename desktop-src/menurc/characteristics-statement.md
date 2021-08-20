---
title: Istruzione CHARACTERISTICS
description: Definisce le informazioni su una risorsa che possono essere usate dagli strumenti che leggono e scrivono file di definizione delle risorse.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Istruzione CHARACTERISTICS Menu e altre risorse
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9910a86263d14dd928fb01347dfea4fd6c796c23b4e5d42d69cdba4bc40e14c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034315"
---
# <a name="characteristics-statement"></a>Istruzione CHARACTERISTICS

Definisce le informazioni su una risorsa che possono essere usate dagli strumenti che leggono e scrivono file di definizione delle risorse. Il valore **DWORD** specificato viene visualizzato con la risorsa nel file con estensione res compilato. Tuttavia, il valore non viene archiviato nel file eseguibile e non ha alcun significato per il sistema.

**L'istruzione CHARACTERISTICS** viene visualizzata prima dell'inizio del corpo di una definizione di risorsa [**ACCELERATORS**](accelerators-resource.md), [**DIALOG**](dialog-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**STRINGTABLE.**](stringtable-resource.md) Il valore specificato si applica solo a tale risorsa.

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*Dword*
</dt> <dd>

Valore **DWORD definito dall'utente.**

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Acceleratori**](accelerators-resource.md)
</dt> <dt>

[**Dialogo**](dialog-resource.md)
</dt> <dt>

[**Lingua**](language-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> </dl>

 

 




