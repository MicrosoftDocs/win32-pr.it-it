---
title: Attributi di sincronizzazione
description: Gli attributi Sync01 tramite Sync16 sono rappresentazioni di stringa di valori a 32 bit utilizzati da Windows Media Player durante la sincronizzazione delle playlist con uno di un massimo di 16 dispositivi portatili.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Attributi di sincronizzazione Windows Media Player
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325580"
---
# <a name="sync-attributes"></a>Attributi di sincronizzazione

Gli attributi **Sync01** tramite **Sync16** sono rappresentazioni di stringa di valori a 32 bit utilizzati da Windows Media Player durante la sincronizzazione delle playlist con uno di un massimo di 16 dispositivi portatili.

## <a name="applies-to"></a>Si applica a

-   [Playlist](playlist-attributes-ref.md)

## <a name="remarks"></a>Commenti

Si tratta di attributi di lettura/scrittura. Un valore pari a zero indica che Windows Media Player non deve sincronizzare la playlist con il dispositivo associato. Un valore maggiore di zero indica una priorità di sincronizzazione per la playlist specificata.

In base all'input dell'utente, Windows Media Player imposta questo attributo per ogni playlist nella libreria. Quando Windows Media Player tenta di sincronizzare una playlist con un dispositivo portatile, esamina ogni playlist per confrontare i valori per gli attributi di **Sync**_XX_ che rappresentano la partnership del dispositivo. Le playlist con valori _XX_ della **sincronizzazione** inferiore ricevono una priorità di sincronizzazione superiore.

Ad esempio, la libreria potrebbe contenere le quattro playlist seguenti e i rispettivi valori _XX_ della **sincronizzazione**:



| Nome della playlist | Valore Sync01 |
|---------------|--------------|
| GymMusic. WPL  | 0x0000000D   |
| Relax. WPL     | 0x00000020   |
| DriveHome. WPL | 0x00000001   |
| NoGo. WPL      | 0x00000000   |



 

Quando Windows Media Player sincronizza il dispositivo associato all'attributo, sincronizza le playlist nell'ordine seguente:

1.  DriveHome. WPL
2.  GymMusic. WPL
3.  Relax. WPL

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> <dt>

[**Enumerazione delle playlist di sincronizzazione**](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





