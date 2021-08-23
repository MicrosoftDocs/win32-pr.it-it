---
title: Annidamento in modalità nativa
description: Nell'elenco seguente vengono descritti gli elementi che possono essere contenuti in un gruppo presente in un dominio in modalità nativa.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Annidamento in AD in modalità nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3fa2842981354738cd4ef112ef278fa33ca310adeedcd62fb245a2663cce07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025739"
---
# <a name="nesting-in-native-mode"></a>Annidamento in modalità nativa

Nell'elenco seguente vengono descritti gli elementi che possono essere contenuti in un gruppo presente in un dominio in modalità nativa. Lo stesso elenco si applica anche ai gruppi di distribuzione nei domini in modalità mista. L'ambito del gruppo determina queste regole di contenimento.

-   Un gruppo universale può contenere altri gruppi universali, gruppi globali e account da qualsiasi dominio all'interno della foresta in cui risiede questo gruppo universale.
-   Un gruppo globale può contenere altri gruppi globali e account dello stesso dominio a cui appartiene il gruppo. Un gruppo globale non può contenere gruppi universali o gruppi globali o account di un altro dominio.
-   Un gruppo locale di dominio può contenere gruppi universali, gruppi globali e account di qualsiasi dominio o foresta. Un gruppo locale di dominio può contenere anche altri gruppi locali di dominio dello stesso dominio a cui appartiene il gruppo. Un gruppo locale di dominio non può contenere altri gruppi locali di dominio di qualsiasi altro dominio o foresta.

 

 




