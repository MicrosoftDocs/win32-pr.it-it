---
description: La sintassi dei messaggi crittografici (CMS), derivata da PKCS \# 7 versione 1,5, è la sintassi usata per eseguire l'hashing, firmare digitalmente, autenticare e crittografare i messaggi arbitrari.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Aggiunte CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309983"
---
# <a name="cms-additions"></a>Aggiunte CMS

La sintassi dei messaggi crittografici (CMS), derivata da PKCS \# 7 versione 1,5, è la sintassi usata per eseguire l' [*hashing*](../secgloss/h-gly.md), [*firmare digitalmente*](../secgloss/d-gly.md), autenticare e crittografare i messaggi arbitrari. Laddove possibile, viene mantenuta la compatibilità con le versioni precedenti; sono state tuttavia apportate modifiche per supportare il trasferimento di certificati degli attributi e le tecniche di accordo chiave per la gestione delle chiavi. CMS consente più incapsulamento in modo che una busta di incapsulamento possa essere annidata all'interno di un'altra. Inoltre, un'entità può firmare digitalmente i dati incapsulati in precedenza; gli attributi arbitrari, ad esempio l'ora di firma, possono essere firmati insieme al contenuto del messaggio. gli attributi e, ad esempio [*controfirme*](../secgloss/c-gly.md), possono essere associati a una firma. CMS può supportare un'ampia gamma di architetture per la gestione delle chiavi basata sui certificati.

Per supportare altre funzionalità di CMS, alle strutture di dati sottostanti sono stati assegnati nuovi campi. Sono stati aggiunti anche nuovi flag e valori di parametro. Tutte le strutture di dati e tutte le API che usano CMS sono compatibili con le versioni precedenti del 100% con PKCS \# 7 versione 1,5.

Sono incluse aggiunte di [dati in busta](enveloped-data-additions.md) e aggiunte di [dati firmati](signed-data-additions.md).

 

 
