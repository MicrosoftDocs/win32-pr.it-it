---
title: Evento External. OnColorChange
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnColorChange
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Media Player di Windows dell'evento External. OnColorChange
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
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328886"
---
# <a name="externaloncolorchange-event"></a>Evento External. OnColorChange

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'evento **OnColorChange** si verifica quando cambia il colore dell'interfaccia utente di Windows Media Player.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento non accetta parametri.

## <a name="remarks"></a>Commenti

Gli utenti possono modificare il colore dell'interfaccia utente di Windows Media Player. È possibile usare questo evento per personalizzare l'aspetto della pagina Web ospitata in modo che corrisponda al lettore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 2 online**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





