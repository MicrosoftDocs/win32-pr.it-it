---
description: Un messaggio di fine viene inviato immediatamente dopo un messaggio di specifica della crittografia delle modifiche per verificare la riuscita dei processi di scambio e autenticazione delle chiavi.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Terminare i messaggi nel protocollo TLS 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a0f0f3e85916e66d434cb3e69b083348e40143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316171"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a>Terminare i messaggi nel protocollo TLS 1,0

Un messaggio di fine viene inviato immediatamente dopo un messaggio di specifica della crittografia delle modifiche per verificare la riuscita dei processi di scambio e autenticazione delle chiavi. I messaggi di fine nel protocollo TLS 1,0 vengono calcolati usando la [*funzione pseudo-random*](../secgloss/p-gly.md) (PRF) con la [*chiave master*](../secgloss/m-gly.md), un'etichetta e un valore di inizializzazione come input. PRF produce un output di lunghezza arbitraria. Il metodo seguente viene usato per generare l'output PRF usato nei messaggi di fine TLS 1,0.

Un handle [*hash*](../secgloss/h-gly.md) PRF viene generato usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con il valore di **\_ ID ALG** impostato su CALG \_ TLS1PRF e l'handle per la chiave master passata nel parametro *HKEY* . I valori di inizializzazione e di etichetta vengono impostati sull'handle hash usando i valori HP \_ TLS1PRF \_ Label e HP \_ TLS1PRF \_ Seed rispettivamente nel parametro *dwParam* con la funzione [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) . Infine, il motore di protocollo chiama la funzione [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) con il valore HP \_ HASHVAL nel parametro *dwParam* per recuperare i dati PRF da includere nel messaggio di fine. Quando si effettua la chiamata a **CryptGetHashParam**, il motore di protocollo deve specificare il numero di byte di data PRF da produrre. Questa operazione viene eseguita nel parametro *pdwDataLen* e i dati risultanti vengono inseriti nel buffer a cui punta il parametro *pbData* .

Di seguito è riportato il codice sorgente tipico per questo motore di protocollo:


```C++
CRYPT_DATA_BLOB Data;
HCRYPTHASH hFinishHash;
BYTE rgbFinishPRF[12];
BYTE rgbCliHashOfHandshakes[36];

//------------------------------------------------------------
// get client finish message

CryptCreateHash(
         hProv, 
         CALG_TLS1PRF, 
         hMasterKey, 
         0, 
         &hFinishHash);

Data.pbData = (BYTE*)"client finished";
Data.cbData = 15;
CryptSetHashParam(
         hFinishHash, 
         HP_TLS1PRF_LABEL, 
         (BYTE*)&Data, 
         0);

Data.pbData = rgbCliHashOfHandshakes;
Data.cbData = sizeof(rgbCliHashOfHandshakes);
CryptSetHashParam(
          hFinishHash, 
          HP_TLS1PRF_SEED, 
          (BYTE*)&Data, 
          0);

cbFinishPRF = sizeof(rgbFinishPRF);
CryptGetHashParam(
          hFinishHash, 
          HP_HASHVAL, 
          rgbFinishPRF, 
          &cbFinishPRF, 
          0);

CryptDestroyHash(hFinishHash);
```



 

 
