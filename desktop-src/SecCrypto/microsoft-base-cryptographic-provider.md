---
description: Microsoft Base Cryptographic Provider è il provider CSP (Cryptographic Service Provider) iniziale e viene distribuito con CryptoAPI versioni 1.0 e 2.0. Si tratta di un provider per utilizzo generico che supporta le firme digitali e la crittografia dei dati.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Provider del servizio di crittografia di base Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32082fc6cd7ec6d34bd994e3d3122e2b4c06eee290af8074cea0c183e5dd0116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100701"
---
# <a name="microsoft-base-cryptographic-provider"></a>Provider del servizio di crittografia di base Microsoft

Microsoft Base Cryptographic Provider è il provider CSP [*(Cryptographic Service Provider)*](../secgloss/c-gly.md) iniziale e viene distribuito con [*CryptoAPI*](../secgloss/c-gly.md) versioni 1.0 e 2.0. Si tratta di un provider per utilizzo generico che supporta [*le firme digitali e*](../secgloss/d-gly.md) la crittografia dei dati.

L'algoritmo a chiave pubblica RSA viene usato per tutte le operazioni con chiave pubblica.

Per mantenere la compatibilità con le versioni precedenti, la nuova versione del provider mantiene la designazione della versione 1.0 del nome in Wincrypt.h. Tuttavia, la versione 2.0 di questo provider è attualmente in distribuzione. Per determinare la versione effettiva del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con l'argomento *dwParam* impostato su **PP \_ VERSION.** Se 0x0200 viene restituito in *pbData*, è disponibile la versione 2.0.

|                   | Valore            |
|-------------------|------------------|
| **Tipo provider** | PROV \_ RSA \_ FULL  |
| **Nome provider** | MS \_ DEF \_ PROV    |



 

 

 
