---
title: Attributi di sincronizzazione
description: Gli attributi da Sync01 a Sync16 sono rappresentazioni di stringa di valori a 32 bit che Windows Media Player usa quando sincronizza le playlist con uno dei 16 dispositivi portatili.
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
ms.openlocfilehash: e720598b17db6b073524d80afc8f39dd6e6f87e777246b5bdb60294b161fa1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134754"
---
# <a name="sync-attributes"></a>Attributi di sincronizzazione

Gli attributi **da Sync01** a **Sync16** sono rappresentazioni di stringa di valori a 32 bit che Windows Media Player usa quando sincronizza le playlist con uno dei 16 dispositivi portatili.

## <a name="applies-to"></a>Si applica a

-   [Playlist](playlist-attributes-ref.md)

## <a name="remarks"></a>Commenti

Si tratta di attributi di lettura/scrittura. Il valore zero indica che Windows Media Player la playlist non deve essere sincronizzata con il dispositivo associato. Un valore maggiore di zero indica una priorità di sincronizzazione per la playlist specificata.

In base all'input dell Windows Media Player'utente, questo attributo viene impostato per ogni playlist nella libreria. Quando Windows Media Player di sincronizzare una playlist con un dispositivo portatile, esamina ogni playlist per confrontare i valori per gli attributi **Sync**_XX_ che rappresentano la relazione tra dispositivi. Le playlist con valori **Sync**_XX inferiori_ ricevono una priorità di sincronizzazione più alta.

Ad esempio, la libreria potrebbe contenere le quattro playlist seguenti e i rispettivi **valori Sync**_XX:_



| Nome playlist | Valore sync01 |
|---------------|--------------|
| GymMusic.WPL  | 0x0000000D   |
| Relax.WPL     | 0x00000020   |
| DriveHome.WPL | 0x00000001   |
| NoGo.WPL      | 0x00000000   |



 

Quando Windows Media Player sincronizza il dispositivo associato all'attributo , le playlist verranno sincronizzate nell'ordine seguente:

1.  DriveHome.WPL
2.  GymMusic.WPL
3.  Relax.WPL

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> <dt>

[**Enumerazione delle playlist di sincronizzazione**](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





