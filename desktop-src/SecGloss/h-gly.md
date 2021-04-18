---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera H.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4165b820-30fc-477e-a690-81109f161323
title: H (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665cd90cfc8a849030b6a1cfd1cb4e6d6f687557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314684"
---
# <a name="h-security-glossary"></a>H (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) H [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_handle_gly"></span><span id="_SECURITY_HANDLE_GLY"></span>**gestire**
</dt> <dd>

Token utilizzato per identificare o accedere a un oggetto, ad esempio l'handle di un provider di crittografia, un archivio certificati, un messaggio o una coppia di chiavi.

</dd> <dt>

<span id="_security_hash_gly"></span><span id="_SECURITY_HASH_GLY"></span>**hash**
</dt> <dd>

Risultato di dimensioni fisse ottenuto applicando una funzione matematica (algoritmo di *hash*) a una quantità arbitraria di dati. (Noto anche come "digest del messaggio").

Vedere anche *funzioni di hashing*.

</dd> <dt>

<span id="_security_hash_object_gly"></span><span id="_SECURITY_HASH_OBJECT_GLY"></span>**hash (oggetto)**
</dt> <dd>

Oggetto utilizzato per l'hashing di messaggi o chiavi di sessione. L'oggetto hash viene creato da una chiamata a **CryptCreateHash**. La definizione dell'oggetto è definita dal CSP specificato nella chiamata.

</dd> <dt>

<span id="_security_hashing_algorithm_gly"></span><span id="_SECURITY_HASHING_ALGORITHM_GLY"></span>**algoritmo hash**
</dt> <dd>

Algoritmo utilizzato per generare un valore hash relativo a un dato, ad esempio un messaggio o una chiave di sessione. Alcuni esempi tipici di algoritmi di hash sono MD2, MD4, MD5 e SHA-1.

</dd> <dt>

<span id="_security_hashing_functions_gly"></span><span id="_SECURITY_HASHING_FUNCTIONS_GLY"></span>**funzioni di hashing**
</dt> <dd>

Set di funzioni usate per creare ed eliminare definitivamente gli oggetti hash, ottenere o impostare i parametri di un oggetto hash e i dati hash e le chiavi della sessione.

</dd> <dt>

<span id="_security_hash_based_message_authentication_code_gly"></span><span id="_SECURITY_HASH_BASED_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**Message Authentication Code basato su hash**
</dt> <dd>

HMAC Algoritmo di hashing con chiave simmetrica implementato dai provider del servizio di crittografia Microsoft. Viene usato un HMAC per verificare l'integrità dei dati per garantire che non sia stato modificato durante l'archiviazione o il transito. Può essere usato con qualsiasi algoritmo hash crittografico iterato, ad esempio MD5 o SHA-1. CryptoAPI fa riferimento a questo algoritmo in base al relativo identificatore di algoritmo (CALG \_ HMAC) e alla classe ( \_ hash della classe ALG \_ ).

Vedere anche [*Message Authentication Code*](m-gly.md).

</dd> <dt>

<span id="_security_hcsbc_gly"></span><span id="_SECURITY_HCSBC_GLY"></span>**HCSBC**
</dt> <dd>

Tipo di dati che funge da handle per un contesto di backup di Servizi certificati. Il suo ruolo consiste nel mantenere lo stato del contesto tra il server e le API di backup durante l'esecuzione di un backup.

</dd> <dt>

<span id="_security_hmac_gly"></span><span id="_SECURITY_HMAC_GLY"></span>**HMAC**
</dt> <dd>

Vedere *Message Authentication Code basati su hash*.

</dd> </dl>

 

 



