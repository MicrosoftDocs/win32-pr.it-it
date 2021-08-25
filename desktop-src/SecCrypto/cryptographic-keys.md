---
description: Le chiavi crittografiche sono centrali per le operazioni crittografiche.
ms.assetid: dda7b527-1522-4b43-8d8e-44ce7983a9aa
title: Chiavi crittografiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25647d64aafa8d996c60df37d1f5b5a86226451e1a0f3a3cfefc7ef405f3a11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876301"
---
# <a name="cryptographic-keys"></a>Chiavi crittografiche

[*Le chiavi crittografiche*](../secgloss/c-gly.md) sono centrali per le operazioni crittografiche. Molti schemi di crittografia sono costituiti da coppie di operazioni, ad esempio crittografia e decrittografia o firma e verifica. Una *chiave* è una parte di dati variabili che viene immessa come input in un algoritmo di crittografia per eseguire un'operazione di questo tipo. In uno schema di crittografia ben progettato, la sicurezza dello schema dipende solo dalla sicurezza delle chiavi usate.

Le chiavi crittografiche possono essere classificate in base al relativo utilizzo all'interno di uno schema di crittografia, ad esempio [chiavi simmetriche](symmetric-keys.md) o [chiavi asimmetriche.](public-private-key-pairs.md) Una [*chiave simmetrica*](../secgloss/s-gly.md) è una singola chiave usata per entrambe le operazioni [](../secgloss/e-gly.md) in uno schema di crittografia, ad esempio per crittografare e decrittografare i dati. [](../secgloss/d-gly.md) In genere, la sicurezza dello schema dipende dal fatto che la chiave sia nota solo ai partecipanti autorizzati. Le chiavi asimmetriche, d'altra parte, vengono usate negli schemi di crittografia in cui sono necessarie chiavi diverse per ogni operazione. Esempi comuni di questi schemi sono quelli che usano coppie di chiavi [*pubbliche/private,*](../secgloss/p-gly.md)in cui la sicurezza dello schema dipende dal fatto che la chiave privata sia nota solo a una parte. [](../secgloss/p-gly.md) Ad esempio, i sistemi di crittografia a [](../secgloss/p-gly.md) chiave pubblica/privata usano due [](../secgloss/p-gly.md) chiavi, una chiave pubblica che chiunque può usare per crittografare i dati e una chiave privata che solo il destinatario autorizzato possiede e che può essere usata per decrittografare i dati.

Le chiavi crittografiche possono essere ulteriormente classificate in base allo scopo per cui vengono usate. Questi usi includono la generazione della firma digitale, la verifica della firma digitale, l'autenticazione dei messaggi, la crittografia e la decrittografia dei dati, il wrapping delle chiavi e il trasporto delle chiavi. Per un elenco completo dei tipi di chiave definiti dal [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST), vedere la sezione 5 GENERAL KEY MANAGEMENT GUIDANCE of [NIST Special Publication 800-57: Recommendation for Key Management - Part 1: General (Revised)](https://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf).

 

 
