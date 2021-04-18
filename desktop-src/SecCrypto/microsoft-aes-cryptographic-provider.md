---
description: Microsoft Enhanced RSA and AES Cryptographic Provider supporta le stesse funzionalità del provider di crittografia di base Microsoft, denominato provider di base.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Provider di crittografia AES Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb4c774eb2cb9d01bcb3a12f5550537abe44b364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307679"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Provider di crittografia AES Microsoft

Microsoft Enhanced RSA and AES Cryptographic Provider supporta le stesse funzionalità del provider di crittografia di base Microsoft, denominato provider di base. Il provider AES supporta una sicurezza più avanzata tramite chiavi più lunghe e algoritmi aggiuntivi. Può essere usato con tutte le versioni di CryptoAPI.

**Windows XP:** Il provider di crittografia Microsoft AES è stato denominato Microsoft Enhanced RSA and AES Cryptographic Provider (prototipo).

Per mantenere la compatibilità con le versioni precedenti del provider, il nome del provider, come definito nel file di intestazione Wincrypt. h, mantiene la designazione della versione 1,0 anche se sono state spedite versioni più recenti di questo provider. Per determinare la versione del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con il parametro *DWPARAM* impostato su PP \_ version. La versione 2,0 è in uso se viene restituito 0x0200.

|                |                             |
|----------------|-----------------------------|
| Tipo di provider: | **PROVA \_ \_ AES RSA**          |
| Nome provider: | **MS \_ Enh \_ RSA \_ AES \_ prov** |



 

Nella tabella seguente vengono evidenziate le differenze tra il provider di base, il provider sicuro e il provider AES. Le [*lunghezze*](../secgloss/k-gly.md) delle chiavi visualizzate sono le lunghezze di chiave predefinite.



| Algoritmo                                                                                | Lunghezza chiave provider di base | Lunghezza chiave provider forte | Lunghezza chiave provider AES                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo di firma della chiave pubblica RSA                                                       | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di scambio di chiave pubblica RSA                                                        | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di crittografia a blocchi RC2                                                           | 40 bit                  | 128 bit                   | è possibile impostare la lunghezza del Salt di 128 bit.<br/> |
| Algoritmo di crittografia del flusso RC4                                                          | 40 bit                  | 128 bit                   | è possibile impostare la lunghezza del Salt di 128 bit.<br/> |
| DES                                                                                      | 56 bit                  | 56 bit                    | 56 bit                                     |
| [*Triple des*](../secgloss/t-gly.md) (2 chiavi) | Non supportato            | 112 bit                   | 112 bit                                    |
| Triple DES (3 tasti)                                                                       | Non supportato            | 168 bit                   | 168 bit                                    |



 

Per un elenco completo degli algoritmi supportati, vedere [algoritmi del provider AES](aes-provider-algorithms.md).

Il provider sicuro, il provider avanzato e il provider AES sono compatibili con le versioni precedenti del provider di base, ad eccezione del fatto che i provider possono generare solo chiavi RC2 o RC4 di lunghezza della chiave predefinita. La lunghezza predefinita per il provider di base è 40 bit. La lunghezza predefinita per il provider AES è 128 bit. Il provider AES, quindi, non può creare chiavi con lunghezze di chiave compatibili con il provider di base. Tuttavia, il provider AES può importare chiavi RC2 e RC4 fino a 128 bit. Il provider AES può pertanto importare e utilizzare chiavi a 40 bit generate utilizzando il provider di base.

 

 
