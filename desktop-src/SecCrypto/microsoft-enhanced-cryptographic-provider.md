---
description: Microsoft Enhanced Cryptographic Provider supporta le stesse funzionalità di Microsoft Base Cryptographic Provider, ma supporta una sicurezza più avanzata tramite chiavi più lunghe e algoritmi aggiuntivi.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Provider di crittografia avanzato Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60dbe254f9f22623a61de51b044b58df3a52f19f8a0b4f283caba3f59db7974
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425511"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Provider di crittografia avanzato Microsoft

Microsoft Enhanced Cryptographic Provider, denominato Provider avanzato, supporta le stesse funzionalità del provider del servizio di crittografia Microsoft Base, denominato provider di base. Il provider avanzato supporta una sicurezza più avanzata tramite chiavi più lunghe e algoritmi aggiuntivi. Può essere usato con tutte le versioni di CryptoAPI.

Per mantenere la compatibilità con le versioni precedenti del provider, il nome del provider, come definito nel file di intestazione Wincrypt.h, mantiene la designazione della versione 1.0. Tuttavia, la versione 2.0 di questo provider è attualmente disponibile. Per determinare la versione del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con l'argomento *dwParam* impostato su **PP \_ VERSION**. La versione 2.0 è in uso se 0x0200 viene restituito .

|                   | Valore               |
|-------------------|---------------------|
| **Tipo provider** | PROV \_ RSA \_ FULL     |
| **Nome provider** | MS \_ ENHANCED \_ PROV  |



 

Nella tabella seguente vengono evidenziate le differenze tra provider di base, provider sicuro e provider avanzato. Le lunghezze delle chiavi visualizzate sono le lunghezze di chiave predefinite.



| Algoritmo                                                                                | Lunghezza della chiave del provider di base | Lunghezza della chiave del provider sicuro | Lunghezza della chiave del provider avanzata                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo di firma a chiave pubblica RSA                                                       | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di scambio di chiavi pubbliche RSA                                                        | 512 bit                 | 1.024 bit                 | 1.024 bit                                  |
| Algoritmo di crittografia a blocchi RC2                                                           | 40 bit                  | 128 bit                   | 128 bit È possibile impostare La lunghezza del sale.<br/> |
| Algoritmo di crittografia del flusso RC4                                                          | 40 bit                  | 128 bit                   | 128 bit È possibile impostare La lunghezza del sale.<br/> |
| DES                                                                                      | 56 bit                  | 56 bit                    | 56 bit                                     |
| [*Triple DES*](../secgloss/t-gly.md) (2 chiavi) | Non supportato            | 112 bit                   | 112 bit                                    |
| Triple DES (3 tasti)                                                                       | Non supportato            | 168 bit                   | 168 bit                                    |



 

Il provider sicuro e il provider avanzato sono compatibili con le versioni precedenti con il provider di base, ad eccezione del fatto che i provider possono generare solo chiavi RC2 o RC4 di lunghezza [*della chiave predefinita.*](../secgloss/k-gly.md) La lunghezza predefinita per il provider di base è di 40 bit. La lunghezza predefinita per il provider avanzato è di 128 bit. Il provider avanzato non può quindi creare chiavi con lunghezze di chiave compatibili con il provider di base. Tuttavia, il provider avanzato può importare chiavi RC2 e RC4 fino a 128 bit. Pertanto, il provider avanzato può importare e usare chiavi a 40 bit generate usando il provider di base.

 

 
