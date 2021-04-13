---
description: Come generare, recuperare ed esportare le chiavi RSA/SChannel.
ms.assetid: 3069232f-d016-4973-ae39-89b0e2a03cd7
title: Chiavi RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c9d23de40f32a499013928086ccb52fc1d1e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526328"
---
# <a name="rsaschannel-keys"></a>Chiavi RSA/SChannel

## <a name="generating-and-retrieving-rsaschannel-keys"></a>Generazione e recupero di chiavi RSA/SChannel

[*RSA*](../secgloss/r-gly.md) / Le chiavi [*Schannel*](../secgloss/s-gly.md) possono essere generate chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . La chiamata a **CryptGenKey** richiede un \_ identificatore dell'algoritmo di scambio delle borse passato nel parametro *algido* .

**Per generare una coppia di chiavi pubblica/privata RSA/SChannel**

1.  Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il [provider di crittografia Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Chiamare la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per generare le chiavi. \_Per il parametro *algido* , è necessario passare a scambio chiavi e i 16 bit superiori del parametro *dwFlags* devono essere impostati sulla dimensione della chiave desiderata (512 bit). Viene restituito un handle della struttura [**HCRYPTKEY**](hcryptkey.md) nel parametro *HKEY* .

**Per recuperare un puntatore a chiavi utente RSA/SChannel generate in precedenza**

1.  Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il [provider di crittografia Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Chiamare la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) con il parametro *dwKeySpec* impostato su in corrispondenza di \_ .

## <a name="exporting-rsaschannel-keys"></a>Esportazione di chiavi RSA/SChannel

Le [*chiavi master*](../secgloss/m-gly.md) possono essere esportate in semplici strutture BLOB di chiavi. Questa operazione deve essere implementata in modo analogo all'esportazione di normali [*chiavi di crittografia di massa*](../secgloss/b-gly.md) [*RC4*](../secgloss/r-gly.md) o [*Data Encryption Standard*](../secgloss/d-gly.md) (des), come descritto in [Simple Key BLOB](https://www.bing.com/search?q=Simple+Key+BLOB). Il membro **aiKeyAlg** della struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) è impostato sull'identificatore dell'algoritmo della chiave master (CALG \_ PCT1 \_ Master, CALG \_ SSL2 \_ Master, CALG \_ SSL3 \_ master o CALG \_ TLS1 \_ Master).

Se la funzione [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) sta esportando una chiave master SSL2 e \_ viene impostato il flag di fallback SSL2 Crypt, \_ per evitare gli attacchi di rollback della versione, impostare i primi otto byte del [*riempimento*](../secgloss/p-gly.md) del blocco di crittografia su 0x03 anziché sui dati casuali.

Se la **costante \_ DESTROYKEY della crittografia** è specificata nel parametro *dwFlags* della funzione [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) , il CSP Elimina la chiave o l'handle di chiave dopo l'esportazione della chiave. Questo flag deve essere utilizzato solo con i [*BLOB opachi*](../secgloss/o-gly.md).

 

 
