---
description: Lo standard Unicode non prescrive significati specifici per i codici di controllo 0x000D (ritorno a capo) e 0x000A (avanzamento riga).
ms.assetid: fb8b1a5c-79a4-45a0-b7a1-8217c370d13e
title: Uso di codici di controllo ASCII 0x000D e 0x000A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44330b81582ca49808394b77d0d8913c94b808acd4314123ed6b49ff9676c196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146934"
---
# <a name="using-ascii-control-codes-0x000d-and-0x000a"></a>Uso di codici di controllo ASCII 0x000D e 0x000A

Lo standard Unicode non prescrive significati specifici per i codici di controllo 0x000D (ritorno a capo) e 0x000A (avanzamento riga). Questi codici non devono essere usati in combinazione. Se usato singolarmente, il codice può rappresentare se stesso solo o entrambi i codici insieme. L'applicazione deve sempre determinare cosa rappresentano questi codici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di caratteri speciali in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



