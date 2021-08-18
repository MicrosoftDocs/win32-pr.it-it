---
description: Le credenziali Schannel sono rappresentate internamente come strutture CERT \_ CONTEXT.
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 Private Keys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ca6356849894ac5d15c07a0116bee7c2a2ba84df8c79de360d96f1e147fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008689"
---
# <a name="cryptoapi-20-private-keys"></a>CryptoAPI 2.0 Private Keys

Le credenziali Schannel sono rappresentate internamente come [**strutture CERT \_ CONTEXT.**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Schannel individua la chiave [*privata*](/windows/desktop/SecGloss/p-gly) associata a un particolare contesto di certificato usando la proprietà CERT KEY PROV PROP ID PROP del \_ \_ \_ \_ \_ certificato. Usando questa proprietà, Schannel accede alla *chiave privata* chiamando la [**funzione CryptAcquireContext.**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) Per altri dettagli, vedere [Coppie di chiavi pubbliche/private.](/windows/desktop/SecCrypto/public-private-key-pairs)

Ogni credenziale Schannel contiene un riferimento a una o più chiavi private, ognuna associata a un certificato specifico. Le [*chiavi private*](/windows/desktop/SecGloss/p-gly) vengono gestite in modo diverso a seconda che le credenziali siano per un client o un server.

## <a name="client-private-keys"></a>Chiavi private client

Le [*chiavi private*](/windows/desktop/SecGloss/p-gly) client vengono gestite dal provider del servizio [*di*](/windows/desktop/SecGloss/c-gly) crittografia (CSP) in uso. Le chiavi private client vengono in genere archiviate da CSP di [tipo PROV \_ RSA \_ FULL](/windows/desktop/SecCrypto/prov-rsa-full) o PROV \_ RSA \_ SIGNATURE.

Se l'applicazione client esegue manualmente la chiamata [**a CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) prima di chiamare [**AcquireCredentialsHandle,**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)il client deve associare l'handle del provider di servizi di crittografia al contesto del certificato usando la proprietà \_ CERT KEY \_ PROV \_ HANDLE PROP \_ \_ ID. Se Schannel trova questo set di proprietà, non usa la proprietà \_ CERT KEY \_ PROV \_ INFO PROP \_ \_ ID.

## <a name="server-private-keys"></a>Chiavi private del server

Le chiavi private del server vengono archiviate da uno dei seguenti CSP:

-   PROV \_ RSA \_ SCHANNEL
-   PROV \_ DH \_ SCHANNEL
-   PROV \_ FORTEZZA CSP

La scelta di CSP dipende dall'algoritmo di [*scambio di chiavi selezionato.*](/windows/desktop/SecGloss/k-gly) Le chiavi private del server devono essere di tipo AT \_ KEYEXCHANGE.

 

 
