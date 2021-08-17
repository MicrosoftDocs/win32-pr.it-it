---
title: Flag di notifica delle modifiche
description: Flag di notifica delle modifiche
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Modifica
- Flag di notifica delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f5311e3313bf23c92972395143d288483181e7a69212115082a2f150d7d1bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791835"
---
# <a name="change-notification-flags"></a>Flag di notifica delle modifiche



| Costante                         | Valore      | Descrizione                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPI DI \_ MODIFICA NUM \_ \_ RTM          | 3          | Specifica il numero di tipi di modifica attualmente utilizzati dal gestore tabelle di routing.                                                                            |
| TIPO DI MODIFICA RTM \_ \_ \_ ALL           | 0x0001     | Notifica al client qualsiasi modifica apportata a una destinazione.                                                                                                                   |
| TIPO DI MODIFICA RTM \_ \_ \_ MIGLIORE          | 0x0002     | Notifica al client le modifiche alla route migliore o quando cambia la route migliore.                                                                                     |
| INOLTRO DEL TIPO DI \_ \_ MODIFICA \_ RTM    | 0x0004     | Notifica al client le modifiche di route migliori che influiscono sull'inoltro, ad esempio le modifiche dell'hop successivo.                                                                      |
| RTM NOTIFY ONLY MARKED DESTS (NOTIFICA RTM \_ SOLO \_ \_ \_ DESTS CONTRASSEGNATI) | 0x00010000 | Notifica al client le modifiche apportate alle destinazioni contrassegnate dal client. Se questo flag non viene specificato, vengono inviati messaggi di notifica delle modifiche per tutte le destinazioni. |



 

 

 




