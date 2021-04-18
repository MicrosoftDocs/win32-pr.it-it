---
title: PLAYERAPPLICATION. hasDisplay (attributo)
description: L'attributo hasDisplay recupera un valore che indica se il video può essere visualizzato tramite il controllo Media Player remoto di Windows.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- Media Player Windows PLAYERAPPLICATION. hasDisplay
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327051"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

L'attributo **hasDisplay** recupera un valore che indica se il video può essere visualizzato tramite il controllo Media Player remoto di Windows.

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di sola lettura.



| Valore | Descrizione               |
|-------|---------------------------|
| True  | Il video può essere visualizzato.    |
| Falso | Non è possibile visualizzare il video. |



 

## <a name="remarks"></a>Commenti

Questo attributo viene utilizzato solo quando la comunicazione remota del controllo Media Player di Windows.

È possibile eseguire contemporaneamente più controlli Media Player di Windows, ma i video possono essere visualizzati solo in una posizione alla volta, sia nella modalità completa del lettore che in uno dei controlli remoti. Usare questa proprietà per determinare se il controllo corrente è quello tramite il quale è possibile visualizzare il video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYERAPPLICATION**](playerapplication-element.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





