---
description: I CSP per PROV \_ RSA \_ Schannel devono supportare l' \_ hash SHAMD5 SSL3 di CALG \_ compatibile con il provider del servizio di crittografia di base Microsoft usato nell'autenticazione client SSL 3,0 e TLS 1,0.
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: Tipo di firma RSA SHA/MD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305596"
---
# <a name="shamd5-rsa-signature-type"></a>Tipo di firma RSA SHA/MD5

I CSP per PROV \_ RSA \_ Schannel devono supportare l' \_ hash SHAMD5 SSL3 di CALG \_ compatibile con il provider del servizio di crittografia di base Microsoft usato nell'autenticazione client SSL 3,0 e TLS 1,0. [](../secgloss/h-gly.md) Questo hash è costituito da una concatenazione di un hash [*MD5*](../secgloss/m-gly.md) e di un hash SHA firmato con una chiave privata RSA o Diffie-Hellman. Un handle per un valore hash di questo tipo viene creato tramite la funzione [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) o [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) con CALG \_ SSL3 \_ SHAMD5 come parametro *algido* . Esempi di utilizzo delle funzioni hash sono disponibili nell' [esempio di programma c: creazione e hashing di una chiave di sessione](example-c-program-creating-and-hashing-a-session-key.md) e di un [programma c di esempio: firma di un hash e verifica della firma hash](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).

 

 
