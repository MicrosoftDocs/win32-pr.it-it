---
title: IDXCoreAdapterList::IsStale
description: Determina se le modifiche apportate a questo sistema hanno comportato la scadenza dell'oggetto elenco di adattatori DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a40a590a76773592d5442993c75149b2349880f7681d625e777d363062f5c4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502572"
---
# <a name="idxcoreadapterlistisstale-method"></a>Metodo IDXCoreAdapterList::IsStale

Determina se le modifiche apportate a questo sistema hanno comportato la scadenza dell'oggetto elenco di adattatori DXCore. Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce se, dopo la generazione dell'elenco, si sono verificate modifiche alle condizioni di sistema che potrebbero far sì che l'elenco `true` di adattatori diventi obsoleto. In caso contrario, restituisce `false`.

## <a name="remarks"></a>Commenti

È possibile eseguire il **polling di IsStale** per determinare se la modifica delle condizioni di sistema ha portato a un elenco non aggiornato. Se **IsStale restituisce una** sola `true` volta, restituisce per la durata `true` rimanente dell'oggetto elenco di adattatori DXCore. Un oggetto elenco non obsoleto viene comunque considerato obsoleto anche se le condizioni di sistema tornano a uno stato corrispondente all'elenco (le stesse condizioni si ottengono ora come quando l'elenco è stato generato per la prima volta).

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)