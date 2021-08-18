---
description: Un messaggio di fine viene inviato immediatamente dopo un messaggio della specifica di crittografia delle modifiche per verificare l'esito positivo dei processi di scambio delle chiavi e autenticazione.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Terminare i messaggi nel protocollo TLS 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e9af7502f0865661e2ed0f6a80059cb822395002ccaf035373dc3db322adac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006979"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a>Terminare i messaggi nel protocollo TLS 1.0

Un messaggio di fine viene inviato immediatamente dopo un messaggio della specifica di crittografia delle modifiche per verificare l'esito positivo dei processi di scambio delle chiavi e autenticazione. I messaggi di fine nel protocollo TLS 1.0 vengono calcolati usando la funzione [*pseudo-casuale*](../secgloss/p-gly.md) (PRF) con la [*chiave master,*](../secgloss/m-gly.md)un'etichetta e un valore di seed come input. PRF produce un output di lunghezza arbitraria. Il metodo seguente viene usato per generare l'output PRF usato nei messaggi di completamento TLS 1.0.

Un handle [*hash*](../secgloss/h-gly.md) PRF viene generato usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con il valore **\_ ID ALG** impostato su CALG TLS1PRF e l'handle per la chiave master passata nel \_ parametro *hKey.* I valori label e seed vengono impostati sull'handle hash usando rispettivamente i valori HP \_ TLS1PRF LABEL e \_ HP TLS1PRF SEED, nel parametro dwParam con la funzione \_ \_ [**CryptSetHashParam.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam)  Infine, il motore del protocollo chiama la funzione [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) con il valore HP HASHVAL nel \_ parametro *dwParam* per recuperare i dati PRF da includere nel messaggio di fine. Quando si effettua la chiamata a **CryptGetHashParam**, il motore del protocollo deve specificare il numero di byte di dati che PRF produrrà. Questa operazione viene eseguita nel *parametro pdwDataLen* e i dati risultanti vengono inseriti nel buffer a cui punta il *parametro pbData.*

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



 

 
