---
description: La crittografia è il processo di conversione dei dati di testo normale (testo non crittografato) in un elemento che sembra essere casuale e senza significato (testo crittografato). La decrittografia è il processo di conversione del testo crittografato in testo non crittografato.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Crittografia e decrittografia dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba508eeb67570d1f293ae55e1b6bff5217529663a6682a17d9817a9dc0834803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100911"
---
# <a name="data-encryption-and-decryption"></a>Crittografia e decrittografia dei dati

La crittografia è il processo di conversione dei dati di testo normale [*(*](../secgloss/p-gly.md)testo non crittografato ) in un elemento che sembra casuale e senza significato ([*testo crittografato*](../secgloss/c-gly.md)). La decrittografia è il processo di conversione del testo crittografato in testo non crittografato.

Per crittografare più di una piccola quantità di dati, [*viene usata la crittografia*](../secgloss/s-gly.md) simmetrica. Una [*chiave simmetrica viene usata*](../secgloss/s-gly.md) durante i processi di crittografia e decrittografia. Per decrittografare un particolare frammento di testo crittografato, è necessario usare la chiave usata per crittografare i dati.

L'obiettivo di ogni algoritmo di crittografia è quello di rendere il più difficile possibile decrittografare il testo crittografato generato senza usare la chiave. Se si usa un algoritmo di crittografia molto efficace, non esiste una tecnica significativamente migliore rispetto al tentativo metodico di ogni possibile chiave. Per un algoritmo di questo tipo, più lunga è la chiave, più difficile è decrittografare un frammento di testo crittografato senza possedere la chiave.

È difficile determinare la qualità di un algoritmo di crittografia. Gli algoritmi che sembrano a volte molto semplici da interrompere, in base all'attacco appropriato. Quando si seleziona un algoritmo di crittografia, è buona idea sceglierne uno che sia in uso da diversi anni e che abbia reato contro tutti gli attacchi.

Per altre informazioni, vedere [Funzioni di crittografia e decrittografia dei dati.](cryptography-functions.md)

 

 
