---
title: Attributo PLAYERAPPLICATION.hasDisplay
description: L'attributo hasDisplay recupera un valore che indica se il video può essere visualizzato tramite il controllo Windows Media Player remoto.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION.hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac144f7e9f96db707944cbb016028578d2446be43a0f06cd0293cb5d56f84c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571944"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

**L'attributo hasDisplay** recupera un valore che indica se il video può essere visualizzato tramite il controllo Windows Media Player remoto.

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano **di sola lettura.**



| Valore | Descrizione               |
|-------|---------------------------|
| True  | Il video può essere visualizzato.    |
| Falso | Il video non può essere visualizzato. |



 

## <a name="remarks"></a>Commenti

Questo attributo viene usato solo quando si esegue la comunicazione remota del Windows Media Player remoto.

Diversi Windows Media Player possono essere eseguiti in remoto contemporaneamente, ma i video possono essere visualizzati solo in una posizione alla volta, nella modalità completa del lettore o in uno dei controlli remoti. Usare questa proprietà per determinare se il controllo corrente è quello tramite il quale è possibile visualizzare il video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYERAPPLICATION**](playerapplication-element.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





