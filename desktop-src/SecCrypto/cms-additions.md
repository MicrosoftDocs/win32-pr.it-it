---
description: Cryptographic Message Syntax (CMS), derivata da PKCS 7 versione 1.5, è la sintassi usata per eseguire l'hashing, la firma digitale, l'autenticazione e la crittografia di \# messaggi arbitrari.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Aggiunte cms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce7c54867c1ee2a603e37751bf43a0abc65cee670c4a1fc994c9ace3f3404bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876961"
---
# <a name="cms-additions"></a>Aggiunte cms

Cryptographic Message Syntax (CMS), derivata da PKCS \# 7 versione 1.5, è la sintassi usata per eseguire [*l'hashing,*](../secgloss/h-gly.md) [*la*](../secgloss/d-gly.md)firma digitale, l'autenticazione e la crittografia di messaggi arbitrari. Se possibile, la compatibilità con le versioni precedenti viene mantenuta; Tuttavia, sono state apportate modifiche per supportare il trasferimento del certificato di attributo e le tecniche di contratto chiave per la gestione delle chiavi. CMS consente l'incapsulamento multiplo in modo che una busta di incapsulamento possa essere annidata all'interno di un'altra. Inoltre, un'entità può firmare digitalmente i dati incapsulati in precedenza; Gli attributi arbitrari, ad esempio l'ora di firma, possono essere firmati insieme al contenuto del messaggio. Gli attributi e , ad esempio [*le controfirme*](../secgloss/c-gly.md), possono essere associati a una firma. CMS può supportare un'ampia gamma di architetture per la gestione delle chiavi basata su certificati.

Per supportare funzionalità CMS aggiuntive, alle strutture di dati sottostanti sono stati dati nuovi campi. Sono stati aggiunti anche nuovi flag e valori di parametro. Tutte le strutture di dati e tutte le API che usano CMS sono compatibili al 100% con le versioni precedenti di PKCS \# 7 versione 1.5.

Le aggiunte includono [le aggiunte di dati in busta](enveloped-data-additions.md) e le aggiunte di dati [firmate.](signed-data-additions.md)

 

 
