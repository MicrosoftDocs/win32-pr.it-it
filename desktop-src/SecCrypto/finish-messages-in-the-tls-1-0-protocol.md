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
# <a name="finish-messages-in-the-tls-10-protocol"></a><span data-ttu-id="9a79b-103">Terminare i messaggi nel protocollo TLS 1,0</span><span class="sxs-lookup"><span data-stu-id="9a79b-103">Finish Messages in the TLS 1.0 Protocol</span></span>

<span data-ttu-id="9a79b-104">Un messaggio di fine viene inviato immediatamente dopo un messaggio di specifica della crittografia delle modifiche per verificare la riuscita dei processi di scambio e autenticazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="9a79b-104">A finish message is sent immediately after a change cipher spec message to verify the success of key exchange and authentication processes.</span></span> <span data-ttu-id="9a79b-105">I messaggi di fine nel protocollo TLS 1,0 vengono calcolati usando la [*funzione pseudo-random*](../secgloss/p-gly.md) (PRF) con la [*chiave master*](../secgloss/m-gly.md), un'etichetta e un valore di inizializzazione come input.</span><span class="sxs-lookup"><span data-stu-id="9a79b-105">The finish messages in the TLS 1.0 protocol are calculated using [*Pseudo-Random Function*](../secgloss/p-gly.md) (PRF) with the [*master key*](../secgloss/m-gly.md), a label, and a seed as input.</span></span> <span data-ttu-id="9a79b-106">PRF produce un output di lunghezza arbitraria.</span><span class="sxs-lookup"><span data-stu-id="9a79b-106">PRF produces an output of arbitrary length.</span></span> <span data-ttu-id="9a79b-107">Il metodo seguente viene usato per generare l'output PRF usato nei messaggi di fine TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="9a79b-107">The following method is used to generate the PRF output used in TLS 1.0 finish messages.</span></span>

<span data-ttu-id="9a79b-108">Un handle [*hash*](../secgloss/h-gly.md) PRF viene generato usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con il valore di **\_ ID ALG** impostato su CALG \_ TLS1PRF e l'handle per la chiave master passata nel parametro *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="9a79b-108">A PRF [*hash*](../secgloss/h-gly.md) handle is generated using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with the **ALG\_ID** value set to CALG\_TLS1PRF and the handle to the master key passed in the *hKey* parameter.</span></span> <span data-ttu-id="9a79b-109">I valori di inizializzazione e di etichetta vengono impostati sull'handle hash usando i valori HP \_ TLS1PRF \_ Label e HP \_ TLS1PRF \_ Seed rispettivamente nel parametro *dwParam* con la funzione [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) .</span><span class="sxs-lookup"><span data-stu-id="9a79b-109">The label and seed values are set on the hash handle using the values HP\_TLS1PRF\_LABEL and HP\_TLS1PRF\_SEED, respectively, in the *dwParam* parameter with the [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) function.</span></span> <span data-ttu-id="9a79b-110">Infine, il motore di protocollo chiama la funzione [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) con il valore HP \_ HASHVAL nel parametro *dwParam* per recuperare i dati PRF da includere nel messaggio di fine.</span><span class="sxs-lookup"><span data-stu-id="9a79b-110">Finally, the protocol engine calls the function [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) with the value HP\_HASHVAL in the *dwParam* parameter to retrieve the PRF data to be included in the finish message.</span></span> <span data-ttu-id="9a79b-111">Quando si effettua la chiamata a **CryptGetHashParam**, il motore di protocollo deve specificare il numero di byte di data PRF da produrre.</span><span class="sxs-lookup"><span data-stu-id="9a79b-111">When making the call to **CryptGetHashParam**, the protocol engine must specify how many bytes of data PRF will produce.</span></span> <span data-ttu-id="9a79b-112">Questa operazione viene eseguita nel parametro *pdwDataLen* e i dati risultanti vengono inseriti nel buffer a cui punta il parametro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="9a79b-112">This is done in the *pdwDataLen* parameter, and the resulting data is placed in the buffer pointed to by the *pbData* parameter.</span></span>

<span data-ttu-id="9a79b-113">Di seguito è riportato il codice sorgente tipico per questo motore di protocollo:</span><span class="sxs-lookup"><span data-stu-id="9a79b-113">The following is typical source code for this protocol engine:</span></span>


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



 

 
