---
description: Un hash di un testo o di un'altra stringa di byte è un valore a lunghezza fissa associato, statisticamente univoco.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hash dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a998c2172f6bd3b48bb3cdc94f1ed2207384606950dd9d6e8b6f3152149eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767769"
---
# <a name="data-hashes"></a>Hash dei dati

Un [*hash*](../secgloss/h-gly.md) di un testo o di un'altra stringa di byte è un valore a lunghezza fissa associato, statisticamente univoco. In alcuni documenti, un *hash* di un testo è detto anche digest. Tuttavia, in questa documentazione verrà sempre usato il termine hash. Le funzioni CryptoAPI consentono di creare un hash per qualsiasi testo o altra stringa di byte. L'hash può quindi essere usato come identificatore univoco dei dati associati.

Per garantire [*l'integrità*](../secgloss/i-gly.md) di un testo, è [*possibile inviare*](../secgloss/h-gly.md) un hash di un testo a corredato del testo. Il ricevitore può quindi calcolare un hash sui dati ricevuti e confrontare l'hash calcolato con l'hash ricevuto. Se le due corrispondenze, i dati ricevuti devono corrispondere ai dati da cui è stato creato l'hash ricevuto.

Per ottenere un valore hash, creare un oggetto hash [**usando CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) Questo oggetto accumula i dati da verificare. I dati vengono quindi aggiunti all'oggetto hash con la [**funzione CryptHashData.**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)

Dopo l'aggiunta dell'ultimo blocco di dati all'hash, viene usata la funzione [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) per ottenere il valore hash dei dati.

Una maggiore sicurezza viene fornita tramite l'eliminazione dell'oggetto hash [**con CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) non appena viene ottenuto il valore hash.

 

 
