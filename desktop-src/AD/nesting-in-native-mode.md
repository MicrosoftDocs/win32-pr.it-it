---
title: Annidamento in modalità nativa
description: Nell'elenco seguente viene descritto il possibile contenuto di un gruppo esistente in un dominio in modalità nativa.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Annidamento in modalità nativa di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855398"
---
# <a name="nesting-in-native-mode"></a>Annidamento in modalità nativa

Nell'elenco seguente viene descritto il possibile contenuto di un gruppo esistente in un dominio in modalità nativa. Questo stesso elenco si applica anche ai gruppi di distribuzione nei domini in modalità mista. L'ambito del gruppo determina queste regole di contenimento.

-   Un gruppo universale può contenere altri gruppi universali, gruppi e account globali di qualsiasi dominio all'interno della foresta in cui risiede questo gruppo universale.
-   Un gruppo globale può contenere altri gruppi e account globali dello stesso dominio a cui appartiene il gruppo. Un gruppo globale non può contenere gruppi universali o qualsiasi account o gruppo globale di un altro dominio.
-   Un gruppo locale di dominio può contenere gruppi universali, gruppi globali e account di qualsiasi dominio o foresta. Un gruppo locale di dominio può inoltre contenere altri gruppi locali di dominio dello stesso dominio a cui appartiene il gruppo. Un gruppo locale di dominio non può contenere altri gruppi locali di dominio da qualsiasi altro dominio o insieme di strutture.

 

 




