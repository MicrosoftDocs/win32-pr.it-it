---
title: Modifica dell'ambito o del tipo di un gruppo
description: In questo argomento viene illustrato come modificare l'ambito o il tipo di un gruppo in domini in modalità nativa.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- gruppi di Active Directory, modifica dell'ambito o del tipo di un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707207"
---
# <a name="changing-a-groups-scope-or-type"></a>Modifica dell'ambito o del tipo di un gruppo

La modifica di un ambito o di un tipo di gruppo non è consentita nei domini in modalità mista. Tuttavia, le conversioni seguenti sono consentite nei domini in modalità nativa:

Gruppo globale-gruppo universale: questa operazione è consentita solo se il gruppo globale non è un membro di un altro gruppo globale.

Gruppo locale di dominio in gruppo universale: il gruppo locale di dominio da convertire non può contenere un altro gruppo locale di dominio.

Dal gruppo universale al gruppo locale di dominio o globale: per la conversione in un gruppo globale, il gruppo universale convertito non può contenere utenti o gruppi globali di un altro dominio. Per la conversione in un gruppo locale di dominio, il gruppo universale convertito non può essere membro di un gruppo universale o di un gruppo locale di dominio di un altro dominio.

In modalità nativa, un tipo di gruppo può essere convertito liberamente tra i gruppi di sicurezza e i gruppi di distribuzione.

Tenere presente che se un gruppo viene usato per impostare il controllo di accesso, la modifica dell'ambito o del tipo può influire sulle voci di controllo di accesso (ACE) che contengono tale gruppo. Il sistema di sicurezza ignorerà le voci ACE contenenti gruppi che non sono gruppi di sicurezza.

 

 




