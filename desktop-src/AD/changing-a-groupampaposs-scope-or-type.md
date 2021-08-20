---
title: Modifica dell'ambito o del tipo di un gruppo
description: Questo argomento illustra come modificare l'ambito o il tipo di un gruppo in domini in modalità nativa.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- groups AD , modifica dell'ambito o del tipo di un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95babe931146078d78b15d1b1d2a33f79bb305acdc6e4449afde467a573514d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118023142"
---
# <a name="changing-a-groups-scope-or-type"></a>Modifica dell'ambito o del tipo di un gruppo

La modifica di un ambito o di un tipo di gruppo non è consentita nei domini in modalità mista. Tuttavia, nei domini in modalità nativa sono consentite le conversioni seguenti:

Da gruppo globale a gruppo universale: questa operazione è consentita solo se il gruppo globale non è membro di un altro gruppo globale.

Da gruppo locale di dominio a gruppo universale: il gruppo locale di dominio convertito non può contenere un altro gruppo locale di dominio.

Gruppo universale in gruppo globale o locale di dominio: per la conversione in gruppo globale, il gruppo universale convertito non può contenere utenti o gruppi globali di un altro dominio. Per la conversione in un gruppo locale di dominio, il gruppo universale convertito non può essere membro di un gruppo universale o di un gruppo locale di dominio di un altro dominio.

In modalità nativa, un tipo di gruppo può essere convertito liberamente tra gruppi di sicurezza e gruppi di distribuzione.

Tenere presente che se un gruppo viene usato per impostare il controllo di accesso, la modifica dell'ambito o del tipo può influire sulle voci di controllo di accesso (ACE) che contengono tale gruppo. Il sistema di sicurezza ignorerà le voci ACE contenenti gruppi che non sono gruppi di sicurezza.

 

 




