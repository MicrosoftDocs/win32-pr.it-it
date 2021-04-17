---
title: IDXCoreAdapterList::IsStale
description: Determina se le modifiche apportate a questo sistema hanno causato la mancata visualizzazione dell'oggetto elenco di adapter DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300376"
---
# <a name="idxcoreadapterlistisstale-method"></a>Metodo IDXCoreAdapterList:: IsValid

Determina se le modifiche apportate a questo sistema hanno causato la mancata visualizzazione dell'oggetto elenco di adapter DXCore. Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce  `true`   se, dall'inizio della generazione dell'elenco, sono state apportate modifiche alle condizioni di sistema che potrebbero rendere obsoleto questo elenco di adapter. In caso contrario, restituisce  `false` .

## <a name="remarks"></a>Commenti

È possibile eseguire **il polling** per determinare se le condizioni di sistema modificate hanno portato a questo elenco non aggiornato. Se il risultato è **obsoleto** `true` , viene restituito `true` per la durata rimanente dell'oggetto elenco di adapter dxcore. Un oggetto elenco non aggiornato è ancora considerato obsoleto anche se le condizioni di sistema tornano a uno stato che corrisponde all'elenco (le stesse condizioni ottengono ora come è stato fatto quando l'elenco è stato generato per la prima volta).

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)