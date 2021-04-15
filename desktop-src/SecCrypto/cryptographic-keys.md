---
description: Le chiavi crittografiche sono fondamentali per le operazioni di crittografia.
ms.assetid: dda7b527-1522-4b43-8d8e-44ce7983a9aa
title: Chiavi crittografiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82858b26fa70ceacb4e7f9714e29983a773e66ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484620"
---
# <a name="cryptographic-keys"></a>Chiavi crittografiche

Le [*chiavi crittografiche*](../secgloss/c-gly.md) sono fondamentali per le operazioni di crittografia. Molti schemi di crittografia sono costituiti da coppie di operazioni, come la crittografia e la decrittografia o la firma e la verifica. Una *chiave* è una porzione di dati variabili che viene inserita come input in un algoritmo di crittografia per eseguire una di queste operazioni. In uno schema di crittografia ben progettato, la sicurezza dello schema dipende solo dalla sicurezza delle chiavi usate.

Le chiavi crittografiche possono essere classificate in base all'utilizzo all'interno di uno schema di crittografia, come [chiavi simmetriche](symmetric-keys.md) o [chiavi asimmetriche](public-private-key-pairs.md). Una [*chiave simmetrica*](../secgloss/s-gly.md) è una chiave singola utilizzata per entrambe le operazioni in uno schema di crittografia, ad esempio per [*crittografare*](../secgloss/e-gly.md) e [*decrittografare*](../secgloss/d-gly.md) i dati. In genere, la sicurezza dello schema dipende dalla garanzia che la chiave sia nota solo ai partecipanti autorizzati. Le chiavi asimmetriche, d'altra parte, vengono usate negli schemi di crittografia, in cui sono necessarie chiavi diverse per ogni operazione. Esempi comuni di tali schemi sono quelli che usano [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md), in cui la sicurezza dello schema dipende dalla garanzia che la [*chiave privata*](../secgloss/p-gly.md) sia nota solo a una parte. Ad esempio, i sistemi di crittografia a chiave pubblica/privata usano due chiavi, una [*chiave pubblica*](../secgloss/p-gly.md) che chiunque può usare per crittografare i dati e una [*chiave privata*](../secgloss/p-gly.md) posseduta solo dal destinatario autorizzato e che può essere usata per decrittografare i dati.

Le chiavi crittografiche possono essere ulteriormente classificate in base allo scopo per cui vengono usate. Che includono la generazione di firme digitali, la verifica della firma digitale, l'autenticazione del messaggio, la crittografia e la decrittografia dei dati, il ritorno a capo e il trasporto delle chiavi Per un elenco completo dei tipi di chiave come definito dal [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST), vedere la sezione 5 indicazioni generali sulla gestione delle chiavi della [pubblicazione speciale NIST 800-57: raccomandazione per la gestione delle chiavi-parte 1: generale (revisione)](https://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf).

 

 
