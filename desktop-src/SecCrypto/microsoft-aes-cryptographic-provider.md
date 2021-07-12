---
description: Microsoft Enhanced RSA e AES Cryptographic Provider supportano le stesse funzionalità del provider del servizio di crittografia Microsoft Base, denominato provider di base.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Provider di crittografia Microsoft AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2449c53cb828a94c8dd596133c3a8c21c9b0388
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581869"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Provider di crittografia Microsoft AES

Microsoft Enhanced RSA e AES Cryptographic Provider supportano le stesse funzionalità del provider del servizio di crittografia Microsoft Base, denominato provider di base. Il provider AES supporta una sicurezza più avanzata tramite chiavi più lunghe e algoritmi aggiuntivi. Può essere usato con tutte le versioni di CryptoAPI.

**Windows XP:** Microsoft AES Cryptographic Provider è stato denominato Microsoft Enhanced RSA e AES Cryptographic Provider (Prototype).

Per mantenere la compatibilità con le versioni precedenti del provider, il nome del provider, come definito nel file di intestazione Wincrypt.h, mantiene la designazione della versione 1.0 anche se sono state fornite versioni più recenti di questo provider. Per determinare la versione del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con il *parametro dwParam* impostato su PP \_ VERSION. La versione 2.0 è in uso se 0x0200 viene restituito .

|                   | Valore                    |
|-------------------|--------------------------|
| **Tipo provider** | PROV \_ RSA \_ AES           |
| **Nome provider** | MS \_ ENH \_ RSA \_ AES \_ PROV  |



 

Nella tabella seguente vengono evidenziate le differenze tra provider di base, provider sicuro e provider AES. Le [*lunghezze delle chiavi*](../secgloss/k-gly.md) visualizzate sono le lunghezze di chiave predefinite.



| Algoritmo                                                                                | Lunghezza della chiave del provider di base | Lunghezza della chiave del provider sicuro | Lunghezza della chiave del provider AES                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo di firma a chiave pubblica RSA                                                       | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di scambio di chiavi pubbliche RSA                                                        | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di crittografia a blocchi RC2                                                           | 40 bit                  | 128 bit                   | 128 bit È possibile impostare La lunghezza del sale.<br/> |
| Algoritmo di crittografia del flusso RC4                                                          | 40 bit                  | 128 bit                   | 128 bit È possibile impostare La lunghezza del sale.<br/> |
| DES                                                                                      | 56 bit                  | 56 bit                    | 56 bit                                     |
| [*Triple DES*](../secgloss/t-gly.md) (2 chiavi) | Non supportato            | 112 bit                   | 112 bit                                    |
| Triple DES (3 tasti)                                                                       | Non supportato            | 168 bit                   | 168 bit                                    |



 

Per un elenco completo degli algoritmi supportati, vedere [Algoritmi del provider AES](aes-provider-algorithms.md).

Il provider sicuro, il provider avanzato e il provider AES sono compatibili con le versioni precedenti del provider di base, ad eccezione del fatto che i provider possono generare solo chiavi RC2 o RC4 di lunghezza della chiave predefinita. La lunghezza predefinita per il provider di base è 40 bit. La lunghezza predefinita per il provider AES è 128 bit. Il provider AES non può quindi creare chiavi con lunghezze di chiave compatibili con il provider di base. Tuttavia, il provider AES può importare chiavi RC2 e RC4 fino a 128 bit. Pertanto, il provider AES può importare e usare chiavi a 40 bit generate usando il provider di base.

 

 
