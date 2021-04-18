---
title: Attributo temporaneo
description: L'attributo Temporary specifica se una playlist è temporanea.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Finestra degli attributi temporanei Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325575"
---
# <a name="temporary-attribute"></a>Attributo temporaneo

L'attributo **Temporary** specifica se una playlist è temporanea.

**Osservazioni:**

Se è stata recuperata una playlist dalla libreria, le modifiche apportate alla playlist verranno riflesse nella libreria dell'utente. Per evitare questo problema, chiamare [IWMPPlaylist:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passando il nome di attributo "Temporary" e il valore "true". Questa operazione converte l'istanza della playlist in una playlist temporanea, che è sicura per la modifica senza modificare la playlist originale.

**Si applica a**

-   [Playlist](playlist-attributes-ref.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





