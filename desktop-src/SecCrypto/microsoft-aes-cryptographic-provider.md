---
description: Microsoft Enhanced RSA e AES Cryptographic Provider supportano le stesse funzionalità di Microsoft Base Cryptographic Provider, denominato provider di base.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Provider del servizio di crittografia Microsoft AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ead697543c9846bbc47b61bd26d721811569b2bcea6584b75fad031d9451195
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683171"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Provider del servizio di crittografia Microsoft AES

Microsoft Enhanced RSA e AES Cryptographic Provider supportano le stesse funzionalità di Microsoft Base Cryptographic Provider, denominato provider di base. Il provider AES supporta una sicurezza più avanzata tramite chiavi più lunghe e algoritmi aggiuntivi. Può essere usato con tutte le versioni di CryptoAPI.

**Windows XP:** Microsoft AES Cryptographic Provider è stato denominato Microsoft Enhanced RSA e AES Cryptographic Provider (Prototype).

Per mantenere la compatibilità con le versioni precedenti del provider, il nome del provider, come definito nel file di intestazione Wincrypt.h, mantiene la designazione della versione 1.0 anche se sono state fornite versioni più recenti di questo provider. Per determinare la versione del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con *il parametro dwParam* impostato su PP \_ VERSION. La versione 2.0 è in uso se 0x0200 viene restituito .

|                   | Valore                    |
|-------------------|--------------------------|
| **Tipo provider** | PROV \_ RSA \_ AES           |
| **Nome provider** | MS \_ ENH \_ RSA \_ AES \_ PROV  |



 

Nella tabella seguente sono evidenziate le differenze tra provider di base, provider sicuro e provider AES. Le [*lunghezze di chiave*](../secgloss/k-gly.md) visualizzate sono le lunghezze di chiave predefinite.



| Algoritmo                                                                                | Lunghezza della chiave del provider di base | Lunghezza della chiave del provider sicuro | Lunghezza della chiave del provider AES                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo di firma a chiave pubblica RSA                                                       | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di scambio di chiavi pubbliche RSA                                                        | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di crittografia a blocchi RC2                                                           | 40 bit                  | 128 bit                   | È possibile impostare la lunghezza salt a 128 bit.<br/> |
| Algoritmo di crittografia del flusso RC4                                                          | 40 bit                  | 128 bit                   | È possibile impostare la lunghezza salt a 128 bit.<br/> |
| DES                                                                                      | 56 bit                  | 56 bit                    | 56 bit                                     |
| [*Triple DES*](../secgloss/t-gly.md) (2 chiavi) | Non supportato            | 112 bit                   | 112 bit                                    |
| Triple DES (3 chiavi)                                                                       | Non supportato            | 168 bit                   | 168 bit                                    |



 

Per un elenco completo degli algoritmi supportati, vedere [Algoritmi del provider AES.](aes-provider-algorithms.md)

Il provider sicuro, il provider avanzato e il provider AES sono compatibili con le versioni precedenti del provider di base, ad eccezione del fatto che i provider possono generare solo chiavi RC2 o RC4 con lunghezza di chiave predefinita. La lunghezza predefinita per il provider di base è 40 bit. La lunghezza predefinita per il provider AES è 128 bit. Di conseguenza, il provider AES non può creare chiavi con lunghezze di chiave compatibili con il provider di base. Tuttavia, il provider AES può importare chiavi RC2 e RC4 fino a 128 bit. Di conseguenza, il provider AES può importare e usare chiavi a 40 bit generate tramite il provider di base.

 

 
