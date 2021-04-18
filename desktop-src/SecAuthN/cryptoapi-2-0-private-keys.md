---
description: Le credenziali Schannel sono rappresentate internamente come strutture del contesto del certificato \_ .
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: Chiavi private CryptoAPI 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313744"
---
# <a name="cryptoapi-20-private-keys"></a>Chiavi private CryptoAPI 2.0

Le credenziali Schannel sono rappresentate internamente come strutture del [**\_ contesto del certificato**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . Schannel individua la [*chiave privata*](/windows/desktop/SecGloss/p-gly) associata a un particolare contesto del certificato usando la \_ Proprietà CERT Key \_ prova \_ info \_ prop \_ ID del certificato. Utilizzando questa proprietà, Schannel accede alla *chiave privata* chiamando la funzione [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) . Per ulteriori informazioni, vedere [coppie di chiavi pubbliche/private](/windows/desktop/SecCrypto/public-private-key-pairs).

Ogni credenziale Schannel contiene un riferimento a una o più chiavi private, ciascuna associata a un particolare certificato. Le [*chiavi private*](/windows/desktop/SecGloss/p-gly) vengono gestite in modo diverso a seconda che si tratti di una credenziale per un client o un server.

## <a name="client-private-keys"></a>Chiavi private client

Le [*chiavi private*](/windows/desktop/SecGloss/p-gly) del client vengono gestite dal [*provider del servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP) in uso. Le chiavi private del client vengono in genere archiviate da DSN di tipo [prov \_ RSA \_ full](/windows/desktop/SecCrypto/prov-rsa-full) o prov \_ RSA \_ Signature.

Se l'applicazione client esegue manualmente la chiamata [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) , prima di chiamare [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), il client deve associare l'handle del CSP al contesto del certificato usando la \_ Proprietà CERT Key \_ ID dell' \_ handle \_ prop \_ . Se Schannel trova questo set di proprietà, non usa la proprietà CERT \_ Key \_ prov \_ info \_ prop \_ ID.

## <a name="server-private-keys"></a>Chiavi private del server

Le chiavi private del server vengono archiviate da uno dei CSP seguenti:

-   DIMOSTRAZIONE di \_ RSA \_ Schannel
-   PROV \_ DH \_ Schannel
-   PROVA \_ CSP di fortezza

La scelta del provider CSP dipende dall'algoritmo di [*scambio delle chiavi*](/windows/desktop/SecGloss/k-gly)selezionato. Le chiavi private del server devono essere di tipo in scambio di chiave \_ .

 

 
