---
description: Una chiave di crittografia bulk viene generata eseguendo l'hashing di una delle chiavi MAC usando CryptHashSessionKey insieme al contenuto del messaggio e ad altri dati. Il messaggio viene crittografato o decrittografato con una delle chiavi di crittografia bulk nel modo consueto.
ms.assetid: 08174502-3ff1-4c1c-bcd0-46fd85882305
title: Crittografia dei dati in blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecfb55c162e5aa576d8baa3d0ccbc45e9588c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318948"
---
# <a name="bulk-data-encryption"></a>Crittografia dei dati in blocco

Una [*chiave di crittografia bulk*](../secgloss/b-gly.md) viene generata eseguendo l' [*hashing*](../secgloss/h-gly.md) di una delle chiavi Mac usando [**CryptHashSessionKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) insieme al contenuto del messaggio e ad altri dati. Il messaggio viene crittografato o decrittografato con una delle chiavi di crittografia bulk nel modo consueto.

Quando si usa [*una crittografia a blocchi*](../secgloss/b-gly.md), il motore di protocollo [*Schannel*](../secgloss/s-gly.md) esegue tutte le necessarie [*imbottiture*](../secgloss/p-gly.md)di *crittografia a blocchi* . Quando [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) e [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) vengono chiamati, il flag finale è sempre **false** e la lunghezza dei dati è un multiplo di lunghezze di blocco intere.

> [!Note]  
> Il CSP non deve mai memorizzare i dati nel buffer internamente. Dopo che i dati sono stati crittografati o decrittografati, la dimensione del [*testo non crittografato*](../secgloss/p-gly.md) deve sempre corrispondere esattamente alle dimensioni del [*testo*](../secgloss/c-gly.md)crittografato.

 

 

 
