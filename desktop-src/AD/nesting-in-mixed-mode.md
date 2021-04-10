---
title: Annidamento in modalità mista
description: Questo argomento elenca le restrizioni dei gruppi di sicurezza in un dominio in modalità mista.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Annidamento in modalità mista AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855401"
---
# <a name="nesting-in-mixed-mode"></a>Annidamento in modalità mista

Questo argomento elenca le restrizioni dei gruppi di sicurezza in un dominio in modalità mista.

I gruppi di sicurezza in un dominio in modalità mista presentano le restrizioni seguenti:

-   Non è possibile creare gruppi universali in domini in modalità mista perché l'ambito universale è supportato solo nei domini in modalità nativa di Windows 2000.
-   Un gruppo globale può contenere account dello stesso dominio a cui appartiene il gruppo. Un gruppo globale non può contenere gruppi universali, gruppi globali o un account di un altro dominio.
-   Un gruppo locale di dominio può contenere gruppi e account globali di qualsiasi dominio o foresta. Un gruppo locale di dominio non può contenere altri gruppi locali di dominio.

Tenere presente che i gruppi di distribuzione possono essere annidati in base alle regole di annidamento per la modalità nativa.

 

 




