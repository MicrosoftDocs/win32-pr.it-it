---
title: Annidamento in modalità mista
description: Questo argomento elenca le restrizioni dei gruppi di sicurezza in un dominio in modalità mista.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Annidamento in Active Directory in modalità mista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c53fd79cb10c452dbb363c3d6803071e6e52871f0ce87b03f9d06a61eaece8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185823"
---
# <a name="nesting-in-mixed-mode"></a>Annidamento in modalità mista

Questo argomento elenca le restrizioni dei gruppi di sicurezza in un dominio in modalità mista.

I gruppi di sicurezza in un dominio in modalità mista hanno le restrizioni seguenti:

-   Non è possibile creare gruppi universali in domini in modalità mista perché l'ambito universale è supportato solo in Windows 2000 domini in modalità nativa.
-   Un gruppo globale può contenere account dello stesso dominio a cui appartiene il gruppo. Un gruppo globale non può contenere gruppi universali, gruppi globali o un account di un altro dominio.
-   Un gruppo locale di dominio può contenere gruppi globali e account di qualsiasi dominio o foresta. Un gruppo locale di dominio non può contenere altri gruppi locali di dominio.

Tenere presente che i gruppi di distribuzione possono essere annidati in base alle regole di annidamento per la modalità nativa.

 

 




