---
title: Flag di notifica delle modifiche
description: Flag di notifica delle modifiche
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Modifica
- Flag di notifica delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330292"
---
# <a name="change-notification-flags"></a>Flag di notifica delle modifiche



| Costante                         | Valore      | Descrizione                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipi di \_ modifiche RTM num \_          | 3          | Specifica il numero di tipi di modifiche attualmente utilizzati da Gestione tabelle di routing.                                                                            |
| \_tipo di modifica RTM \_ \_ All           | 0x0001     | Notifica al client qualsiasi modifica a una destinazione.                                                                                                                   |
| \_tipo di modifica RTM \_ \_ migliore          | 0x0002     | Notifica al client le modifiche apportate alla route migliore o quando viene modificata la route migliore.                                                                                     |
| \_avanzamento del \_ tipo di modifica RTM \_    | 0x0004     | Notifica al client eventuali modifiche della route migliori che interessano l'inoltro, ad esempio le modifiche all'hop successivo.                                                                      |
| \_ \_ solo \_ \_ DestS contrassegnato per la notifica RTM | 0x00010000 | Notifica al client le modifiche apportate alle destinazioni contrassegnate dal client. Se questo flag non è specificato, vengono inviati i messaggi di notifica delle modifiche per tutte le destinazioni. |



 

 

 




