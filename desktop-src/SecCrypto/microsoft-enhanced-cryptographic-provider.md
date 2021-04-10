---
description: Microsoft Enhanced Cryptographic Provider supporta le stesse funzionalità del provider di crittografia di base Microsoft, ma supporta una sicurezza più avanzata tramite chiavi più lunghe e algoritmi aggiuntivi.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Microsoft Enhanced Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cadaa0b6325dc7d855aa0b7eeb8d7ff5f114cfd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966752"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Microsoft Enhanced Cryptographic Provider

Microsoft Enhanced Cryptographic Provider, denominato provider avanzato, supporta le stesse funzionalità del provider di crittografia di base Microsoft, denominato provider di base. Il provider migliorato supporta una sicurezza più avanzata tramite chiavi più lunghe e algoritmi aggiuntivi. Può essere usato con tutte le versioni di CryptoAPI.

Per mantenere la compatibilità con le versioni precedenti del provider, il nome del provider, come definito nel file di intestazione Wincrypt. h, mantiene la designazione della versione 1,0. Tuttavia, la versione 2,0 di questo provider è attualmente in fase di spedizione. Per determinare la versione del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con l'argomento *DwParam* impostato su **PP \_ Version**. La versione 2,0 è in uso se viene restituito 0x0200.

|                |                        |
|----------------|------------------------|
| Tipo di provider: | **PROV \_ RSA \_ completo**    |
| Nome provider: | **\_prova avanzata \_ ms** |



 

Nella tabella seguente vengono evidenziate le differenze tra il provider di base, il provider sicuro e il provider migliorato. Le lunghezze delle chiavi visualizzate sono le lunghezze di chiave predefinite.



| Algoritmo                                                                                | Lunghezza chiave provider di base | Lunghezza chiave provider forte | Lunghezza chiave provider migliorata                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo di firma della chiave pubblica RSA                                                       | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di scambio di chiave pubblica RSA                                                        | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di crittografia a blocchi RC2                                                           | 40 bit                  | 128 bit                   | è possibile impostare la lunghezza del Salt di 128 bit.<br/> |
| Algoritmo di crittografia del flusso RC4                                                          | 40 bit                  | 128 bit                   | è possibile impostare la lunghezza del Salt di 128 bit.<br/> |
| DES                                                                                      | 56 bit                  | 56 bit                    | 56 bit                                     |
| [*Triple des*](../secgloss/t-gly.md) (2 chiavi) | Non supportato            | 112 bit                   | 112 bit                                    |
| Triple DES (3 tasti)                                                                       | Non supportato            | 168 bit                   | 168 bit                                    |



 

Il provider sicuro e il provider avanzato sono compatibili con le versioni precedenti del provider di base, ad eccezione del fatto che i provider possono generare solo chiavi RC2 o RC4 con la [*lunghezza della chiave*](../secgloss/k-gly.md)predefinita. La lunghezza predefinita per il provider di base è 40 bit. La lunghezza predefinita per il provider migliorato è 128 bit. Il provider avanzato non può quindi creare chiavi con lunghezze di chiave compatibili con il provider di base. Tuttavia, il provider avanzato può importare chiavi RC2 e RC4 fino a 128 bit. Pertanto, il provider avanzato può importare e usare chiavi di bit 40 generate usando il provider di base.

 

 
