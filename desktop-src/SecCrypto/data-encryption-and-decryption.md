---
description: La crittografia è il processo di conversione di dati di testo normale (testo normale) in un elemento apparentemente casuale e non significativo (testo crittografato). La decrittografia è il processo di conversione del testo crittografato di nuovo in testo normale.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Crittografia e decrittografia dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128791"
---
# <a name="data-encryption-and-decryption"></a>Crittografia e decrittografia dei dati

La crittografia è il processo di conversione di dati di testo normale [*(testo normale) in*](../secgloss/p-gly.md)un elemento apparentemente casuale e non significativo (testo [*crittografato*](../secgloss/c-gly.md)). La decrittografia è il processo di conversione del testo crittografato di nuovo in testo normale.

Per crittografare più di una piccola quantità di dati, viene utilizzata la [*crittografia simmetrica*](../secgloss/s-gly.md) . Una [*chiave simmetrica*](../secgloss/s-gly.md) viene utilizzata durante i processi di crittografia e decrittografia. Per decrittografare una particolare parte del testo crittografato, è necessario usare la chiave usata per crittografare i dati.

L'obiettivo di ogni algoritmo di crittografia è renderlo il più difficile possibile per decrittografare il testo crittografato generato senza usare la chiave. Se viene usato un algoritmo di crittografia realmente valido, non sono disponibili tecniche significativamente migliori rispetto alla possibilità di provare ogni chiave possibile. Per un algoritmo di questo tipo, più è lunga la chiave, più è difficile decrittografare un pezzo di testo crittografato senza avere la chiave.

È difficile determinare la qualità di un algoritmo di crittografia. Gli algoritmi che sembrano promesse a volte diventano molto facili da interrompere, dato l'attacco appropriato. Quando si seleziona un algoritmo di crittografia, è consigliabile sceglierne uno che è stato usato per diversi anni e che abbia superato tutti gli attacchi.

Per altre informazioni, vedere [funzioni di crittografia e decrittografia dei dati](cryptography-functions.md).

 

 
