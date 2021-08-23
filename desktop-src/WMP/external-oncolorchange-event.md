---
title: Evento External.OnColorChange
description: Nota In questo argomento vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. | Evento External.OnColorChange
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Evento External.OnColorChange Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae4ca15d4d7035fc342fa20263220560570d902e28b9245a6458ac59c40a4f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648751"
---
# <a name="externaloncolorchange-event"></a>Evento External.OnColorChange

> [!Note]  
> Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'evento OnColorChange** si verifica quando cambia il colore Windows Media Player'interfaccia utente.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiamate quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento non accetta parametri.

## <a name="remarks"></a>Commenti

Gli utenti possono modificare il colore dell'Windows Media Player utente. È possibile usare questo evento per personalizzare l'aspetto della pagina Web ospitata in modo che corrisponda al lettore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





