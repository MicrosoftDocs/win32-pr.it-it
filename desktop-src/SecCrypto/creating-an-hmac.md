---
description: Viene illustrato come creare un HMAC.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Creazione di un HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb600b00c0bfa3ac8af24cd297b1e2dd67933e2990216dafe84713ee5e831c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876668"
---
# <a name="creating-an-hmac"></a>Creazione di un HMAC

**Per calcolare un HMAC**

1.  Ottenere un puntatore a Microsoft [*Cryptographic Service Provider*](../secgloss/c-gly.md) (CSP) chiamando [**CryptAcquireContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
2.  Creare un handle per un oggetto [*hash*](../secgloss/h-gly.md) [*HMAC*](../secgloss/h-gly.md)chiamando [**CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) Passare CALG \_ HMAC nel *parametro Algid.* Passare l'handle di [*una chiave simmetrica*](../secgloss/s-gly.md) nel *parametro hKey.* Questa chiave simmetrica è la chiave usata per calcolare HMAC.
3.  Specificare il tipo di hash da usare chiamando [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) con il *parametro dwParam* impostato sul valore HP \_ HMAC \_ INFO. Il *parametro pbData* deve puntare a una struttura [**HMAC INFO \_ inizializzata.**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info)
4.  Chiamare [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) per iniziare a calcolare il valore HMAC dei dati. La prima chiamata a **CryptHashData** fa sì che il valore della chiave sia combinato usando l'operatore XOR con la stringa interna e i dati. Viene eseguito l'hashing del risultato dell'operazione XOR e quindi viene eseguito l'hashing dei dati di destinazione per HMAC (a cui punta il parametro *pbData* passato nella chiamata a **CryptHashData).** Se necessario, è possibile effettuare chiamate successive a **CryptHashData** per completare l'hashing dei dati di destinazione.
5.  Chiamare [**CryptGetHashParam con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) il *parametro dwParam* impostato su HP \_ HASHVAL. Questa chiamata fa sì che l'hash interno sia completato e che la stringa esterna sia combinata usando XOR con la chiave. Viene eseguito l'hashing del risultato dell'operazione XOR e quindi viene eseguito l'hashing del risultato dell'hash interno (completato nel passaggio precedente). L'hash esterno viene quindi completato e restituito nel *parametro pbData* e la lunghezza nel *parametro dwDataLen.*

> [!Note]  
> Non usare la stessa chiave [*simmetrica*](../secgloss/s-gly.md) ([*sessione*](../secgloss/s-gly.md)) per la crittografia dei messaggi [*e la Message Authentication Code*](../secgloss/m-gly.md) (MAC). L'uso della stessa chiave per entrambi aumenta notevolmente il rischio che i messaggi vengano decodificati da utenti malintenzionati.

 

 

 
