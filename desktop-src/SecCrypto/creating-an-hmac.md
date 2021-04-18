---
description: Viene illustrato come creare un HMAC.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Creazione di un HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364314081bd1d84d6d9bfff889c234470cc6775c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314130"
---
# <a name="creating-an-hmac"></a>Creazione di un HMAC

**Per calcolare un HMAC**

1.  Ottenere un puntatore al provider del [*servizio di crittografia*](../secgloss/c-gly.md) (CSP) Microsoft chiamando [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
2.  Creare un handle per un [](../secgloss/h-gly.md)[*oggetto hash*](../secgloss/h-gly.md) HMAC chiamando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Passare CALG \_ HMAC nel parametro *algido* . Passare l'handle di una [*chiave simmetrica*](../secgloss/s-gly.md) nel parametro *HKEY* . Questa chiave simmetrica è la chiave utilizzata per calcolare il HMAC.
3.  Specificare il tipo di hash da utilizzare chiamando [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) con il parametro *dwParam* impostato sul valore HP \_ HMAC \_ info. Il parametro *pbData* deve puntare a una struttura [**di \_ informazioni HMAC**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info) inizializzata.
4.  Chiamare [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) per iniziare a calcolare il HMAC dei dati. La prima chiamata a **CryptHashData** fa sì che il valore della chiave venga combinato usando l'operatore XOR con la stringa interna e i dati. Viene generato un hash per il risultato dell'operazione XOR, quindi i dati di destinazione per HMAC (a cui fa riferimento il parametro *pbData* passato nella chiamata a **CryptHashData**) vengono sottoposizionati a hash. Se necessario, è possibile che vengano effettuate chiamate successive a **CryptHashData** per completare l'hashing dei dati di destinazione.
5.  Chiamare [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) con il parametro *DWPARAM* impostato su HP \_ HASHVAL. Questa chiamata fa sì che l'hash interno venga completato e che la stringa esterna venga combinata usando XOR con la chiave. Viene eseguito l'hashing del risultato dell'operazione XOR, quindi viene generato un hash per il risultato dell'hash interno (completato nel passaggio precedente). L'hash esterno viene quindi terminato e restituito nel parametro *pbData* e la lunghezza nel parametro *dwDataLen* .

> [!Note]  
> Non usare la stessa chiave [*simmetrica*](../secgloss/s-gly.md) ([*Session*](../secgloss/s-gly.md)) per la generazione di crittografia dei messaggi e di [*Message Authentication Code*](../secgloss/m-gly.md) (Mac). L'utilizzo della stessa chiave per entrambi aumenta significativamente il rischio che i messaggi vengano decodificati da utenti malintenzionati.

 

 

 
