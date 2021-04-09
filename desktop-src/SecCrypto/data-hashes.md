---
description: Un hash di un testo o di un'altra stringa di byte è un valore associato, statisticamente univoco a lunghezza fissa.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hash dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885070"
---
# <a name="data-hashes"></a>Hash dei dati

Un [*hash*](../secgloss/h-gly.md) di un testo o di un'altra stringa di byte è un valore associato, statisticamente univoco a lunghezza fissa. In alcuni documenti, un *hash* di un testo viene anche definito digest; Tuttavia, in questa documentazione viene sempre usato il termine hash. Le funzioni CryptoAPI forniscono un metodo per creare un hash per qualsiasi testo o altra stringa di byte. Tale hash, quindi, può essere utilizzato come identificatore univoco dei dati associati.

Per garantire l' [*integrità*](../secgloss/i-gly.md) di un testo, è possibile inviare un [*hash*](../secgloss/h-gly.md) di un testo per accompagnare il testo. Il ricevitore può quindi calcolare un hash sui dati ricevuti e confrontare l'hash calcolato con l'hash ricevuto. Se le due corrispondenze, i dati ricevuti devono corrispondere ai dati da cui è stato creato l'hash ricevuto.

Per ottenere un valore hash, creare un oggetto hash usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Questo oggetto accumulerà i dati da verificare. I dati vengono quindi aggiunti all'oggetto hash con la funzione [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .

Dopo l'aggiunta dell'ultimo blocco di dati all'hash, viene usata la funzione [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) per ottenere il valore hash dei dati.

Viene garantita una migliore sicurezza eliminando l'oggetto hash con [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) non appena viene ottenuto il valore hash.

 

 
